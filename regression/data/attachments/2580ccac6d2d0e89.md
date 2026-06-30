# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/test-events-visibility.spec.ts >> Test events visibility (UI) >> Home — admin sees the test event card (highlighted); regular does not
- Location: ui/test-events-visibility.spec.ts:22:7

# Error details

```
Error: expect(locator).toBeVisible() failed

Locator: locator('a[href$="/event/484475e4-6919-4dd9-86f4-0061e3b9ecc6"]').first()
Expected: visible
Timeout: 25000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 25000ms
  - waiting for locator('a[href$="/event/484475e4-6919-4dd9-86f4-0061e3b9ecc6"]').first()

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
          - link "Schedule" [ref=e12] [cursor=pointer]:
            - /url: /schedule
            - generic [ref=e13]: Schedule
          - link "Demand" [ref=e14] [cursor=pointer]:
            - /url: /search
            - generic [ref=e15]: Demand
          - link "Explore" [ref=e16] [cursor=pointer]:
            - /url: /explore
            - generic [ref=e17]: Explore
        - generic [ref=e19]:
          - generic:
            - img
          - textbox "Search" [ref=e20]:
            - /placeholder: Search on Overnght …
        - generic [ref=e21]:
          - button "Account menu" [ref=e23] [cursor=pointer]:
            - generic [ref=e24]: SA
          - link "Help" [ref=e25] [cursor=pointer]:
            - /url: /faq
            - img
    - main [ref=e26]:
      - generic [ref=e29]:
        - region "Featured" [ref=e30]:
          - generic [ref=e31] [cursor=pointer]:
            - img "BLUE DIVISION | MISSION vs. NYAC" [ref=e34]
            - generic:
              - generic:
                - generic:
                  - generic:
                    - generic:
                      - generic: Football
                      - generic: ·
                      - generic: Sat, Jun 27 • 1:00 AM
                  - generic:
                    - generic:
                      - heading "BLUE DIVISION | MISSION vs. NYAC" [level=1]
                  - generic:
                    - button "Watch now" [ref=e35]:
                      - img
                      - text: Watch now
                    - button "Share" [ref=e36]:
                      - img
                      - text: Share
        - generic [ref=e37]:
          - generic [ref=e38]:
            - generic [ref=e40]:
              - heading "Live Now" [level=2] [ref=e43]
              - paragraph [ref=e44]: Join the action happening right now - don't miss a moment
            - 'link "Water Polo: test live 0515" [ref=e47] [cursor=pointer]':
              - /url: /event/f82d40aa-4527-4e5b-8df9-d906abeb4f84?src=card
              - generic [ref=e48]:
                - generic [ref=e50]:
                  - img "test live 0515" [ref=e52]
                  - generic [ref=e54]: CN
                  - generic [ref=e55]: VS
                - generic [ref=e57]: LIVE
                - generic:
                  - generic:
                    - img
              - generic [ref=e58]:
                - generic [ref=e59]: Water Polo
                - heading "test live 0515" [level=3] [ref=e60]
          - generic [ref=e61]:
            - generic [ref=e62]:
              - generic [ref=e63]:
                - heading "On the Horizon" [level=2] [ref=e65]
                - paragraph [ref=e66]: Exciting competitions and events coming your way - set your calendar
              - generic [ref=e67]:
                - link "See all" [ref=e68] [cursor=pointer]:
                  - /url: /schedule/search
                  - generic [ref=e69]: See all
                - generic [ref=e70]:
                  - button "Scroll left" [ref=e71] [cursor=pointer]:
                    - img [ref=e72]
                  - button "Scroll right" [disabled] [ref=e74]:
                    - img [ref=e75]
            - generic [ref=e77]:
              - 'link "Rowing: San Diego Crew Classic" [ref=e79] [cursor=pointer]':
                - /url: /event/88834c9e-1bb1-42d0-afc5-403026dfbbc7?src=card
                - generic [ref=e80]:
                  - img "San Diego Crew Classic" [ref=e82]
                  - generic [ref=e84]: DELAYED
                  - generic [ref=e86]:
                    - img [ref=e87]
                    - text: Mar 28 · 2:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e90]:
                  - generic [ref=e91]: Rowing
                  - heading "San Diego Crew Classic" [level=3] [ref=e92]
              - 'link "Water Polo: Live Test Event Delayed [STG]" [ref=e94] [cursor=pointer]':
                - /url: /event/6336b38e-7254-4c36-b8e2-c9629673cdd4?src=card
                - generic [ref=e95]:
                  - img "Live Test Event Delayed [STG]" [ref=e97]
                  - generic [ref=e99]: DELAYED
                  - generic [ref=e101]:
                    - img [ref=e102]
                    - text: Apr 29 · 12:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e105]:
                  - generic [ref=e106]: Water Polo
                  - heading "Live Test Event Delayed [STG]" [level=3] [ref=e107]
              - 'link "Women''s Water Polo: featured 1" [ref=e109] [cursor=pointer]':
                - /url: /event/c2454e40-5040-4f06-a0e7-d4dfa066e0e6?src=card
                - generic [ref=e110]:
                  - img "featured 1" [ref=e112]
                  - generic [ref=e114]: DELAYED
                  - generic [ref=e116]:
                    - img [ref=e117]
                    - text: Jun 1 · 3:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e120]:
                  - generic [ref=e121]: Women's Water Polo
                  - heading "featured 1" [level=3] [ref=e122]
              - 'link "Women''s Water Polo: featured 2" [ref=e124] [cursor=pointer]':
                - /url: /event/f7c30c7f-f495-4492-813d-ce4654a60ec5?src=card
                - generic [ref=e125]:
                  - img "featured 2" [ref=e127]
                  - generic [ref=e129]: DELAYED
                  - generic [ref=e131]:
                    - img [ref=e132]
                    - text: Jun 2 · 4:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e135]:
                  - generic [ref=e136]: Women's Water Polo
                  - heading "featured 2" [level=3] [ref=e137]
              - 'link "Women''s Water Polo: featured 3" [ref=e139] [cursor=pointer]':
                - /url: /event/8a8afe75-674c-4c35-9d3c-60c2a7dbc30d?src=card
                - generic [ref=e140]:
                  - img "featured 3" [ref=e142]
                  - generic [ref=e144]: DELAYED
                  - generic [ref=e146]:
                    - img [ref=e147]
                    - text: Jun 3 · 5:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e150]:
                  - generic [ref=e151]: Women's Water Polo
                  - heading "featured 3" [level=3] [ref=e152]
              - 'link "Men''s Rowing: test events" [ref=e154] [cursor=pointer]':
                - /url: /event/a9e0cedb-1bf6-4cff-91f3-e7b63ae530af?src=card
                - generic [ref=e155]:
                  - img "test events" [ref=e157]
                  - generic [ref=e159]: DELAYED
                  - generic [ref=e161]:
                    - img [ref=e162]
                    - text: Jun 10 · 6:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e165]:
                  - generic [ref=e166]: Men's Rowing
                  - heading "test events" [level=3] [ref=e167]
              - 'link "Water Polo: event 2" [ref=e169] [cursor=pointer]':
                - /url: /event/5f0bef70-09f8-4400-9d16-8d9b22066701?src=card
                - generic [ref=e170]:
                  - img "event 2" [ref=e172]
                  - generic [ref=e174]: DELAYED
                  - generic [ref=e176]:
                    - img [ref=e177]
                    - text: Jun 11 · 7:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e180]:
                  - generic [ref=e181]: Water Polo
                  - heading "event 2" [level=3] [ref=e182]
              - 'link "Women''s Water Polo: event 3" [ref=e184] [cursor=pointer]':
                - /url: /event/0ccbc356-3ea4-48b1-a4bc-cc0245cca381?src=card
                - generic [ref=e185]:
                  - generic [ref=e187]:
                    - img "event 3" [ref=e189]
                    - img "event 3" [ref=e191]
                    - generic [ref=e192]: VS
                  - generic [ref=e194]: DELAYED
                  - generic [ref=e196]:
                    - img [ref=e197]
                    - text: Jun 13 · 5:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e200]:
                  - generic [ref=e201]: Women's Water Polo
                  - heading "event 3" [level=3] [ref=e202]
              - 'link "Omega Ball: www" [ref=e204] [cursor=pointer]':
                - /url: /event/484475e4-6919-4dd9-86f4-0061e3b9ecc6?src=card
                - generic [ref=e205]:
                  - img "www" [ref=e207]
                  - generic [ref=e209]:
                    - img [ref=e210]
                    - text: Jul 12 · 2:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e213]:
                  - generic [ref=e214]: Omega Ball
                  - heading "www" [level=3] [ref=e215]
          - generic [ref=e216]:
            - generic [ref=e218]:
              - heading "Popular Sports" [level=2] [ref=e220]
              - paragraph [ref=e221]: Explore world-class events and competitions across different sporting disciplines
            - generic [ref=e222]:
              - link "Water Polo" [ref=e223] [cursor=pointer]:
                - /url: /sports/water-polo
                - img [ref=e226]
                - heading "Water Polo" [level=3] [ref=e230]
              - link "Rowing" [ref=e231] [cursor=pointer]:
                - /url: /sports/rowing
                - img [ref=e234]
                - heading "Rowing" [level=3] [ref=e238]
              - link "Football" [ref=e239] [cursor=pointer]:
                - /url: /sports/football
                - img [ref=e242]
                - heading "Football" [level=3] [ref=e246]
          - generic [ref=e247]:
            - generic [ref=e249]:
              - heading "Conferences" [level=2] [ref=e251]
              - paragraph [ref=e252]: Explore sports conferences and leagues
            - generic [ref=e253]:
              - link "European Aquatics Water Polo" [ref=e254] [cursor=pointer]:
                - /url: /conferences/european-aquatics-water-polo
                - img "European Aquatics Water Polo" [ref=e257]
                - heading "European Aquatics Water Polo" [level=3] [ref=e258]
              - link "USAWP" [ref=e259] [cursor=pointer]:
                - /url: /conferences/usawp
                - img "USAWP" [ref=e262]
                - heading "USAWP" [level=3] [ref=e263]
              - link "USRowing" [ref=e264] [cursor=pointer]:
                - /url: /conferences/usrowing
                - img "USRowing" [ref=e267]
                - heading "USRowing" [level=3] [ref=e268]
          - generic [ref=e270]:
            - generic [ref=e273]:
              - generic [ref=e274]: USRowing
              - heading "USRowing" [level=2] [ref=e276]
              - paragraph [ref=e277]: USRowing USRowing USRowing
            - 'link "Men''s Water Polo: 2024 DII Men''s Water Polo Championship Game 1" [ref=e282] [cursor=pointer]':
              - /url: /event/4fafc2e3-8c11-451d-981a-e251ab2d4119?src=card
              - generic [ref=e283]:
                - img "2024 DII Men's Water Polo Championship Game 1" [ref=e285]
                - generic [ref=e287]:
                  - img [ref=e288]
                  - text: Dec 7, 2024
                - generic:
                  - generic:
                    - img
              - generic [ref=e291]:
                - generic [ref=e292]: Men's Water Polo
                - heading "2024 DII Men's Water Polo Championship Game 1" [level=3] [ref=e293]
          - generic [ref=e295]:
            - generic [ref=e297]:
              - generic [ref=e298]:
                - generic [ref=e299]: USRowing
                - heading "USRowing" [level=2] [ref=e301]
                - paragraph [ref=e302]: USRowingUSRowingUSRowingUSRowingUSRowing
              - generic [ref=e303]:
                - button "Scroll left" [disabled] [ref=e304] [cursor=pointer]:
                  - img [ref=e305]
                - button "Scroll right" [ref=e307] [cursor=pointer]:
                  - img [ref=e308]
            - generic [ref=e312]:
              - 'link "Swimming and Diving: 2025/26 Pepperdine Swim & Dive vs Fresno St" [ref=e314] [cursor=pointer]':
                - /url: /event/8b6ee049-b6d5-4854-ba27-990a21567047?src=card
                - generic [ref=e315]:
                  - img "2025/26 Pepperdine Swim & Dive vs Fresno St" [ref=e317]
                  - generic [ref=e319]:
                    - img [ref=e320]
                    - text: Jan 10
                  - generic:
                    - generic:
                      - img
                - generic [ref=e323]:
                  - generic [ref=e324]: Swimming and Diving
                  - heading "2025/26 Pepperdine Swim & Dive vs Fresno St" [level=3] [ref=e325]
              - 'link "Swimming and Diving: 2025/26 Pepperdine Swim & Dive vs Azusa Pacific" [ref=e327] [cursor=pointer]':
                - /url: /event/918a3019-8c93-4593-912d-ff74d4687068?src=card
                - generic [ref=e328]:
                  - img "2025/26 Pepperdine Swim & Dive vs Azusa Pacific" [ref=e330]
                  - generic [ref=e332]:
                    - img [ref=e333]
                    - text: Jan 24
                  - generic:
                    - generic:
                      - img
                - generic [ref=e336]:
                  - generic [ref=e337]: Swimming and Diving
                  - heading "2025/26 Pepperdine Swim & Dive vs Azusa Pacific" [level=3] [ref=e338]
              - 'link "Men''s Water Polo: 2024 National League Championship: NYAC vs.USAWP SR" [ref=e340] [cursor=pointer]':
                - /url: /event/4625c3b5-f56c-411e-9f6c-2b6ca6e9f0e3?src=card
                - generic [ref=e341]:
                  - 'img "2024 National League Championship: NYAC vs.USAWP SR" [ref=e343]'
                  - generic [ref=e345]:
                    - img [ref=e346]
                    - text: Apr 28, 2024
                  - generic:
                    - generic:
                      - img
                - generic [ref=e349]:
                  - generic [ref=e350]: Men's Water Polo
                  - 'heading "2024 National League Championship: NYAC vs.USAWP SR" [level=3] [ref=e351]'
              - 'link "Women''s Water Polo: 2024 MPSF Championship: UCLA vs. CAL" [ref=e353] [cursor=pointer]':
                - /url: /event/f59e62c5-74d7-46ed-afc0-2caee53b9e90?src=card
                - generic [ref=e354]:
                  - generic [ref=e356]:
                    - 'img "2024 MPSF Championship: UCLA vs. CAL" [ref=e358]'
                    - 'img "2024 MPSF Championship: UCLA vs. CAL" [ref=e360]'
                    - generic [ref=e361]: VS
                  - generic [ref=e363]:
                    - img [ref=e364]
                    - text: Apr 28, 2024
                  - generic:
                    - generic:
                      - img
                - generic [ref=e367]:
                  - generic [ref=e368]: Women's Water Polo
                  - 'heading "2024 MPSF Championship: UCLA vs. CAL" [level=3] [ref=e369]'
              - 'link "Rowing: 2024 INTERCOLLEGIATE ROWING ASSOCIATION (IRA) Championships: Day 3" [ref=e371] [cursor=pointer]':
                - /url: /event/1ac4e76f-7978-4e5c-aabd-b53e4ec4d42d?src=card
                - generic [ref=e372]:
                  - 'img "2024 INTERCOLLEGIATE ROWING ASSOCIATION (IRA) Championships: Day 3" [ref=e374]'
                  - generic [ref=e376]:
                    - img [ref=e377]
                    - text: Jun 2, 2024
                  - generic:
                    - generic:
                      - img
                - generic [ref=e380]:
                  - generic [ref=e381]: Rowing
                  - 'heading "2024 INTERCOLLEGIATE ROWING ASSOCIATION (IRA) Championships: Day 3" [level=3] [ref=e382]'
          - generic [ref=e383]:
            - generic [ref=e384]:
              - generic [ref=e385]:
                - heading "Featured Past Events" [level=2] [ref=e387]
                - paragraph [ref=e388]: The main competition you can't miss
              - generic [ref=e389]:
                - link "See all" [ref=e390] [cursor=pointer]:
                  - /url: /search?featured=1
                  - generic [ref=e391]: See all
                - generic [ref=e392]:
                  - button "Scroll left" [disabled] [ref=e393]:
                    - img [ref=e394]
                  - button "Scroll right" [ref=e396] [cursor=pointer]:
                    - img [ref=e397]
            - generic [ref=e399]:
              - 'link "Men''s Water Polo: Super Cup 2025 - Pro Recco vs. FTC" [ref=e401] [cursor=pointer]':
                - /url: /event/1cf33c12-e9e0-4652-a835-c29574f0fc03?src=card
                - generic [ref=e402]:
                  - img "Super Cup 2025 - Pro Recco vs. FTC" [ref=e404]
                  - generic [ref=e406]:
                    - img [ref=e407]
                    - text: Oct 8, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e410]:
                  - generic [ref=e411]: Men's Water Polo
                  - heading "Super Cup 2025 - Pro Recco vs. FTC" [level=3] [ref=e412]
              - 'link "Men''s Water Polo: Princeton vs. FTC Telekom" [ref=e414] [cursor=pointer]':
                - /url: /event/3b1b3223-425c-4845-81a9-a086fe1a8e3a?src=card
                - generic [ref=e415]:
                  - img "Princeton vs. FTC Telekom" [ref=e417]
                  - generic [ref=e419]:
                    - img [ref=e420]
                    - text: Sep 3, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e423]:
                  - generic [ref=e424]: Men's Water Polo
                  - heading "Princeton vs. FTC Telekom" [level=3] [ref=e425]
              - 'link "Men''s Water Polo: Pro Recco vs. UCLA" [ref=e427] [cursor=pointer]':
                - /url: /event/c5da92ff-029c-4254-96cc-a9c538074b60?src=card
                - generic [ref=e428]:
                  - img "Pro Recco vs. UCLA" [ref=e430]
                  - generic [ref=e432]:
                    - img [ref=e433]
                    - text: Sep 3, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e436]:
                  - generic [ref=e437]: Men's Water Polo
                  - heading "Pro Recco vs. UCLA" [level=3] [ref=e438]
              - 'link "Rowing: 2025 Day 1: USRowing RowFest National Championships" [ref=e440] [cursor=pointer]':
                - /url: /event/ec27439e-c22b-4079-ab8e-3aa0d9f76f16?src=card
                - generic [ref=e441]:
                  - 'img "2025 Day 1: USRowing RowFest National Championships" [ref=e443]'
                  - generic [ref=e445]:
                    - img [ref=e446]
                    - text: Jul 12, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e449]:
                  - generic [ref=e450]: Rowing
                  - 'heading "2025 Day 1: USRowing RowFest National Championships" [level=3] [ref=e451]'
              - 'link "Rowing: Day 2: 2025 USRowing Youth National Championships" [ref=e453] [cursor=pointer]':
                - /url: /event/68f89bac-bb5a-4d03-a390-070137b179b3?src=card
                - generic [ref=e454]:
                  - 'img "Day 2: 2025 USRowing Youth National Championships" [ref=e456]'
                  - generic [ref=e458]:
                    - img [ref=e459]
                    - text: Jun 13, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e462]:
                  - generic [ref=e463]: Rowing
                  - 'heading "Day 2: 2025 USRowing Youth National Championships" [level=3] [ref=e464]'
              - 'link "Rowing: Day 1: 2025 USRowing Youth National Championships" [ref=e466] [cursor=pointer]':
                - /url: /event/a398171a-d01f-4b99-8cdf-e3c7738f1f07?src=card
                - generic [ref=e467]:
                  - 'img "Day 1: 2025 USRowing Youth National Championships" [ref=e469]'
                  - generic [ref=e471]:
                    - img [ref=e472]
                    - text: Jun 12, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e475]:
                  - generic [ref=e476]: Rowing
                  - 'heading "Day 1: 2025 USRowing Youth National Championships" [level=3] [ref=e477]'
          - generic [ref=e478]:
            - generic [ref=e479]:
              - generic [ref=e480]:
                - heading "Featured Overnght Shows" [level=2] [ref=e482]
                - paragraph [ref=e483]: Unique sports talk and behind-the-scenes shows, only here
              - link "See all" [ref=e485] [cursor=pointer]:
                - /url: /search?show=1&featured=1
                - generic [ref=e486]: See all
            - generic [ref=e487]:
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e489] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5?src=card
                - article [ref=e490]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e493]
                  - generic [ref=e494]:
                    - generic [ref=e495]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e496]
                    - generic [ref=e497]: Rowing
                    - generic [ref=e498]:
                      - img [ref=e499]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e502] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980?src=card
                - article [ref=e503]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e506]
                  - generic [ref=e507]:
                    - generic [ref=e508]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e509]
                    - generic [ref=e510]: Rowing
                    - generic [ref=e511]:
                      - img [ref=e512]
                      - text: Watch Now
          - generic [ref=e514]:
            - generic [ref=e515]:
              - generic [ref=e516]:
                - heading "All Overnght Shows" [level=2] [ref=e518]
                - paragraph [ref=e519]: Late-night sports content and exclusive shows
              - generic [ref=e520]:
                - link "See all" [ref=e521] [cursor=pointer]:
                  - /url: /search?show=1
                  - generic [ref=e522]: See all
                - generic [ref=e523]:
                  - button "Scroll left" [disabled] [ref=e524]:
                    - img [ref=e525]
                  - button "Scroll right" [ref=e527] [cursor=pointer]:
                    - img [ref=e528]
            - generic [ref=e530]:
              - link "The Counter Attack ON Overnght Ep 41 | March 4, 2026 — show" [ref=e532] [cursor=pointer]:
                - /url: /event/4ad7c642-76de-4694-a9ed-052243bb959c?src=card
                - article [ref=e533]:
                  - img "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [ref=e536]
                  - generic [ref=e537]:
                    - generic [ref=e538]: Mar 5 · 6:15 PM
                    - heading "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [level=3] [ref=e539]
                    - generic [ref=e540]: Water Polo
                    - generic [ref=e541]:
                      - img [ref=e542]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 25, 2026 — show" [ref=e545] [cursor=pointer]:
                - /url: /event/5c84a6fd-6320-4b8d-b159-2c58f8908b15?src=card
                - article [ref=e546]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [ref=e549]
                  - generic [ref=e550]:
                    - generic [ref=e551]: Mar 2 · 7:15 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [level=3] [ref=e552]
                    - generic [ref=e553]: Water Polo
                    - generic [ref=e554]:
                      - img [ref=e555]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 26, 2026 — show" [ref=e558] [cursor=pointer]:
                - /url: /event/1635113c-beee-489c-b512-5153efb101e1?src=card
                - article [ref=e559]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [ref=e562]
                  - generic [ref=e563]:
                    - generic [ref=e564]: Feb 26 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [level=3] [ref=e565]
                    - generic [ref=e566]: Water Polo
                    - generic [ref=e567]:
                      - img [ref=e568]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.4 — show" [ref=e571] [cursor=pointer]:
                - /url: /event/c4a63e93-2463-42da-8405-c439d7560aa1?src=card
                - article [ref=e572]:
                  - img "Rowing Wolf Podcast, Ep1.4" [ref=e575]
                  - generic [ref=e576]:
                    - generic [ref=e577]: Feb 24 · 10:05 PM
                    - heading "Rowing Wolf Podcast, Ep1.4" [level=3] [ref=e578]
                    - generic [ref=e579]: Rowing
                    - generic [ref=e580]:
                      - img [ref=e581]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 39 | February 18, 2026 — show" [ref=e584] [cursor=pointer]:
                - /url: /event/bca89acc-e481-4d23-8e93-df683231f507?src=card
                - article [ref=e585]:
                  - img "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [ref=e588]
                  - generic [ref=e589]:
                    - generic [ref=e590]: Feb 20 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [level=3] [ref=e591]
                    - generic [ref=e592]: Water Polo
                    - generic [ref=e593]:
                      - img [ref=e594]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e597] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5?src=card
                - article [ref=e598]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e601]
                  - generic [ref=e602]:
                    - generic [ref=e603]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e604]
                    - generic [ref=e605]: Rowing
                    - generic [ref=e606]:
                      - img [ref=e607]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e610] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980?src=card
                - article [ref=e611]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e614]
                  - generic [ref=e615]:
                    - generic [ref=e616]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e617]
                    - generic [ref=e618]: Rowing
                    - generic [ref=e619]:
                      - img [ref=e620]
                      - text: Watch Now
              - link "2025 Cutino Awards — show" [ref=e623] [cursor=pointer]:
                - /url: /event/6f99d5e7-fb65-429d-9024-fef463d2f2d4?src=card
                - article [ref=e624]:
                  - img "2025 Cutino Awards" [ref=e627]
                  - generic [ref=e628]:
                    - generic [ref=e629]: Jun 8, 2025 · 1:45 AM
                    - heading "2025 Cutino Awards" [level=3] [ref=e630]
                    - generic [ref=e631]: Water Polo
                    - generic [ref=e632]:
                      - img [ref=e633]
                      - text: Watch Now
              - link "JRN IRA National Championship Day Three Review — show" [ref=e636] [cursor=pointer]:
                - /url: /event/1ae42c95-a95b-4e4a-a9cc-99615adc4d67?src=card
                - article [ref=e637]:
                  - img "JRN IRA National Championship Day Three Review" [ref=e640]
                  - generic [ref=e641]:
                    - generic [ref=e642]: Jun 1, 2025 · 9:40 PM
                    - heading "JRN IRA National Championship Day Three Review" [level=3] [ref=e643]
                    - generic [ref=e644]: Rowing
                    - generic [ref=e645]:
                      - img [ref=e646]
                      - text: Watch Now
          - generic [ref=e648]:
            - generic [ref=e649]:
              - generic [ref=e650]:
                - heading "All Past Events" [level=2] [ref=e652]
                - paragraph [ref=e653]: Browse every event in one place
              - generic [ref=e654]:
                - link "See all" [ref=e655] [cursor=pointer]:
                  - /url: /search
                  - generic [ref=e656]: See all
                - generic [ref=e657]:
                  - button "Scroll left" [disabled] [ref=e658]:
                    - img [ref=e659]
                  - button "Scroll right" [ref=e661] [cursor=pointer]:
                    - img [ref=e662]
            - generic [ref=e664]:
              - 'link "Football: Germany vs Paraguay" [ref=e666] [cursor=pointer]':
                - /url: /event/058e1113-02c6-47e6-8dc8-9e3524836be9?src=card
                - generic [ref=e667]:
                  - img "Germany vs Paraguay" [ref=e669]
                  - generic [ref=e671]:
                    - img [ref=e672]
                    - text: Jun 30
                  - generic:
                    - generic:
                      - img
                - generic [ref=e675]:
                  - generic [ref=e676]: Football
                  - heading "Germany vs Paraguay" [level=3] [ref=e677]
              - 'link "Football: Brazil vs Japan" [ref=e679] [cursor=pointer]':
                - /url: /event/098faf6d-6164-4e5e-a9ed-c36772f1f707?src=card
                - generic [ref=e680]:
                  - img "Brazil vs Japan" [ref=e682]
                  - generic [ref=e684]:
                    - img [ref=e685]
                    - text: Jun 29
                  - generic:
                    - generic:
                      - img
                - generic [ref=e688]:
                  - generic [ref=e689]: Football
                  - heading "Brazil vs Japan" [level=3] [ref=e690]
              - 'link "Football: Norway vs France" [ref=e692] [cursor=pointer]':
                - /url: /event/a07fe0ea-a713-434a-98f9-32271e663257?src=card
                - generic [ref=e693]:
                  - img "Norway vs France" [ref=e695]
                  - generic [ref=e697]:
                    - img [ref=e698]
                    - text: Jun 27
                  - generic:
                    - generic:
                      - img
                - generic [ref=e701]:
                  - generic [ref=e702]: Football
                  - heading "Norway vs France" [level=3] [ref=e703]
              - 'link "Water Polo: VOD Test Event Scheduled [STG]" [ref=e705] [cursor=pointer]':
                - /url: /event/27963fc8-f89c-4fed-a2a5-84c6d20060a7?src=card
                - generic [ref=e706]:
                  - img "VOD Test Event Scheduled [STG]" [ref=e708]
                  - generic [ref=e710]:
                    - img [ref=e711]
                    - text: May 28
                  - generic:
                    - generic:
                      - img
                - generic [ref=e714]:
                  - generic [ref=e715]: Water Polo
                  - heading "VOD Test Event Scheduled [STG]" [level=3] [ref=e716]
              - 'link "Water Polo: Live test event 0512" [ref=e718] [cursor=pointer]':
                - /url: /event/27aac4b3-ccca-478e-b178-e76424220b40?src=card
                - generic [ref=e719]:
                  - generic [ref=e721]:
                    - img "Live test event 0512" [ref=e723]
                    - generic [ref=e725]: CN
                    - generic [ref=e726]: VS
                  - generic [ref=e728]:
                    - img [ref=e729]
                    - text: May 12
                  - generic:
                    - generic:
                      - img
                - generic [ref=e732]:
                  - generic [ref=e733]: Water Polo
                  - heading "Live test event 0512" [level=3] [ref=e734]
              - 'link "Water Polo: Live Event for Autotests" [ref=e736] [cursor=pointer]':
                - /url: /event/7dfe92c5-6773-4025-980f-3924167d6114?src=card
                - generic [ref=e737]:
                  - generic [ref=e739]:
                    - img "Live Event for Autotests" [ref=e741]
                    - img "Live Event for Autotests" [ref=e743]
                    - generic [ref=e744]: VS
                  - generic [ref=e746]:
                    - img [ref=e747]
                    - text: May 11
                  - generic:
                    - generic:
                      - img
                - generic [ref=e750]:
                  - generic [ref=e751]: Water Polo
                  - heading "Live Event for Autotests" [level=3] [ref=e752]
              - 'link "Water Polo: Test Event VOD [STG]" [ref=e754] [cursor=pointer]':
                - /url: /event/94655734-5203-40b3-9cc4-62892d56c829?src=card
                - generic [ref=e755]:
                  - img "Test Event VOD [STG]" [ref=e757]
                  - generic [ref=e759]:
                    - img [ref=e760]
                    - text: Apr 28
                  - generic:
                    - generic:
                      - img
                - generic [ref=e763]:
                  - generic [ref=e764]: Water Polo
                  - heading "Test Event VOD [STG]" [level=3] [ref=e765]
              - 'link "Water Polo: Event B" [ref=e767] [cursor=pointer]':
                - /url: /event/3b4001ce-9481-4f9d-871e-367c8b47d5a7?src=card
                - generic [ref=e768]:
                  - img "Event B" [ref=e770]
                  - generic [ref=e772]:
                    - img [ref=e773]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e776]:
                  - generic [ref=e777]: Water Polo
                  - heading "Event B" [level=3] [ref=e778]
              - 'link "Water Polo: Event A" [ref=e780] [cursor=pointer]':
                - /url: /event/d1ea6b2b-f306-4ee2-b893-5b0fe4199522?src=card
                - generic [ref=e781]:
                  - img "Event A" [ref=e783]
                  - generic [ref=e785]:
                    - img [ref=e786]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e789]:
                  - generic [ref=e790]: Water Polo
                  - heading "Event A" [level=3] [ref=e791]
        - generic [ref=e794]:
          - generic [ref=e795]:
            - generic [ref=e796]: Help center
            - heading "Questions? Answered." [level=2] [ref=e798]:
              - text: Questions?
              - text: Answered.
            - paragraph [ref=e799]: The essentials about watching, replays and your membership — in one tap.
            - generic [ref=e800]:
              - heading "Still need a hand?" [level=3] [ref=e802]
              - paragraph [ref=e803]: Support is on the clock worldwide, every matchday.
              - link "Email" [ref=e805] [cursor=pointer]:
                - /url: /contact
                - img
                - generic [ref=e806]: Email
          - generic [ref=e808]:
            - generic [ref=e809]:
              - generic [ref=e810]:
                - button "01 How many devices can I use with my subscription?" [expanded] [ref=e811] [cursor=pointer]:
                  - generic [ref=e812]: "01"
                  - generic [ref=e813]: How many devices can I use with my subscription?
                  - img [ref=e815]
                - paragraph [ref=e820]: Up to 2
              - generic [ref=e821]:
                - button "02 I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?" [ref=e822] [cursor=pointer]:
                  - generic [ref=e823]: "02"
                  - generic [ref=e824]: I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?
                  - img [ref=e826]
                - generic [ref=e828]:
                  - paragraph [ref=e829]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e830]:
                    - listitem [ref=e831]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e832]: Check your internet connection.
                    - listitem [ref=e833]:
                      - text: You can click
                      - link "[this link]" [ref=e834] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                  - paragraph [ref=e835]
                  - paragraph [ref=e836]
              - generic [ref=e837]:
                - button "03 How do I cancel my subscription?" [ref=e838] [cursor=pointer]:
                  - generic [ref=e839]: "03"
                  - generic [ref=e840]: How do I cancel my subscription?
                  - img [ref=e842]
                - list [ref=e845]:
                  - listitem [ref=e846]: Click on My account on the header
                  - listitem [ref=e847]: Select my account
                  - listitem [ref=e848]: Click on cancel subscription
              - generic [ref=e849]:
                - button "04 Why am I still being charged after canceling my subscription?" [ref=e850] [cursor=pointer]:
                  - generic [ref=e851]: "04"
                  - generic [ref=e852]: Why am I still being charged after canceling my subscription?
                  - img [ref=e854]
                - list [ref=e857]:
                  - listitem [ref=e858]: If you are being charged, please check your subscription status and click cancel. Cancel subscription is best done on Chrome of Safari web browser on your mobile, tablet or desktop.
                  - listitem [ref=e859]: You cannot cancel subscription via mobile app at this time.
              - generic [ref=e860]:
                - button "05 I was unable to watch a live event due to a website or technology problem. Can I get a refund?" [ref=e861] [cursor=pointer]:
                  - generic [ref=e862]: "05"
                  - generic [ref=e863]: I was unable to watch a live event due to a website or technology problem. Can I get a refund?
                  - img [ref=e865]
                - generic [ref=e867]:
                  - paragraph [ref=e868]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e869]:
                    - listitem [ref=e870]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e871]: Check your internet connection.
                    - listitem [ref=e872]:
                      - text: You can click
                      - link "[this link]" [ref=e873] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                    - listitem [ref=e874]:
                      - text: If the problem persists, please contact us via email at
                      - strong [ref=e875]:
                        - link "support@overnght.com" [ref=e876] [cursor=pointer]:
                          - /url: mailto:support@overnght.com
                      - text: .
                  - paragraph [ref=e877]
            - link "See all FAQs" [ref=e878] [cursor=pointer]:
              - /url: /faq
              - text: See all FAQs
              - img [ref=e879]
        - generic [ref=e882]:
          - generic [ref=e883]:
            - generic [ref=e884]:
              - generic [ref=e885]:
                - link "Overnght — Home" [ref=e886] [cursor=pointer]:
                  - /url: /
                  - img [ref=e887]
                - paragraph [ref=e890]: Live sports and exclusive content. Watch live or on demand, in HD.
              - generic [ref=e891]:
                - link "Download Overnght on the App Store" [ref=e892] [cursor=pointer]:
                  - /url: https://apps.apple.com/us/app/overnght/id6476713008
                  - img [ref=e893]
                  - generic [ref=e895]:
                    - generic [ref=e896]: Download on the
                    - generic [ref=e897]: App Store
                - link "Get Overnght on Google Play" [ref=e898] [cursor=pointer]:
                  - /url: https://play.google.com/store/apps/details?id=com.overnght.app
                  - img [ref=e899]
                  - generic [ref=e901]:
                    - generic [ref=e902]: Get it on
                    - generic [ref=e903]: Google Play
            - navigation "Footer" [ref=e904]:
              - generic [ref=e905]:
                - heading "Watch" [level=3] [ref=e906]
                - list [ref=e907]:
                  - listitem [ref=e908]:
                    - link "Home" [ref=e909] [cursor=pointer]:
                      - /url: /
                  - listitem [ref=e910]:
                    - link "Schedule" [ref=e911] [cursor=pointer]:
                      - /url: /schedule
                  - listitem [ref=e912]:
                    - link "On Demand" [ref=e913] [cursor=pointer]:
                      - /url: /search
              - generic [ref=e914]:
                - heading "Account" [level=3] [ref=e915]
                - list [ref=e916]:
                  - listitem [ref=e917]:
                    - link "My account" [ref=e918] [cursor=pointer]:
                      - /url: /account
                  - listitem [ref=e919]:
                    - link "Subscription" [ref=e920] [cursor=pointer]:
                      - /url: /subscription
              - generic [ref=e921]:
                - heading "Support" [level=3] [ref=e922]
                - list [ref=e923]:
                  - listitem [ref=e924]:
                    - link "FAQ" [ref=e925] [cursor=pointer]:
                      - /url: /faq
                  - listitem [ref=e926]:
                    - link "Contact" [ref=e927] [cursor=pointer]:
                      - /url: /contact
          - generic [ref=e928]:
            - paragraph [ref=e929]: © Overnght 2026
            - navigation "Legal" [ref=e930]:
              - link "Privacy Policy" [ref=e931] [cursor=pointer]:
                - /url: /legalese/termsOfService#privacy-policy
              - link "Terms of Use" [ref=e932] [cursor=pointer]:
                - /url: /legalese/termsOfService
  - alert [ref=e933]
  - region "Notifications Alt+T"
  - generic:
    - list [ref=e934]:
      - img [ref=e936] [cursor=pointer]
      - listitem [ref=e938]:
        - 'generic "Chatbot wrote: Ask us" [ref=e939] [cursor=pointer]': Ask us
    - button "Button to initiate Chatbot Dialogue" [ref=e940] [cursor=pointer]:
      - img "Open or close chat" [ref=e941]
```

