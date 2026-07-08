# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/subscription-duplicate-repro.spec.ts >> Subscription duplicate reproduction (user flows) >> Sequential: Visa success then second /s/start is blocked (expect 1 active)
- Location: ui/subscription-duplicate-repro.spec.ts:359:7

# Error details

```
Test timeout of 120000ms exceeded.
```

```
Error: expect(locator).toBeVisible() failed

Locator: getByRole('heading', { name: /welcome to overnght/i })
Expected: visible
Timeout: 90000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 90000ms
  - waiting for getByRole('heading', { name: /welcome to overnght/i })

```

# Test source

```ts
  295 |     const { email, password } = creds;
  296 | 
  297 |     const verified = await ensureDupUserEmailVerified(request, email);
  298 |     if (!verified.ok) {
  299 |       testInfo.skip(true, verified.reason);
  300 |       return;
  301 |     }
  302 | 
  303 |     const before = await countActiveSubs(request, email, password);
  304 |     if (before.active > 0) {
  305 |       testInfo.skip(true, 'Dup user already has active subscription; use a fresh account');
  306 |       return;
  307 |     }
  308 | 
  309 |     const webOrigin = new URL(process.env.BASE_URL || 'http://localhost:3000').origin;
  310 |     const ctx = await browser.newContext();
  311 |     const page1 = await ctx.newPage();
  312 |     const page2 = await ctx.newPage();
  313 | 
  314 |     try {
  315 |       await loginAs(page1, email, password, '/s/start');
  316 |       await page2.goto(`${webOrigin}/s/start`);
  317 | 
  318 |       await Promise.all([dismissBanner(page1), dismissBanner(page2)]);
  319 | 
  320 |       await Promise.all([
  321 |         page1.getByRole('heading', { name: 'Choose Your Plan' }).waitFor({ state: 'visible', timeout: 25_000 }),
  322 |         page2.getByRole('heading', { name: 'Choose Your Plan' }).waitFor({ state: 'visible', timeout: 25_000 }),
  323 |       ]);
  324 | 
  325 |       await Promise.all([openPlanAndPayment(page1), openPlanAndPayment(page2)]);
  326 | 
  327 |       await Promise.all([
  328 |         fillStripeCard(page1, { number: '4242424242424242', cvc: '222' }),
  329 |         fillStripeCard(page2, { number: '5555555555554444', cvc: '222' }),
  330 |       ]);
  331 | 
  332 |       const b1 = page1.getByRole('button', { name: /complete subscription/i });
  333 |       const b2 = page2.getByRole('button', { name: /complete subscription/i });
  334 |       await Promise.all([
  335 |         expect(b1).toBeEnabled({ timeout: 30_000 }),
  336 |         expect(b2).toBeEnabled({ timeout: 30_000 }),
  337 |       ]);
  338 | 
  339 |       await Promise.all([clickPayOnce(page1, b1), clickPayOnce(page2, b2)]);
  340 | 
  341 |       await Promise.all([page1.waitForTimeout(8000), page2.waitForTimeout(8000)]);
  342 | 
  343 |       const after = await countActiveSubs(request, email, password);
  344 |       testLog('dup-repro', 'After parallel pay (same context, two tabs)', after);
  345 |       await testInfo.attach('parallel-same-context-result', {
  346 |         body: JSON.stringify(after, null, 2),
  347 |         contentType: 'application/json',
  348 |       });
  349 | 
  350 |       expect(
  351 |         after.active,
  352 |         `Data integrity: at most one active subscription. Got ${after.active} active of ${after.total} total.`,
  353 |       ).toBeLessThanOrEqual(1);
  354 |     } finally {
  355 |       await ctx.close();
  356 |     }
  357 |   });
  358 | 
  359 |   test('Sequential: Visa success then second /s/start is blocked (expect 1 active)', async ({
  360 |     page,
  361 |     request,
  362 |   }, testInfo) => {
  363 |     const creds = dupCreds();
  364 |     if (!creds) {
  365 |       testInfo.skip(true, 'Set E2E_DUP_USER_EMAIL + E2E_DUP_USER_PASSWORD');
  366 |       return;
  367 |     }
  368 |     const { email, password } = creds;
  369 | 
  370 |     const verified = await ensureDupUserEmailVerified(request, email);
  371 |     if (!verified.ok) {
  372 |       testInfo.skip(true, verified.reason);
  373 |       return;
  374 |     }
  375 | 
  376 |     const before = await countActiveSubs(request, email, password);
  377 |     if (before.active > 0) {
  378 |       testInfo.skip(true, 'Dup user already has active subscription; use a fresh account');
  379 |       return;
  380 |     }
  381 | 
  382 |     await loginAs(page, email, password, '/s/start');
  383 |     await dismissBanner(page);
  384 | 
  385 |     const plan = page.getByRole('heading', { name: 'Choose Your Plan' });
  386 |     await plan.waitFor({ state: 'visible', timeout: 25_000 });
  387 | 
  388 |     await openPlanAndPayment(page);
  389 |     await fillStripeCard(page, { number: '4242424242424242', cvc: '111' });
  390 |     const submit = page.getByRole('button', { name: /complete subscription/i });
  391 |     await expect(submit).toBeEnabled({ timeout: 30_000 });
  392 |     await clickPayOnce(page, submit);
  393 |     await expect(
  394 |       page.getByRole('heading', { name: /welcome to overnght/i }),
> 395 |     ).toBeVisible({ timeout: 90_000 });
      |       ^ Error: expect(locator).toBeVisible() failed
  396 | 
  397 |     await loginAs(page, email, password, '/s/start');
  398 |     await dismissBanner(page);
  399 |     await expect(page).toHaveURL(/\/subscription/, { timeout: 20_000 });
  400 | 
  401 |     const after = await countActiveSubs(request, email, password);
  402 |     expect(
  403 |       after.active,
  404 |       `After one purchase + redirect guard: expected exactly 1 active, got ${after.active}. Subs: ${JSON.stringify(after.subs)}`,
  405 |     ).toBe(1);
  406 |   });
  407 | });
  408 | 
```