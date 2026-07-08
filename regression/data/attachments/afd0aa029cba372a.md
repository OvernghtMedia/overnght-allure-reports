# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/subscription-coupon.spec.ts >> Subscription with coupon >> subscribe with coupon MARIA2025 — 10% discount applied (TC-SUBSCRIPTION-002)
- Location: ui/subscription-coupon.spec.ts:44:7

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: getByText(/-10%|10% off|discount applied|promo applied/i).or(locator('[data-testid*="discount"], [class*="discount"]'))
Expected: visible
Error: strict mode violation: getByText(/-10%|10% off|discount applied|promo applied/i).or(locator('[data-testid*="discount"], [class*="discount"]')) resolved to 2 elements:
    1) <span class="block text-xs font-semibold text-success">10% off</span> aka getByText('10% off', { exact: true })
    2) <p class="mt-2 text-[12.5px] text-success">Coupon applied — 10% off your first payment.</p> aka getByText('Coupon applied — 10% off your')

Call log:
  - Expect "toBeVisible" with timeout 15000ms
  - waiting for getByText(/-10%|10% off|discount applied|promo applied/i).or(locator('[data-testid*="discount"], [class*="discount"]'))

```

# Test source

```ts
  13  | function couponUser(): { email: string; password: string } | null {
  14  |   const email =
  15  |     process.env.E2E_COUPON_USER_EMAIL || process.env.E2E_USER2_EMAIL || '';
  16  |   const password =
  17  |     process.env.E2E_COUPON_USER_PASSWORD ||
  18  |     process.env.E2E_USER2_PASSWORD ||
  19  |     '';
  20  |   if (!email || !password) return null;
  21  |   return { email, password };
  22  | }
  23  | 
  24  | test.describe('Subscription with coupon', () => {
  25  |   // retries: 0 — never retry payment tests to avoid duplicate subscriptions
  26  |   test.describe.configure({ retries: 0 });
  27  | 
  28  |   // Self-cleanup so the coupon account doesn't stay subscribed between runs:
  29  |   // cancel any active sub BEFORE (so the plan picker shows instead of skipping
  30  |   // "already subscribed") and AFTER (leave it clean). No-op without creds.
  31  |   async function resetCouponSubscription() {
  32  |     const creds = couponUser();
  33  |     if (!creds) return;
  34  |     const ctx = await apiRequest.newContext();
  35  |     try {
  36  |       await cancelActiveSubscriptions(ctx, creds.email, creds.password);
  37  |     } finally {
  38  |       await ctx.dispose();
  39  |     }
  40  |   }
  41  |   test.beforeAll(resetCouponSubscription);
  42  |   test.afterAll(resetCouponSubscription);
  43  | 
  44  |   test('subscribe with coupon MARIA2025 — 10% discount applied (TC-SUBSCRIPTION-002)', async ({
  45  |     page,
  46  |   }, testInfo) => {
  47  |     const creds = couponUser();
  48  |     if (!creds) {
  49  |       testInfo.skip(
  50  |         true,
  51  |         'Set E2E_COUPON_USER_EMAIL + E2E_COUPON_USER_PASSWORD (user without active subscription) to run this test',
  52  |       );
  53  |       return;
  54  |     }
  55  | 
  56  |     await test.step('Login & navigate to checkout', async () => {
  57  |       await loginAs(page, creds.email, creds.password, '/s/start');
  58  |     });
  59  | 
  60  |     await test.step('Check plan picker visible', async () => {
  61  |       const hasPlanPicker = await page
  62  |         .getByRole('heading', { name: 'Choose Your Plan' })
  63  |         .waitFor({ state: 'visible', timeout: 15_000 })
  64  |         .then(() => true)
  65  |         .catch(() => false);
  66  | 
  67  |       if (!hasPlanPicker) {
  68  |         testInfo.skip(
  69  |           true,
  70  |           'Account already subscribed — coupon test requires a fresh non-subscriber',
  71  |         );
  72  |         return;
  73  |       }
  74  |     });
  75  | 
  76  |     await test.step('Choose plan', async () => {
  77  |       await page.getByRole('button', { name: 'Get Started' }).first().click();
  78  |       await page
  79  |         .getByText('Payment details', { exact: false })
  80  |         .first()
  81  |         .waitFor({ state: 'visible', timeout: 20_000 });
  82  |     });
  83  | 
  84  |     await test.step('Apply coupon MARIA2025', async () => {
  85  |       const couponInput = page
  86  |         .getByPlaceholder(/coupon|promo.*code|discount.*code/i)
  87  |         .or(page.locator('input[name*="coupon" i], input[name*="promo" i]'))
  88  |         .first();
  89  | 
  90  |       const hasCouponField = await couponInput
  91  |         .waitFor({ state: 'visible', timeout: 10_000 })
  92  |         .then(() => true)
  93  |         .catch(() => false);
  94  | 
  95  |       if (!hasCouponField) {
  96  |         testInfo.annotations.push({
  97  |           type: 'note',
  98  |           description: 'Coupon input field not found on the checkout page — verify UI',
  99  |         });
  100 |         testLog('coupon', 'Coupon input not found, proceeding without coupon');
  101 |       } else {
  102 |         await couponInput.fill('MARIA2025');
  103 |         await page
  104 |           .getByRole('button', { name: /apply/i })
  105 |           .or(page.getByText(/apply coupon/i))
  106 |           .first()
  107 |           .click();
  108 | 
  109 |         await expect(
  110 |           page
  111 |             .getByText(/-10%|10% off|discount applied|promo applied/i)
  112 |             .or(page.locator('[data-testid*="discount"], [class*="discount"]')),
> 113 |         ).toBeVisible({ timeout: 15_000 });
      |           ^ Error: expect(locator).toBeVisible() failed
  114 |         testLog('coupon', 'Coupon MARIA2025 applied — 10% discount visible');
  115 |       }
  116 |     });
  117 | 
  118 |     await test.step('Pay with test card', async () => {
  119 |       await fillStripeCard(page, { number: '4242424242424242', cvc: '111' });
  120 |       const submitBtn = page.getByRole('button', { name: /complete subscription/i });
  121 |       await expect(submitBtn).toBeEnabled({ timeout: 15_000 });
  122 |       await clickPayOnce(page, submitBtn);
  123 |     });
  124 | 
  125 |     await test.step('Subscription success screen', async () => {
  126 |       await expect(
  127 |         page.getByRole('heading', { name: /welcome to overnght/i }),
  128 |       ).toBeVisible({ timeout: 90_000 });
  129 |       testLog('coupon', 'Subscription with coupon purchased successfully');
  130 |     });
  131 |   });
  132 | });
  133 | 
```