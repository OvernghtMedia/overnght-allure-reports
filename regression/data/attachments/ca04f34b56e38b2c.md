# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/home.spec.ts >> Home screen >> TC-HOME-004: navigate to VOD from "See More" on Home
- Location: ui/home.spec.ts:135:7

# Error details

```
TimeoutError: locator.click: Timeout 25000ms exceeded.
Call log:
  - waiting for getByRole('link', { name: /see more|see all/i }).or(locator('a').filter({ hasText: /see more|see all/i })).first()
    - found getByRole('button', { name: /maybe later, continue free/i }), intercepting action to run the handler
    - locator handler has finished
    - interception handler has finished, continuing
    - locator resolved to <a href="/schedule/search" class="flex shrink-0 items-center justify-center rounded-full border border-white/20 bg-black/35 text-white backdrop-blur-md transition cursor-pointer hover:border-white/50 hover:bg-black/55 h-10 px-4 font-body text-sm font-medium">See all</a>
  - attempting click action
    2 × found getByRole('button', { name: /maybe later, continue free/i }), intercepting action to run the handler
      - locator handler has finished
      - interception handler has finished, continuing
      - waiting for element to be visible, enabled and stable
      - element is visible, enabled and stable
      - scrolling into view if needed
      - done scrolling
      - <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 sm:gap-8 md:gap-12 lg:gap-16 items-center">…</div> from <div class="fixed inset-0 z-50 flex items-center justify-center">…</div> subtree intercepts pointer events
    - retrying click action
    - waiting 20ms
    - found getByRole('button', { name: /maybe later, continue free/i }), intercepting action to run the handler
    - locator handler has finished
    - interception handler has finished, continuing
    - waiting for element to be visible, enabled and stable
    - element is visible, enabled and stable
    - scrolling into view if needed
    - done scrolling
    - <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"></div> from <div class="fixed inset-0 z-50 flex items-center justify-center">…</div> subtree intercepts pointer events
  - retrying click action
    - waiting 100ms
    - found getByRole('button', { name: /maybe later, continue free/i }), intercepting action to run the handler

```

# Test source

```ts
  66  |     // ("Explore" drawer with per-sport buttons) was removed. Sports are now
  67  |     // reached from the "Discover most popular sports" home section, which links
  68  |     // straight to `/sports/:slug`. We click the first such link instead of the
  69  |     // old burger → aside flow (which silently skipped after the removal).
  70  |     const { page, close } = await openAuthenticatedHome(browser);
  71  |     try {
  72  |       const sportLink = page.locator('a[href*="/sports/"]').first();
  73  | 
  74  |       // Scroll the home feed until a sport link mounts (lazy sections).
  75  |       for (let i = 0; i < 6; i++) {
  76  |         if (await sportLink.isVisible().catch(() => false)) break;
  77  |         await page.keyboard.press('End');
  78  |         await page.waitForTimeout(500);
  79  |       }
  80  | 
  81  |       if (!(await sportLink.isVisible().catch(() => false))) {
  82  |         testInfo.skip(true, 'No /sports/ link rendered on home — empty catalog?');
  83  |         return;
  84  |       }
  85  | 
  86  |       await sportLink.scrollIntoViewIfNeeded();
  87  |       await sportLink.click();
  88  |       await expect(page).toHaveURL(/\/sports\//, { timeout: 30_000 });
  89  |       await expect(
  90  |         page.getByRole('heading', { level: 1 }),
  91  |       ).toBeVisible({ timeout: 45_000 });
  92  | 
  93  |       const live = page.getByRole('heading', { name: 'Live Now' });
  94  |       const sched = page.getByRole('heading', { name: 'On the Horizon' });
  95  |       const past = page.getByRole('heading', { name: 'All Past Events' });
  96  |       const shows = page.getByRole('heading', { name: 'All Overnght Shows' });
  97  |       const anyH2 = page.getByRole('heading', { level: 2 }).first();
  98  |       await expect(live.or(sched).or(past).or(shows).or(anyH2).first()).toBeVisible({
  99  |         timeout: 60_000,
  100 |       });
  101 |     } finally {
  102 |       await close();
  103 |     }
  104 |   });
  105 | 
  106 |   test('TC-HOME-003: navigate to Event Video Player from event card', async ({
  107 |     browser,
  108 |   }) => {
  109 |     const { page, close } = await openAuthenticatedHome(browser);
  110 |     try {
  111 |       // Find first event card link and click it
  112 |       const eventLink = page.locator('a[href*="/event/"]').first();
  113 |       await eventLink.scrollIntoViewIfNeeded();
  114 |       await expect(eventLink).toBeVisible({ timeout: 60_000 });
  115 |       await eventLink.click();
  116 | 
  117 |       // Verify event page opened
  118 |       await expect(page).toHaveURL(/\/event\//, { timeout: 30_000 });
  119 | 
  120 |       // Accept any valid event page state
  121 |       const player = page.locator('video, [class*="video-js"]').first();
  122 |       const subGate = page.getByRole('heading', { name: /watch with subscription|subscribe/i });
  123 |       const upcomingGate = page.getByRole('heading', { name: /upcoming|scheduled|delayed/i });
  124 |       const geoGate = page.getByRole('heading', { name: /content unavailable|unavailable in your region/i });
  125 |       const notFound = page.getByRole('heading', { name: /offside|not found/i });
  126 | 
  127 |       await expect(
  128 |         player.or(subGate).or(upcomingGate).or(geoGate).or(notFound).first(),
  129 |       ).toBeVisible({ timeout: 45_000 });
  130 |     } finally {
  131 |       await close();
  132 |     }
  133 |   });
  134 | 
  135 |   test('TC-HOME-004: navigate to VOD from "See More" on Home', async ({
  136 |     browser,
  137 |   }, testInfo) => {
  138 |     const { page, close } = await openAuthenticatedHome(browser);
  139 |     try {
  140 |       // Wait for content sections to load
  141 |       const anySection = page.getByRole('heading', { level: 2 }).first();
  142 |       await expect(anySection).toBeVisible({ timeout: 60_000 });
  143 | 
  144 |       // Scroll down to find "See more" / "See all" CTA
  145 |       // Home page has multiple sections, CTAs may be in EventSectionCta
  146 |       const seeMore = page
  147 |         .getByRole('link', { name: /see more|see all/i })
  148 |         .or(page.locator('a').filter({ hasText: /see more|see all/i }))
  149 |         .first();
  150 | 
  151 |       // Scroll through the page looking for the CTA
  152 |       for (let i = 0; i < 5; i++) {
  153 |         if (await seeMore.isVisible().catch(() => false)) break;
  154 |         await page.keyboard.press('End');
  155 |         await page.waitForTimeout(500);
  156 |       }
  157 | 
  158 |       if (!(await seeMore.isVisible().catch(() => false))) {
  159 |         testInfo.annotations.push({ type: 'note', description: '"See More" CTA not found — no content sections may be loaded' });
  160 |         // At least verify the home page loaded
  161 |         await expect(anySection).toBeVisible();
  162 |         return;
  163 |       }
  164 | 
  165 |       await seeMore.scrollIntoViewIfNeeded();
> 166 |       await seeMore.click();
      |                     ^ TimeoutError: locator.click: Timeout 25000ms exceeded.
  167 | 
  168 |       // Should navigate to search or an event list page
  169 |       await expect(page).toHaveURL(/\/search|\/event|\/sports/, {
  170 |         timeout: 20_000,
  171 |       });
  172 |     } finally {
  173 |       await close();
  174 |     }
  175 |   });
  176 | });
  177 | 
```