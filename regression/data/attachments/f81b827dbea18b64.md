# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/home-banners.spec.ts >> Home Screen Banners >> TC-HOME-BAN-003: hero renders and advances
- Location: ui/home-banners.spec.ts:162:7

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator:  locator('section[aria-label="Featured"]').first().getByRole('heading', { level: 1 }).first()
Expected: visible
Received: undefined
Timeout:  10000ms

Call log:
  - Expect "toBeVisible" with timeout 10000ms
  - waiting for locator('section[aria-label="Featured"]').first().getByRole('heading', { level: 1 }).first()
    - found getByRole('button', { name: /maybe later, continue free/i }), intercepting action to run the handler

```

# Test source

```ts
  82  |       }
  83  |       const label = ((await cta.textContent()) ?? '').toLowerCase();
  84  |       // The hero autoplays + crossfades, so the CTA rarely satisfies Playwright's
  85  |       // "stable" actionability check under parallel load (same churn that broke
  86  |       // TC-AUTH-004). Force the click to skip the stability/interception waits;
  87  |       // unlike dispatchEvent it stays a TRUSTED gesture (BAN-002 needs that for
  88  |       // the link banner's window.open to actually open a tab).
  89  |       await cta.click({ force: true });
  90  | 
  91  |       if (label.includes('watch')) {
  92  |         await expect(page).toHaveURL(/\/event\/[0-9a-f-]{36}/i, { timeout: 15_000 });
  93  |       } else if (label.includes('subscribe')) {
  94  |         await expect(page).toHaveURL(/\/subscription/, { timeout: 15_000 });
  95  |       } else {
  96  |         await expect(page).toHaveURL(/\/auth\/registration/, { timeout: 15_000 });
  97  |       }
  98  |     } finally {
  99  |       await close();
  100 |     }
  101 |   });
  102 | 
  103 |   test('TC-HOME-BAN-002: link banner "Learn more" opens the URL in a new tab', async ({
  104 |     browser,
  105 |   }, testInfo) => {
  106 |     const { page, close } = await openHome(browser);
  107 |     try {
  108 |       // `handleCta` does `window.open(item.link, '_blank', …)`. Catching a real
  109 |       // popup is racy (and gets blocked once the SubscribeNow modal has cycled),
  110 |       // so capture the window.open call instead — same intent, deterministic.
  111 |       await page.evaluate(() => {
  112 |         const w = window as unknown as { __opened?: Array<[string, string]> };
  113 |         w.__opened = [];
  114 |         window.open = ((url?: string | URL, target?: string) => {
  115 |           w.__opened!.push([String(url ?? ''), String(target ?? '')]);
  116 |           return null;
  117 |         }) as typeof window.open;
  118 |       });
  119 | 
  120 |       // Cycle slides and click each "Learn more" until one actually fires
  121 |       // window.open. The FIRST-rendered slide's CTA can be pre-hydration / not yet
  122 |       // wired (observed: slide 0 click is a no-op, the same link banner fires on
  123 |       // its next rotation), so we can't just click the first match.
  124 |       const h = hero(page);
  125 |       await h.scrollIntoViewIfNeeded().catch(() => {});
  126 |       await h.hover().catch(() => {});
  127 |       const next = h.getByRole('button', { name: 'Next slide' });
  128 |       const readOpened = () =>
  129 |         page.evaluate(() => (window as unknown as { __opened: Array<[string, string]> }).__opened);
  130 | 
  131 |       let sawLearn = false;
  132 |       let opened: Array<[string, string]> = [];
  133 |       for (let i = 0; i < 8; i++) {
  134 |         const learn = h.getByRole('button', { name: /learn more/i }).first();
  135 |         if (await learn.isVisible({ timeout: 1_500 }).catch(() => false)) {
  136 |           sawLearn = true;
  137 |           await learn.click({ force: true });
  138 |           await page.waitForTimeout(250);
  139 |           opened = await readOpened();
  140 |           if (opened.length) break;
  141 |         }
  142 |         if (!(await next.isVisible().catch(() => false))) break; // single banner
  143 |         await next.click({ force: true }).catch(() => {});
  144 |         await page.waitForTimeout(700); // crossfade (no-op under reduced motion) + buffer
  145 |       }
  146 | 
  147 |       if (!sawLearn) {
  148 |         testInfo.skip(true, 'No link-type hero banner currently configured');
  149 |         return;
  150 |       }
  151 |       expect(
  152 |         opened.length,
  153 |         '"Learn more" should call window.open for the configured URL',
  154 |       ).toBeGreaterThan(0);
  155 |       expect(opened[0][0], 'opened URL should be absolute http(s)').toMatch(/^https?:\/\//);
  156 |       expect(opened[0][1], 'link banner should open in a new tab').toBe('_blank');
  157 |     } finally {
  158 |       await close();
  159 |     }
  160 |   });
  161 | 
  162 |   test('TC-HOME-BAN-003: hero renders and advances', async ({
  163 |     browser,
  164 |   }, testInfo) => {
  165 |     const { page, close } = await openHome(browser);
  166 |     try {
  167 |       const h = hero(page);
  168 |       await expect(h).toBeVisible({ timeout: 15_000 });
  169 | 
  170 |       const title = h.getByRole('heading', { level: 1 }).first();
  171 |       if (!(await title.isVisible({ timeout: 15_000 }).catch(() => false))) {
  172 |         testInfo.skip(true, 'Hero rail rendered no slide (no banners / not hydrated)');
  173 |         return;
  174 |       }
  175 | 
  176 |       // Advance (if multi-banner) and confirm a slide title is still shown.
  177 |       await h.hover().catch(() => {});
  178 |       const next = h.getByRole('button', { name: 'Next slide' });
  179 |       if (await next.isVisible().catch(() => false)) {
  180 |         await next.click({ force: true });
  181 |         await page.waitForTimeout(900);
> 182 |         await expect(h.getByRole('heading', { level: 1 }).first()).toBeVisible({
      |                                                                    ^ Error: expect(locator).toBeVisible() failed
  183 |           timeout: 10_000,
  184 |         });
  185 |       }
  186 |     } finally {
  187 |       await close();
  188 |     }
  189 |   });
  190 | });
  191 | 
```