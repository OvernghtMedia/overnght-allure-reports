# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/faq.spec.ts >> FAQ >> TC-FAQ-003: deep-link #slug opens the targeted item
- Location: ui/faq.spec.ts:108:7

# Error details

```
Error: expect(locator).toHaveAttribute(expected) failed

Locator:  locator('[id="i-m-experiencing-connection-problems-audio-quality-issues-or-full-screen-viewing-problems-what-should-i-do"] > button[aria-expanded]')
Expected: "true"
Received: "false"
Timeout:  45000ms

Call log:
  - Expect "toHaveAttribute" with timeout 45000ms
  - waiting for locator('[id="i-m-experiencing-connection-problems-audio-quality-issues-or-full-screen-viewing-problems-what-should-i-do"] > button[aria-expanded]')
    48 × locator resolved to <button type="button" aria-expanded="false" class="flex w-full items-center gap-4 text-left px-4 py-[17px] md:px-[22px] md:py-5">…</button>
       - unexpected value "false"

```

# Page snapshot

```yaml
- generic [active] [ref=e1]:
  - generic [ref=e2]:
    - link "Skip to content" [ref=e3] [cursor=pointer]:
      - /url: "#main-content"
    - banner [ref=e4]:
      - generic [ref=e5]:
        - link "Overnght — Home" [ref=e6] [cursor=pointer]:
          - /url: /
          - img "Overnght" [ref=e7]
        - navigation "Primary" [ref=e8]:
          - link "Home" [ref=e9] [cursor=pointer]:
            - /url: /
            - generic [ref=e10]: Home
          - link "Schedule" [ref=e11] [cursor=pointer]:
            - /url: /schedule
            - generic [ref=e12]: Schedule
          - link "Demand" [ref=e13] [cursor=pointer]:
            - /url: /search
            - generic [ref=e14]: Demand
          - link "Explore" [ref=e15] [cursor=pointer]:
            - /url: /explore
            - generic [ref=e16]: Explore
        - generic [ref=e18]:
          - generic:
            - img
          - textbox "Search" [ref=e19]:
            - /placeholder: Search on Overnght …
        - generic [ref=e20]:
          - link "Sign up" [ref=e21] [cursor=pointer]:
            - /url: /auth/registration
          - link "Log in" [ref=e22] [cursor=pointer]:
            - /url: /auth/login
          - link "Help" [ref=e23] [cursor=pointer]:
            - /url: /faq
            - img
    - main [ref=e24]:
      - generic [ref=e30]:
        - generic [ref=e31]:
          - generic [ref=e32]: Help center
          - heading "Frequently asked questions" [level=2] [ref=e34]:
            - text: Frequently
            - text: asked questions
          - paragraph [ref=e35]: Everything you need to know about watching live sport, replays and managing your Overnght membership.
          - generic [ref=e36]:
            - heading "Still need a hand?" [level=3] [ref=e38]
            - paragraph [ref=e39]: Our support team is on the clock around the world, every matchday.
            - link "Email support" [ref=e41] [cursor=pointer]:
              - /url: /contact
              - img
              - generic [ref=e42]: Email support
        - generic [ref=e45]:
          - generic [ref=e46]:
            - button "01 How many devices can I use with my subscription?" [expanded] [ref=e47] [cursor=pointer]:
              - generic [ref=e48]: "01"
              - generic [ref=e49]: How many devices can I use with my subscription?
              - img [ref=e51]
            - paragraph [ref=e56]: Up to 2
          - generic [ref=e57]:
            - button "02 I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?" [ref=e58] [cursor=pointer]:
              - generic [ref=e59]: "02"
              - generic [ref=e60]: I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?
              - img [ref=e62]
            - generic [ref=e64]:
              - paragraph [ref=e65]: "Sorry that you had issues. But to watch events here are some tips:"
              - list [ref=e66]:
                - listitem [ref=e67]: Make sure you are using Google Chrome or Safari.
                - listitem [ref=e68]: Check your internet connection.
                - listitem [ref=e69]:
                  - text: You can click
                  - link "[this link]" [ref=e70] [cursor=pointer]:
                    - /url: https://fiber.google.com/speedtest/
                  - text: to test your connection—issues with connectivity often affect the quality of the transmission.
              - paragraph [ref=e71]
              - paragraph [ref=e72]
          - generic [ref=e73]:
            - button "03 How do I cancel my subscription?" [ref=e74] [cursor=pointer]:
              - generic [ref=e75]: "03"
              - generic [ref=e76]: How do I cancel my subscription?
              - img [ref=e78]
            - list [ref=e81]:
              - listitem [ref=e82]: Click on My account on the header
              - listitem [ref=e83]: Select my account
              - listitem [ref=e84]: Click on cancel subscription
          - generic [ref=e85]:
            - button "04 Why am I still being charged after canceling my subscription?" [ref=e86] [cursor=pointer]:
              - generic [ref=e87]: "04"
              - generic [ref=e88]: Why am I still being charged after canceling my subscription?
              - img [ref=e90]
            - list [ref=e93]:
              - listitem [ref=e94]: If you are being charged, please check your subscription status and click cancel. Cancel subscription is best done on Chrome of Safari web browser on your mobile, tablet or desktop.
              - listitem [ref=e95]: You cannot cancel subscription via mobile app at this time.
          - generic [ref=e96]:
            - button "05 I was unable to watch a live event due to a website or technology problem. Can I get a refund?" [ref=e97] [cursor=pointer]:
              - generic [ref=e98]: "05"
              - generic [ref=e99]: I was unable to watch a live event due to a website or technology problem. Can I get a refund?
              - img [ref=e101]
            - generic [ref=e103]:
              - paragraph [ref=e104]: "Sorry that you had issues. But to watch events here are some tips:"
              - list [ref=e105]:
                - listitem [ref=e106]: Make sure you are using Google Chrome or Safari.
                - listitem [ref=e107]: Check your internet connection.
                - listitem [ref=e108]:
                  - text: You can click
                  - link "[this link]" [ref=e109] [cursor=pointer]:
                    - /url: https://fiber.google.com/speedtest/
                  - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                - listitem [ref=e110]:
                  - text: If the problem persists, please contact us via email at
                  - strong [ref=e111]:
                    - link "support@overnght.com" [ref=e112] [cursor=pointer]:
                      - /url: mailto:support@overnght.com
                  - text: .
              - paragraph [ref=e113]
          - generic [ref=e114]:
            - button "06 What does \"no compatible source\" mean when trying to watch video on my iPhone?" [ref=e115] [cursor=pointer]:
              - generic [ref=e116]: "06"
              - generic [ref=e117]: What does "no compatible source" mean when trying to watch video on my iPhone?
              - img [ref=e119]
            - generic [ref=e121]:
              - list [ref=e122]:
                - listitem [ref=e123]: The video player might not be optimized for in-app browser you're using. Some platforms work better on Chrome and Safari. Please try watching on Chrome or Safari on your mobile, tablet or desktop.
                - listitem [ref=e124]: If your iPhone or browser is not updated, it might lack the necessary codecs or features to play the video. Please try updating and clearing your chache.
              - paragraph [ref=e125]
              - paragraph [ref=e126]
          - generic [ref=e127]:
            - button "07 What type of sports does Overnght stream?" [ref=e128] [cursor=pointer]:
              - generic [ref=e129]: "07"
              - generic [ref=e130]: What type of sports does Overnght stream?
              - img [ref=e132]
            - paragraph [ref=e135]: Overnght is the home of Water Polo and Rowing, but is adding sports from Soccer to Football.
  - alert [ref=e136]
  - region "Notifications Alt+T"
  - generic:
    - list [ref=e137]:
      - img [ref=e139] [cursor=pointer]
      - listitem [ref=e141]:
        - 'generic "Chatbot wrote: Ask us" [ref=e142] [cursor=pointer]': Ask us
    - button "Button to initiate Chatbot Dialogue" [ref=e143] [cursor=pointer]:
      - img "Open or close chat" [ref=e144]
```