# Test source

```ts
  1   | import { test, expect, request as playwrightRequest } from '@playwright/test';
  2   | import { requireEnv, resolveApiBaseUrl, resolveWebBaseUrl, setSessionCookie } from '../utils/auth';
  3   | import { getTestAndProdEvents } from '../utils/events';
  4   | 
  5   | test.describe('Test events visibility (UI)', () => {
  6   |   test.describe.configure({ mode: 'serial' });
  7   | 
  8   |   let testEvent: { id: string; name: string; isTest: boolean; isFree?: boolean };
  9   | 
  10  |   test.beforeAll(async () => {
  11  |     const api = await playwrightRequest.newContext({
  12  |       baseURL: resolveApiBaseUrl(),
  13  |     });
  14  |     try {
  15  |       const bundle = await getTestAndProdEvents(api);
  16  |       testEvent = bundle.testEvent;
  17  |     } finally {
  18  |       await api.dispose();
  19  |     }
  20  |   });
  21  | 
  22  |   test('Home — admin sees the test event card (highlighted); regular does not', async ({
  23  |     browser,
  24  |   }) => {
  25  |     const webBase = resolveWebBaseUrl();
  26  | 
  27  |     const adminContext = await browser.newContext();
  28  |     await setSessionCookie(adminContext, requireEnv('ADMIN_TOKEN'), webBase);
  29  |     const adminPage = await adminContext.newPage();
  30  |     await adminPage.goto('/', { waitUntil: 'domcontentloaded' });
  31  |     await adminPage.getByRole('link', { name: testEvent.name }).first().scrollIntoViewIfNeeded();
  32  |     await expect(
  33  |       adminPage.getByRole('link', { name: testEvent.name }).first(),
  34  |     ).toBeVisible({ timeout: 45_000 });
  35  | 
  36  |     const testCard = adminPage.locator(`a[href$="/event/${testEvent.id}"]`).first();
> 37  |     await expect(testCard).toBeVisible();
      |                            ^ Error: expect(locator).toBeVisible() failed
  38  |     // Admin highlight on a test-event card is `ring-2 ring-danger/70`
  39  |     // (EventCard.tsx) — the old `ring-red-500` class was replaced by the DS
  40  |     // `ring-danger` token.
  41  |     await expect(
  42  |       testCard.locator('[class*="ring-danger"]').first(),
  43  |     ).toBeVisible();
  44  | 
  45  |     await adminContext.close();
  46  | 
  47  |     const regContext = await browser.newContext();
  48  |     await setSessionCookie(regContext, requireEnv('REGULAR_TOKEN'), webBase);
  49  |     const regPage = await regContext.newPage();
  50  |     await regPage.goto('/', { waitUntil: 'domcontentloaded' });
  51  |     await expect(regPage.locator(`a[href$="/event/${testEvent.id}"]`)).toHaveCount(0);
  52  | 
  53  |     await regContext.close();
  54  |   });
  55  | 
  56  |   test('Event detail — admin: banner, robots meta, player shell', async ({
  57  |     browser,
  58  |   }) => {
  59  |     const webBase = resolveWebBaseUrl();
  60  |     const ctx = await browser.newContext();
  61  |     await setSessionCookie(ctx, requireEnv('ADMIN_TOKEN'), webBase);
  62  |     const page = await ctx.newPage();
  63  | 
  64  |     await page.goto(`/event/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  65  | 
  66  |     await expect(
  67  |       page.getByRole('status').filter({ hasText: /test event/i }),
  68  |     ).toBeVisible();
  69  | 
  70  |     const robots = await page.locator('meta[name="robots"]').getAttribute('content');
  71  |     expect(robots ?? '').toMatch(/noindex/i);
  72  |     expect(robots ?? '').toMatch(/nofollow/i);
  73  | 
  74  |     const video = page.locator('video, [class*="video-js"]').first();
  75  |     const subscriptionGate = page.getByRole('heading', {
  76  |       name: /Watch with Subscription/i,
  77  |     });
  78  |     const scheduledGate = page.getByRole('heading', {
  79  |       name: /Upcoming Event|Event Delayed/i,
  80  |     });
  81  |     await expect(video.or(subscriptionGate).or(scheduledGate).first()).toBeVisible({
  82  |       timeout: 60_000,
  83  |     });
  84  | 
  85  |     await ctx.close();
  86  |   });
  87  | 
  88  |   test('Event detail — regular: test event URL shows 404 page', async ({
  89  |     browser,
  90  |   }) => {
  91  |     const webBase = resolveWebBaseUrl();
  92  |     const ctx = await browser.newContext();
  93  |     await setSessionCookie(ctx, requireEnv('REGULAR_TOKEN'), webBase);
  94  |     const page = await ctx.newPage();
  95  | 
  96  |     await page.goto(`/event/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  97  |     await expect(
  98  |       page.getByRole('heading', { name: /Page Not Found/i }),
  99  |     ).toBeVisible();
  100 | 
  101 |     await ctx.close();
  102 |   });
  103 | 
  104 |   test('Direct access — /event/:testId and /stream/:testId as regular → 404', async ({
  105 |     browser,
  106 |   }) => {
  107 |     const webBase = resolveWebBaseUrl();
  108 |     const ctx = await browser.newContext();
  109 |     await setSessionCookie(ctx, requireEnv('REGULAR_TOKEN'), webBase);
  110 |     const page = await ctx.newPage();
  111 | 
  112 |     await page.goto(`/event/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  113 |     await expect(
  114 |       page.getByRole('heading', { name: /Page Not Found/i }),
  115 |     ).toBeVisible();
  116 | 
  117 |     await page.goto(`/stream/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  118 |     await expect(
  119 |       page.getByRole('heading', { name: /Page Not Found/i }),
  120 |     ).toBeVisible();
  121 | 
  122 |     await ctx.close();
  123 |   });
  124 | });
  125 | 
```