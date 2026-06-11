# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../api/subscription-duplicate-invariants.spec.ts >> Subscription duplicates — API invariants >> E2E_USER_EMAIL (wallet): at most one active after /login
- Location: api/subscription-duplicate-invariants.spec.ts:89:7

# Error details

```
Error: Login failed HTTP 404: {"success":false,"message":"Cannot POST /api/login","error":"Not Found","statusCode":404}

expect(received).toBeTruthy()

Received: false
```

# Test source

```ts
  1   | import { test, expect } from '@playwright/test';
  2   | import type { APIRequestContext } from '@playwright/test';
  3   | import { getAuthHeaders } from '../utils/auth';
  4   | import { getApiBaseUrl } from '../utils/env';
  5   | 
  6   | /**
  7   |  * Data-integrity checks for "at most one active subscription per user".
  8   |  *
  9   |  * Root-cause analysis: backend only blocks create when an existing row has `active: true`
  10  |  * (see `StripeSubscriptionsService.createSubscription`). Incomplete Stripe subs are stored
  11  |  * with `active: false`, so a second checkout is allowed and can yield two rows that later
  12  |  * both become active. There is no DB partial unique index on (userId) WHERE active.
  13  |  *
  14  |  * Reproduction (manual / future automated with Stripe test keys):
  15  |  * - Parallel POST /v2.0/subscriptions with two different `paymentMethodId` values (different
  16  |  *   Stripe idempotency keys) before either payment settles.
  17  |  * - Or: leave first subscription in `incomplete` + `active: false`, start checkout again.
  18  |  *
  19  |  * Webhook replay does not INSERT rows (handlers only UPDATE by `stripeId`).
  20  |  *
  21  |  * Placeholders (manual / future automation — do NOT use `test.skip(true)` here:
  22  |  * it marks the whole describe as skipped in Playwright):
  23  |  * - Parallel POST /v2.0/subscriptions with two `pm_` IDs (needs Stripe test PM creation).
  24  |  * - Replay Stripe webhook: handlers only UPDATE by `stripeId`; duplicates come from API INSERT paths.
  25  |  */
  26  | 
  27  | type SubscriptionRow = {
  28  |   id: string;
  29  |   active: boolean;
  30  |   status?: string;
  31  | };
  32  | 
  33  | function countActive(subs: SubscriptionRow[] | undefined): number {
  34  |   return (subs ?? []).filter((s) => s.active === true).length;
  35  | }
  36  | 
  37  | async function apiLogin(
  38  |   request: APIRequestContext,
  39  |   email: string,
  40  |   password: string,
  41  | ): Promise<string> {
  42  |   const api = getApiBaseUrl();
  43  |   const res = await request.post(`${api}/login`, {
  44  |     data: { email, password },
  45  |     headers: { 'Content-Type': 'application/json' },
  46  |   });
  47  |   expect(
  48  |     res.ok(),
  49  |     `Login failed HTTP ${res.status()}: ${await res.text()}`,
> 50  |   ).toBeTruthy();
      |     ^ Error: Login failed HTTP 404: {"success":false,"message":"Cannot POST /api/login","error":"Not Found","statusCode":404}
  51  |   const body = (await res.json()) as { token?: string };
  52  |   expect(body.token, 'Login response must include token').toBeTruthy();
  53  |   return body.token as string;
  54  | }
  55  | 
  56  | async function fetchMySubscriptions(
  57  |   request: APIRequestContext,
  58  |   bearer: string,
  59  | ): Promise<SubscriptionRow[]> {
  60  |   const api = getApiBaseUrl();
  61  |   const res = await request.get(`${api}/v2.0/subscriptions`, {
  62  |     headers: {
  63  |       Authorization: `Bearer ${bearer}`,
  64  |       Accept: 'application/json',
  65  |     },
  66  |   });
  67  |   expect(res.ok(), await res.text()).toBeTruthy();
  68  |   const body = (await res.json()) as { subscriptions?: SubscriptionRow[] };
  69  |   return body.subscriptions ?? [];
  70  | }
  71  | 
  72  | test.describe('Subscription duplicates — API invariants', () => {
  73  |   test('REGULAR_TOKEN: at most one active subscription row', async ({
  74  |     request,
  75  |   }) => {
  76  |     const api = getApiBaseUrl();
  77  |     const res = await request.get(`${api}/v2.0/subscriptions`, {
  78  |       headers: getAuthHeaders('regular'),
  79  |     });
  80  |     expect(res.ok(), await res.text()).toBeTruthy();
  81  |     const body = (await res.json()) as { subscriptions?: SubscriptionRow[] };
  82  |     const activeCount = countActive(body.subscriptions);
  83  |     expect(
  84  |       activeCount,
  85  |       'Multiple active subscription rows for the same user — data integrity violation (see subscription-duplicate investigation)',
  86  |     ).toBeLessThanOrEqual(1);
  87  |   });
  88  | 
  89  |   test('E2E_USER_EMAIL (wallet): at most one active after /login', async ({
  90  |     request,
  91  |   }, testInfo) => {
  92  |     const email = process.env.E2E_USER_EMAIL?.trim();
  93  |     const password = process.env.E2E_USER_PASSWORD?.trim();
  94  |     if (!email || !password) {
  95  |       testInfo.skip(true, 'Set E2E_USER_EMAIL + E2E_USER_PASSWORD');
  96  |       return;
  97  |     }
  98  | 
  99  |     const token = await apiLogin(request, email, password);
  100 |     const subs = await fetchMySubscriptions(request, token);
  101 |     const activeCount = countActive(subs);
  102 |     expect(
  103 |       activeCount,
  104 |       `User ${email} has ${activeCount} active subscription(s); expected ≤ 1`,
  105 |     ).toBeLessThanOrEqual(1);
  106 |   });
  107 | 
  108 |   test('Admin user detail: E2E wallet user has ≤ 1 active subscription', async ({
  109 |     request,
  110 |   }, testInfo) => {
  111 |     const adminToken = process.env.ADMIN_TOKEN?.trim();
  112 |     const email = process.env.E2E_USER_EMAIL?.trim();
  113 |     if (!adminToken || !email) {
  114 |       testInfo.skip(true, 'Set ADMIN_TOKEN + E2E_USER_EMAIL');
  115 |       return;
  116 |     }
  117 | 
  118 |     const api = getApiBaseUrl();
  119 |     const listRes = await request.get(`${api}/admin/users`, {
  120 |       headers: {
  121 |         Authorization: `Bearer ${adminToken}`,
  122 |         Accept: 'application/json',
  123 |       },
  124 |       params: { search: email, limit: '10', page: '1' },
  125 |     });
  126 |     expect(listRes.ok(), await listRes.text()).toBeTruthy();
  127 |     const listBody = (await listRes.json()) as {
  128 |       data: { id: string; email: string }[];
  129 |     };
  130 |     const row = listBody.data?.find(
  131 |       (u) => u.email.toLowerCase() === email.toLowerCase(),
  132 |     );
  133 |     expect(row, `Admin search must find user ${email}`).toBeTruthy();
  134 | 
  135 |     const detailRes = await request.get(`${api}/admin/users/${row!.id}`, {
  136 |       headers: {
  137 |         Authorization: `Bearer ${adminToken}`,
  138 |         Accept: 'application/json',
  139 |       },
  140 |     });
  141 |     expect(detailRes.ok(), await detailRes.text()).toBeTruthy();
  142 |     const detail = (await detailRes.json()) as {
  143 |       subscriptions?: SubscriptionRow[];
  144 |     };
  145 |     const activeCount = countActive(detail.subscriptions);
  146 |     expect(
  147 |       activeCount,
  148 |       `Admin view: user ${email} has ${activeCount} active subscription(s)`,
  149 |     ).toBeLessThanOrEqual(1);
  150 |   });
```