# Test source

```ts
  33  |    * mobile search Dialog.Trigger that carries `aria-expanded` but is
  34  |    * `display:none` at desktop width, so a bare `button[aria-expanded]` would
  35  |    * match that hidden header control first.
  36  |    */
  37  |   const ITEM = 'div[id]:has(> button[aria-expanded])';
  38  |   /** Accordion toggles only — direct child buttons of an item row. */
  39  |   const TRIGGER = `${ITEM} > button[aria-expanded]`;
  40  | 
  41  |   test('TC-FAQ-001: /faq loads, first item open by default', { tag: '@smoke' }, async ({ page }) => {
  42  |     await page.goto('/faq', { waitUntil: 'domcontentloaded' });
  43  |     await dismissCookieConsentBarIfPresent(page);
  44  | 
  45  |     await expect(
  46  |       page.getByRole('heading', { name: /frequently asked questions/i }),
  47  |     ).toBeVisible({ timeout: 30_000 });
  48  | 
  49  |     const triggers = page.locator(TRIGGER);
  50  | 
  51  |     // No FAQs from the API → graceful empty state, test still passes.
  52  |     if ((await triggers.count()) === 0) {
  53  |       await expect(page.getByText(/no questions yet/i)).toBeVisible({
  54  |         timeout: 10_000,
  55  |       });
  56  |       return;
  57  |     }
  58  | 
  59  |     // First item is seeded open (SSR + first client render agree).
  60  |     const firstTrigger = triggers.first();
  61  |     await expect(firstTrigger).toHaveAttribute('aria-expanded', 'true');
  62  |     await expect(page.locator('.ds-faq-answer').first()).toBeVisible({
  63  |       timeout: 10_000,
  64  |     });
  65  |   });
  66  | 
  67  |   test('TC-FAQ-002: a collapsed item expands and collapses on click', async ({
  68  |     page,
  69  |   }, testInfo) => {
  70  |     await page.goto('/faq', { waitUntil: 'domcontentloaded' });
  71  |     await dismissCookieConsentBarIfPresent(page);
  72  | 
  73  |     const items = page.locator(ITEM);
  74  |     if ((await items.count()) < 2) {
  75  |       testInfo.skip(true, 'Fewer than two FAQs — no collapsed item to toggle');
  76  |       return;
  77  |     }
  78  | 
  79  |     // The 2nd item is collapsed by default (only the first is seeded open).
  80  |     // Bind to the row, NOT to `[aria-expanded="false"]`: an attribute-valued
  81  |     // locator stops matching the element the moment it flips to "true".
  82  |     const row = items.nth(1);
  83  |     const trigger = row.locator('> button[aria-expanded]');
  84  |     await expect(trigger).toHaveAttribute('aria-expanded', 'false');
  85  |     await trigger.scrollIntoViewIfNeeded();
  86  | 
  87  |     // Retry the click until it sticks — the accordion is a client component, so
  88  |     // a click that lands before hydration is a no-op (flaky under parallel load).
  89  |     await expect(async () => {
  90  |       await trigger.click();
  91  |       await expect(trigger).toHaveAttribute('aria-expanded', 'true', {
  92  |         timeout: 2_000,
  93  |       });
  94  |     }).toPass({ timeout: 20_000 });
  95  | 
  96  |     // The answer inside this row becomes visible (grid row 0fr → 1fr).
  97  |     await expect(row.locator('.ds-faq-answer')).toBeVisible({ timeout: 10_000 });
  98  | 
  99  |     // Toggling again collapses it (items are independent, several can be open).
  100 |     await expect(async () => {
  101 |       await trigger.click();
  102 |       await expect(trigger).toHaveAttribute('aria-expanded', 'false', {
  103 |         timeout: 2_000,
  104 |       });
  105 |     }).toPass({ timeout: 20_000 });
  106 |   });
  107 | 
  108 |   test('TC-FAQ-003: deep-link #slug opens the targeted item', async ({
  109 |     page,
  110 |   }, testInfo) => {
  111 |     // Discover a real slug from the rendered items, then deep-link to it.
  112 |     await page.goto('/faq', { waitUntil: 'domcontentloaded' });
  113 |     await dismissCookieConsentBarIfPresent(page);
  114 | 
  115 |     const items = page.locator(ITEM);
  116 |     if ((await items.count()) < 2) {
  117 |       testInfo.skip(true, 'Fewer than two FAQs — cannot validate a non-first deep-link');
  118 |       return;
  119 |     }
  120 | 
  121 |     // Use the second item to prove it is the hash (not the default-open first).
  122 |     const slug = await items.nth(1).getAttribute('id');
  123 |     expect(slug, 'FAQ item must expose a slug id for deep-linking').toBeTruthy();
  124 | 
  125 |     await page.goto(`/faq#${slug}`, { waitUntil: 'load' });
  126 |     await dismissCookieConsentBarIfPresent(page);
  127 | 
  128 |     // The hash → open happens in a post-hydration effect (FaqAccordion reads
  129 |     // window.location.hash on mount). Hydration can be slow on staging under
  130 |     // parallel load (observed ~23s), so give it a generous budget — the page
  131 |     // itself is light and the ui-project test timeout is 120s.
  132 |     const targeted = page.locator(`[id="${slug}"] > button[aria-expanded]`);
> 133 |     await expect(targeted).toHaveAttribute('aria-expanded', 'true', {
      |                            ^ Error: expect(locator).toHaveAttribute(expected) failed
  134 |       timeout: 45_000,
  135 |     });
  136 |   });
  137 | });
  138 | 
```