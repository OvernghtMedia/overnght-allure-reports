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

Locator: locator('a[href$="/event/484475e4-6919-4dd9-86f4-0061e3b9ecc6"]').first().locator('[class*="ring-red-500"]').first()
Expected: visible
Timeout: 25000ms
Error: element(s) not found

Call log:
  - Expect "toBeVisible" with timeout 25000ms
  - waiting for locator('a[href$="/event/484475e4-6919-4dd9-86f4-0061e3b9ecc6"]').first().locator('[class*="ring-red-500"]').first()

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
            - img [ref=e34]
            - img [ref=e37]
            - img "BLUE DIVISION | MISSION vs. NYAC" [ref=e40]
            - generic:
              - generic:
                - generic:
                  - generic:
                    - generic:
                      - generic: Men's Water Polo
                      - generic: ·
                      - generic: Feb 22 • 3:15 AM
                  - generic:
                    - generic:
                      - heading "BLUE DIVISION | MISSION vs. NYAC" [level=1]
                  - generic:
                    - button "Watch now" [ref=e41]:
                      - img
                      - text: Watch now
                    - button "Share" [ref=e42]:
                      - img
                      - text: Share
            - generic:
              - generic:
                - generic [ref=e43]:
                  - button "Go to slide 1" [ref=e44]
                  - button "Go to slide 2" [ref=e45]
                  - button "Go to slide 3" [ref=e46]
                - generic [ref=e49]:
                  - button "Previous slide" [ref=e50]:
                    - img [ref=e51]
                  - button "Next slide" [ref=e53]:
                    - img [ref=e54]
        - generic [ref=e56]:
          - generic [ref=e57]:
            - generic [ref=e59]:
              - heading "Live Now" [level=2] [ref=e62]
              - paragraph [ref=e63]: Join the action happening right now - don't miss a moment
            - 'link "Water Polo: test live 0515" [ref=e66] [cursor=pointer]':
              - /url: /event/f82d40aa-4527-4e5b-8df9-d906abeb4f84
              - generic [ref=e67]:
                - generic [ref=e69]:
                  - img "test live 0515" [ref=e71]
                  - generic [ref=e73]: CN
                  - generic [ref=e74]: VS
                - generic [ref=e76]: LIVE
                - generic:
                  - generic:
                    - img
              - generic [ref=e77]:
                - generic [ref=e78]: Water Polo
                - heading "test live 0515" [level=3] [ref=e79]
          - generic [ref=e80]:
            - generic [ref=e81]:
              - generic [ref=e82]:
                - heading "On the Horizon" [level=2] [ref=e84]
                - paragraph [ref=e85]: Exciting competitions and events coming your way - set your calendar
              - generic [ref=e86]:
                - link "See all" [ref=e87] [cursor=pointer]:
                  - /url: /schedule/search
                - generic [ref=e88]:
                  - button "Scroll left" [ref=e89] [cursor=pointer]:
                    - img [ref=e90]
                  - button "Scroll right" [disabled] [ref=e92]:
                    - img [ref=e93]
            - generic [ref=e95]:
              - 'link "Rowing: San Diego Crew Classic" [ref=e97] [cursor=pointer]':
                - /url: /event/88834c9e-1bb1-42d0-afc5-403026dfbbc7
                - generic [ref=e98]:
                  - img "San Diego Crew Classic" [ref=e100]
                  - generic [ref=e102]: DELAYED
                  - generic [ref=e104]:
                    - img [ref=e105]
                    - text: Mar 28 · 2:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e108]:
                  - generic [ref=e109]: Rowing
                  - heading "San Diego Crew Classic" [level=3] [ref=e110]
              - 'link "Water Polo: Live Test Event Delayed [STG]" [ref=e112] [cursor=pointer]':
                - /url: /event/6336b38e-7254-4c36-b8e2-c9629673cdd4
                - generic [ref=e113]:
                  - img "Live Test Event Delayed [STG]" [ref=e115]
                  - generic [ref=e117]: DELAYED
                  - generic [ref=e119]:
                    - img [ref=e120]
                    - text: Apr 29 · 12:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e123]:
                  - generic [ref=e124]: Water Polo
                  - heading "Live Test Event Delayed [STG]" [level=3] [ref=e125]
              - 'link "Women''s Water Polo: featured 1" [ref=e127] [cursor=pointer]':
                - /url: /event/c2454e40-5040-4f06-a0e7-d4dfa066e0e6
                - generic [ref=e128]:
                  - img "featured 1" [ref=e130]
                  - generic [ref=e132]: DELAYED
                  - generic [ref=e134]:
                    - img [ref=e135]
                    - text: Jun 1 · 3:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e138]:
                  - generic [ref=e139]: Women's Water Polo
                  - heading "featured 1" [level=3] [ref=e140]
              - 'link "Women''s Water Polo: featured 2" [ref=e142] [cursor=pointer]':
                - /url: /event/f7c30c7f-f495-4492-813d-ce4654a60ec5
                - generic [ref=e143]:
                  - img "featured 2" [ref=e145]
                  - generic [ref=e147]: DELAYED
                  - generic [ref=e149]:
                    - img [ref=e150]
                    - text: Jun 2 · 4:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e153]:
                  - generic [ref=e154]: Women's Water Polo
                  - heading "featured 2" [level=3] [ref=e155]
              - 'link "Women''s Water Polo: featured 3" [ref=e157] [cursor=pointer]':
                - /url: /event/8a8afe75-674c-4c35-9d3c-60c2a7dbc30d
                - generic [ref=e158]:
                  - img "featured 3" [ref=e160]
                  - generic [ref=e162]: DELAYED
                  - generic [ref=e164]:
                    - img [ref=e165]
                    - text: Jun 3 · 5:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e168]:
                  - generic [ref=e169]: Women's Water Polo
                  - heading "featured 3" [level=3] [ref=e170]
              - 'link "Men''s Rowing: test events" [ref=e172] [cursor=pointer]':
                - /url: /event/a9e0cedb-1bf6-4cff-91f3-e7b63ae530af
                - generic [ref=e173]:
                  - img "test events" [ref=e175]
                  - generic [ref=e177]: DELAYED
                  - generic [ref=e179]:
                    - img [ref=e180]
                    - text: Wed · 6:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e183]:
                  - generic [ref=e184]: Men's Rowing
                  - heading "test events" [level=3] [ref=e185]
              - 'link "Water Polo: event 2" [ref=e187] [cursor=pointer]':
                - /url: /event/5f0bef70-09f8-4400-9d16-8d9b22066701
                - generic [ref=e188]:
                  - img "event 2" [ref=e190]
                  - generic [ref=e192]: DELAYED
                  - generic [ref=e194]:
                    - img [ref=e195]
                    - text: Thu · 7:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e198]:
                  - generic [ref=e199]: Water Polo
                  - heading "event 2" [level=3] [ref=e200]
              - 'link "Women''s Water Polo: event 3" [ref=e202] [cursor=pointer]':
                - /url: /event/0ccbc356-3ea4-48b1-a4bc-cc0245cca381
                - generic [ref=e203]:
                  - generic [ref=e205]:
                    - img "event 3" [ref=e207]
                    - img "event 3" [ref=e209]
                    - generic [ref=e210]: VS
                  - generic [ref=e212]: DELAYED
                  - generic [ref=e214]:
                    - img [ref=e215]
                    - text: Sat · 5:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e218]:
                  - generic [ref=e219]: Women's Water Polo
                  - heading "event 3" [level=3] [ref=e220]
              - 'link "Omega Ball: www" [ref=e222] [cursor=pointer]':
                - /url: /event/484475e4-6919-4dd9-86f4-0061e3b9ecc6
                - generic [ref=e223]:
                  - img "www" [ref=e225]
                  - generic [ref=e227]:
                    - img [ref=e228]
                    - text: Jul 12 · 2:00 PM
                  - generic:
                    - generic:
                      - img
                - generic [ref=e231]:
                  - generic [ref=e232]: Omega Ball
                  - heading "www" [level=3] [ref=e233]
          - generic [ref=e234]:
            - generic [ref=e236]:
              - heading "Popular Sports" [level=2] [ref=e238]
              - paragraph [ref=e239]: Explore world-class events and competitions across different sporting disciplines
            - generic [ref=e240]:
              - link "Water Polo" [ref=e241] [cursor=pointer]:
                - /url: /sports/water-polo
                - img [ref=e244]
                - heading "Water Polo" [level=3] [ref=e248]
              - link "Rowing" [ref=e249] [cursor=pointer]:
                - /url: /sports/rowing
                - img [ref=e252]
                - heading "Rowing" [level=3] [ref=e256]
              - link "Football" [ref=e257] [cursor=pointer]:
                - /url: /sports/football
                - img [ref=e260]
                - heading "Football" [level=3] [ref=e264]
          - generic [ref=e265]:
            - generic [ref=e267]:
              - heading "Conferences" [level=2] [ref=e269]
              - paragraph [ref=e270]: Explore sports conferences and leagues
            - generic [ref=e271]:
              - link "European Aquatics Water Polo" [ref=e272] [cursor=pointer]:
                - /url: /conferences/european-aquatics-water-polo
                - img "European Aquatics Water Polo" [ref=e275]
                - heading "European Aquatics Water Polo" [level=3] [ref=e276]
              - link "USAWP" [ref=e277] [cursor=pointer]:
                - /url: /conferences/usawp
                - img "USAWP" [ref=e280]
                - heading "USAWP" [level=3] [ref=e281]
              - link "USRowing" [ref=e282] [cursor=pointer]:
                - /url: /conferences/usrowing
                - img "USRowing" [ref=e285]
                - heading "USRowing" [level=3] [ref=e286]
          - generic [ref=e287]:
            - generic [ref=e288]:
              - generic [ref=e289]:
                - heading "Featured Past Events" [level=2] [ref=e291]
                - paragraph [ref=e292]: The main competition you can't miss
              - generic [ref=e293]:
                - link "See all" [ref=e294] [cursor=pointer]:
                  - /url: /search?featured=1
                - generic [ref=e295]:
                  - button "Scroll left" [disabled] [ref=e296]:
                    - img [ref=e297]
                  - button "Scroll right" [ref=e299] [cursor=pointer]:
                    - img [ref=e300]
            - generic [ref=e302]:
              - 'link "Men''s Water Polo: Super Cup 2025 - Pro Recco vs. FTC" [ref=e304] [cursor=pointer]':
                - /url: /event/1cf33c12-e9e0-4652-a835-c29574f0fc03
                - generic [ref=e305]:
                  - img "Super Cup 2025 - Pro Recco vs. FTC" [ref=e307]
                  - generic [ref=e309]:
                    - img [ref=e310]
                    - text: Oct 8, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e313]:
                  - generic [ref=e314]: Men's Water Polo
                  - heading "Super Cup 2025 - Pro Recco vs. FTC" [level=3] [ref=e315]
              - 'link "Men''s Water Polo: Princeton vs. FTC Telekom" [ref=e317] [cursor=pointer]':
                - /url: /event/3b1b3223-425c-4845-81a9-a086fe1a8e3a
                - generic [ref=e318]:
                  - img "Princeton vs. FTC Telekom" [ref=e320]
                  - generic [ref=e322]:
                    - img [ref=e323]
                    - text: Sep 3, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e326]:
                  - generic [ref=e327]: Men's Water Polo
                  - heading "Princeton vs. FTC Telekom" [level=3] [ref=e328]
              - 'link "Men''s Water Polo: Pro Recco vs. UCLA" [ref=e330] [cursor=pointer]':
                - /url: /event/c5da92ff-029c-4254-96cc-a9c538074b60
                - generic [ref=e331]:
                  - img "Pro Recco vs. UCLA" [ref=e333]
                  - generic [ref=e335]:
                    - img [ref=e336]
                    - text: Sep 3, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e339]:
                  - generic [ref=e340]: Men's Water Polo
                  - heading "Pro Recco vs. UCLA" [level=3] [ref=e341]
              - 'link "Rowing: 2025 Day 1: USRowing RowFest National Championships" [ref=e343] [cursor=pointer]':
                - /url: /event/ec27439e-c22b-4079-ab8e-3aa0d9f76f16
                - generic [ref=e344]:
                  - 'img "2025 Day 1: USRowing RowFest National Championships" [ref=e346]'
                  - generic [ref=e348]:
                    - img [ref=e349]
                    - text: Jul 12, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e352]:
                  - generic [ref=e353]: Rowing
                  - 'heading "2025 Day 1: USRowing RowFest National Championships" [level=3] [ref=e354]'
              - 'link "Rowing: Day 2: 2025 USRowing Youth National Championships" [ref=e356] [cursor=pointer]':
                - /url: /event/68f89bac-bb5a-4d03-a390-070137b179b3
                - generic [ref=e357]:
                  - 'img "Day 2: 2025 USRowing Youth National Championships" [ref=e359]'
                  - generic [ref=e361]:
                    - img [ref=e362]
                    - text: Jun 13, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e365]:
                  - generic [ref=e366]: Rowing
                  - 'heading "Day 2: 2025 USRowing Youth National Championships" [level=3] [ref=e367]'
              - 'link "Rowing: Day 1: 2025 USRowing Youth National Championships" [ref=e369] [cursor=pointer]':
                - /url: /event/a398171a-d01f-4b99-8cdf-e3c7738f1f07
                - generic [ref=e370]:
                  - 'img "Day 1: 2025 USRowing Youth National Championships" [ref=e372]'
                  - generic [ref=e374]:
                    - img [ref=e375]
                    - text: Jun 12, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e378]:
                  - generic [ref=e379]: Rowing
                  - 'heading "Day 1: 2025 USRowing Youth National Championships" [level=3] [ref=e380]'
          - generic [ref=e381]:
            - generic [ref=e382]:
              - generic [ref=e383]:
                - heading "Featured Overnght Shows" [level=2] [ref=e385]
                - paragraph [ref=e386]: Unique sports talk and behind-the-scenes shows, only here
              - link "See all" [ref=e388] [cursor=pointer]:
                - /url: /search?show=1&featured=1
            - generic [ref=e389]:
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e391] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5
                - article [ref=e392]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e395]
                  - generic [ref=e396]:
                    - generic [ref=e397]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e398]
                    - generic [ref=e399]: Rowing
                    - generic [ref=e400]:
                      - img [ref=e401]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e404] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980
                - article [ref=e405]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e408]
                  - generic [ref=e409]:
                    - generic [ref=e410]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e411]
                    - generic [ref=e412]: Rowing
                    - generic [ref=e413]:
                      - img [ref=e414]
                      - text: Watch Now
          - generic [ref=e416]:
            - generic [ref=e417]:
              - generic [ref=e418]:
                - heading "All Overnght Shows" [level=2] [ref=e420]
                - paragraph [ref=e421]: Late-night sports content and exclusive shows
              - generic [ref=e422]:
                - link "See all" [ref=e423] [cursor=pointer]:
                  - /url: /search?show=1
                - generic [ref=e424]:
                  - button "Scroll left" [disabled] [ref=e425]:
                    - img [ref=e426]
                  - button "Scroll right" [ref=e428] [cursor=pointer]:
                    - img [ref=e429]
            - generic [ref=e431]:
              - link "The Counter Attack ON Overnght Ep 41 | March 4, 2026 — show" [ref=e433] [cursor=pointer]:
                - /url: /event/4ad7c642-76de-4694-a9ed-052243bb959c
                - article [ref=e434]:
                  - img "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [ref=e437]
                  - generic [ref=e438]:
                    - generic [ref=e439]: Mar 5 · 6:15 PM
                    - heading "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [level=3] [ref=e440]
                    - generic [ref=e441]: Water Polo
                    - generic [ref=e442]:
                      - img [ref=e443]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 25, 2026 — show" [ref=e446] [cursor=pointer]:
                - /url: /event/5c84a6fd-6320-4b8d-b159-2c58f8908b15
                - article [ref=e447]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [ref=e450]
                  - generic [ref=e451]:
                    - generic [ref=e452]: Mar 2 · 7:15 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [level=3] [ref=e453]
                    - generic [ref=e454]: Water Polo
                    - generic [ref=e455]:
                      - img [ref=e456]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 26, 2026 — show" [ref=e459] [cursor=pointer]:
                - /url: /event/1635113c-beee-489c-b512-5153efb101e1
                - article [ref=e460]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [ref=e463]
                  - generic [ref=e464]:
                    - generic [ref=e465]: Feb 26 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [level=3] [ref=e466]
                    - generic [ref=e467]: Water Polo
                    - generic [ref=e468]:
                      - img [ref=e469]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.4 — show" [ref=e472] [cursor=pointer]:
                - /url: /event/c4a63e93-2463-42da-8405-c439d7560aa1
                - article [ref=e473]:
                  - img "Rowing Wolf Podcast, Ep1.4" [ref=e476]
                  - generic [ref=e477]:
                    - generic [ref=e478]: Feb 24 · 10:05 PM
                    - heading "Rowing Wolf Podcast, Ep1.4" [level=3] [ref=e479]
                    - generic [ref=e480]: Rowing
                    - generic [ref=e481]:
                      - img [ref=e482]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 39 | February 18, 2026 — show" [ref=e485] [cursor=pointer]:
                - /url: /event/bca89acc-e481-4d23-8e93-df683231f507
                - article [ref=e486]:
                  - img "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [ref=e489]
                  - generic [ref=e490]:
                    - generic [ref=e491]: Feb 20 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [level=3] [ref=e492]
                    - generic [ref=e493]: Water Polo
                    - generic [ref=e494]:
                      - img [ref=e495]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e498] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5
                - article [ref=e499]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e502]
                  - generic [ref=e503]:
                    - generic [ref=e504]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e505]
                    - generic [ref=e506]: Rowing
                    - generic [ref=e507]:
                      - img [ref=e508]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e511] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980
                - article [ref=e512]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e515]
                  - generic [ref=e516]:
                    - generic [ref=e517]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e518]
                    - generic [ref=e519]: Rowing
                    - generic [ref=e520]:
                      - img [ref=e521]
                      - text: Watch Now
              - link "2025 Cutino Awards — show" [ref=e524] [cursor=pointer]:
                - /url: /event/6f99d5e7-fb65-429d-9024-fef463d2f2d4
                - article [ref=e525]:
                  - img "2025 Cutino Awards" [ref=e528]
                  - generic [ref=e529]:
                    - generic [ref=e530]: Jun 8, 2025 · 1:45 AM
                    - heading "2025 Cutino Awards" [level=3] [ref=e531]
                    - generic [ref=e532]: Water Polo
                    - generic [ref=e533]:
                      - img [ref=e534]
                      - text: Watch Now
              - link "JRN IRA National Championship Day Three Review — show" [ref=e537] [cursor=pointer]:
                - /url: /event/1ae42c95-a95b-4e4a-a9cc-99615adc4d67
                - article [ref=e538]:
                  - img "JRN IRA National Championship Day Three Review" [ref=e541]
                  - generic [ref=e542]:
                    - generic [ref=e543]: Jun 1, 2025 · 9:40 PM
                    - heading "JRN IRA National Championship Day Three Review" [level=3] [ref=e544]
                    - generic [ref=e545]: Rowing
                    - generic [ref=e546]:
                      - img [ref=e547]
                      - text: Watch Now
          - generic [ref=e549]:
            - generic [ref=e550]:
              - generic [ref=e551]:
                - heading "All Past Events" [level=2] [ref=e553]
                - paragraph [ref=e554]: Browse every event in one place
              - generic [ref=e555]:
                - link "See all" [ref=e556] [cursor=pointer]:
                  - /url: /search
                - generic [ref=e557]:
                  - button "Scroll left" [ref=e558] [cursor=pointer]:
                    - img [ref=e559]
                  - button "Scroll right" [ref=e561] [cursor=pointer]:
                    - img [ref=e562]
            - generic [ref=e564]:
              - 'link "Water Polo: VOD Test Event Scheduled [STG]" [ref=e566] [cursor=pointer]':
                - /url: /event/27963fc8-f89c-4fed-a2a5-84c6d20060a7
                - generic [ref=e567]:
                  - img "VOD Test Event Scheduled [STG]" [ref=e569]
                  - generic [ref=e571]:
                    - img [ref=e572]
                    - text: May 28
                  - generic:
                    - generic:
                      - img
                - generic [ref=e575]:
                  - generic [ref=e576]: Water Polo
                  - heading "VOD Test Event Scheduled [STG]" [level=3] [ref=e577]
              - 'link "Water Polo: Live test event 0512" [ref=e579] [cursor=pointer]':
                - /url: /event/27aac4b3-ccca-478e-b178-e76424220b40
                - generic [ref=e580]:
                  - img "Live test event 0512" [ref=e582]
                  - generic [ref=e584]:
                    - img [ref=e585]
                    - text: May 12
                  - generic:
                    - generic:
                      - img
                - generic [ref=e588]:
                  - generic [ref=e589]: Water Polo
                  - heading "Live test event 0512" [level=3] [ref=e590]
              - 'link "Water Polo: Live Event for Autotests" [ref=e592] [cursor=pointer]':
                - /url: /event/7dfe92c5-6773-4025-980f-3924167d6114
                - generic [ref=e593]:
                  - generic [ref=e595]:
                    - img "Live Event for Autotests" [ref=e597]
                    - img "Live Event for Autotests" [ref=e599]
                    - generic [ref=e600]: VS
                  - generic [ref=e602]:
                    - img [ref=e603]
                    - text: May 11
                  - generic:
                    - generic:
                      - img
                - generic [ref=e606]:
                  - generic [ref=e607]: Water Polo
                  - heading "Live Event for Autotests" [level=3] [ref=e608]
              - 'link "Water Polo: Test Event VOD [STG]" [ref=e610] [cursor=pointer]':
                - /url: /event/94655734-5203-40b3-9cc4-62892d56c829
                - generic [ref=e611]:
                  - img "Test Event VOD [STG]" [ref=e613]
                  - generic [ref=e615]:
                    - img [ref=e616]
                    - text: Apr 28
                  - generic:
                    - generic:
                      - img
                - generic [ref=e619]:
                  - generic [ref=e620]: Water Polo
                  - heading "Test Event VOD [STG]" [level=3] [ref=e621]
              - 'link "Water Polo: Event B" [ref=e623] [cursor=pointer]':
                - /url: /event/3b4001ce-9481-4f9d-871e-367c8b47d5a7
                - generic [ref=e624]:
                  - img "Event B" [ref=e626]
                  - generic [ref=e628]:
                    - img [ref=e629]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e632]:
                  - generic [ref=e633]: Water Polo
                  - heading "Event B" [level=3] [ref=e634]
              - 'link "Water Polo: Event A" [ref=e636] [cursor=pointer]':
                - /url: /event/d1ea6b2b-f306-4ee2-b893-5b0fe4199522
                - generic [ref=e637]:
                  - img "Event A" [ref=e639]
                  - generic [ref=e641]:
                    - img [ref=e642]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e645]:
                  - generic [ref=e646]: Water Polo
                  - heading "Event A" [level=3] [ref=e647]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [ref=e649] [cursor=pointer]':
                - /url: /event/b2e3f38e-d1e3-45be-a8a3-300b54cdb1a3
                - generic [ref=e650]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [ref=e652]
                  - generic [ref=e654]:
                    - img [ref=e655]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e658]:
                  - generic [ref=e659]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [level=3] [ref=e660]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [ref=e662] [cursor=pointer]':
                - /url: /event/848e2337-26b6-4a7b-ae72-e69cc536c49c
                - generic [ref=e663]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [ref=e665]
                  - generic [ref=e667]:
                    - img [ref=e668]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e671]:
                  - generic [ref=e672]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [level=3] [ref=e673]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [ref=e675] [cursor=pointer]':
                - /url: /event/587976e0-d3e1-4637-9734-4fa364af86dc
                - generic [ref=e676]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [ref=e678]
                  - generic [ref=e680]:
                    - img [ref=e681]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e684]:
                  - generic [ref=e685]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [level=3] [ref=e686]
        - generic [ref=e689]:
          - generic [ref=e690]:
            - generic [ref=e691]: Help center
            - heading "Questions? Answered." [level=2] [ref=e693]:
              - text: Questions?
              - text: Answered.
            - paragraph [ref=e694]: The essentials about watching, replays and your membership — in one tap.
            - generic [ref=e695]:
              - heading "Still need a hand?" [level=3] [ref=e697]
              - paragraph [ref=e698]: Support is on the clock worldwide, every matchday.
              - link "Email" [ref=e700] [cursor=pointer]:
                - /url: /contact
                - img
                - generic [ref=e701]: Email
          - generic [ref=e703]:
            - generic [ref=e704]:
              - generic [ref=e705]:
                - button "01 How many devices can I use with my subscription?" [expanded] [ref=e706] [cursor=pointer]:
                  - generic [ref=e707]: "01"
                  - generic [ref=e708]: How many devices can I use with my subscription?
                  - img [ref=e710]
                - paragraph [ref=e715]: Up to 2
              - generic [ref=e716]:
                - button "02 I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?" [ref=e717] [cursor=pointer]:
                  - generic [ref=e718]: "02"
                  - generic [ref=e719]: I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?
                  - img [ref=e721]
                - generic [ref=e723]:
                  - paragraph [ref=e724]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e725]:
                    - listitem [ref=e726]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e727]: Check your internet connection.
                    - listitem [ref=e728]:
                      - text: You can click
                      - link "[this link]" [ref=e729] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                  - paragraph [ref=e730]
                  - paragraph [ref=e731]
              - generic [ref=e732]:
                - button "03 How do I cancel my subscription?" [ref=e733] [cursor=pointer]:
                  - generic [ref=e734]: "03"
                  - generic [ref=e735]: How do I cancel my subscription?
                  - img [ref=e737]
                - list [ref=e740]:
                  - listitem [ref=e741]: Click on My account on the header
                  - listitem [ref=e742]: Select my account
                  - listitem [ref=e743]: Click on cancel subscription
              - generic [ref=e744]:
                - button "04 Why am I still being charged after canceling my subscription?" [ref=e745] [cursor=pointer]:
                  - generic [ref=e746]: "04"
                  - generic [ref=e747]: Why am I still being charged after canceling my subscription?
                  - img [ref=e749]
                - list [ref=e752]:
                  - listitem [ref=e753]: If you are being charged, please check your subscription status and click cancel. Cancel subscription is best done on Chrome of Safari web browser on your mobile, tablet or desktop.
                  - listitem [ref=e754]: You cannot cancel subscription via mobile app at this time.
              - generic [ref=e755]:
                - button "05 I was unable to watch a live event due to a website or technology problem. Can I get a refund?" [ref=e756] [cursor=pointer]:
                  - generic [ref=e757]: "05"
                  - generic [ref=e758]: I was unable to watch a live event due to a website or technology problem. Can I get a refund?
                  - img [ref=e760]
                - generic [ref=e762]:
                  - paragraph [ref=e763]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e764]:
                    - listitem [ref=e765]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e766]: Check your internet connection.
                    - listitem [ref=e767]:
                      - text: You can click
                      - link "[this link]" [ref=e768] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                    - listitem [ref=e769]:
                      - text: If the problem persists, please contact us via email at
                      - strong [ref=e770]:
                        - link "support@overnght.com" [ref=e771] [cursor=pointer]:
                          - /url: mailto:support@overnght.com
                      - text: .
                  - paragraph [ref=e772]
            - link "See all FAQs" [ref=e773] [cursor=pointer]:
              - /url: /faq
              - text: See all FAQs
              - img [ref=e774]
        - generic [ref=e777]:
          - generic [ref=e778]:
            - generic [ref=e779]:
              - generic [ref=e780]:
                - link "Overnght — Home" [ref=e781] [cursor=pointer]:
                  - /url: /
                  - img [ref=e782]
                - paragraph [ref=e785]: Live sports and exclusive content. Watch live or on demand, in HD.
              - generic [ref=e786]:
                - link "Download Overnght on the App Store" [ref=e787] [cursor=pointer]:
                  - /url: https://apps.apple.com/us/app/overnght/id6476713008
                  - img [ref=e788]
                  - generic [ref=e790]:
                    - generic [ref=e791]: Download on the
                    - generic [ref=e792]: App Store
                - link "Get Overnght on Google Play" [ref=e793] [cursor=pointer]:
                  - /url: https://play.google.com/store/apps/details?id=com.overnght.app
                  - img [ref=e794]
                  - generic [ref=e796]:
                    - generic [ref=e797]: Get it on
                    - generic [ref=e798]: Google Play
            - navigation "Footer" [ref=e799]:
              - generic [ref=e800]:
                - heading "Watch" [level=3] [ref=e801]
                - list [ref=e802]:
                  - listitem [ref=e803]:
                    - link "Home" [ref=e804] [cursor=pointer]:
                      - /url: /
                  - listitem [ref=e805]:
                    - link "Schedule" [ref=e806] [cursor=pointer]:
                      - /url: /schedule
                  - listitem [ref=e807]:
                    - link "On Demand" [ref=e808] [cursor=pointer]:
                      - /url: /search
              - generic [ref=e809]:
                - heading "Account" [level=3] [ref=e810]
                - list [ref=e811]:
                  - listitem [ref=e812]:
                    - link "My account" [ref=e813] [cursor=pointer]:
                      - /url: /account
                  - listitem [ref=e814]:
                    - link "Subscription" [ref=e815] [cursor=pointer]:
                      - /url: /subscription
              - generic [ref=e816]:
                - heading "Support" [level=3] [ref=e817]
                - list [ref=e818]:
                  - listitem [ref=e819]:
                    - link "FAQ" [ref=e820] [cursor=pointer]:
                      - /url: /faq
                  - listitem [ref=e821]:
                    - link "Contact" [ref=e822] [cursor=pointer]:
                      - /url: /contact
          - generic [ref=e823]:
            - paragraph [ref=e824]: © Overnght 2026
            - navigation "Legal" [ref=e825]:
              - link "Privacy Policy" [ref=e826] [cursor=pointer]:
                - /url: /legalese/termsOfService#privacy-policy
              - link "Terms of Use" [ref=e827] [cursor=pointer]:
                - /url: /legalese/termsOfService
  - alert [ref=e828]
  - generic [ref=e833]:
    - generic [ref=e834]:
      - img [ref=e836]
      - paragraph [ref=e838]:
        - text: We use cookies to improve your experience and analyze platform usage.
        - link "Privacy Policy" [ref=e839] [cursor=pointer]:
          - /url: /legalese/termsOfService#privacy-policy
    - generic [ref=e840]:
      - button "Decline" [ref=e841]
      - button "Accept Cookies" [ref=e842]
  - region "Notifications Alt+T"
  - generic:
    - list [ref=e843]:
      - img [ref=e845] [cursor=pointer]
      - listitem [ref=e847]:
        - 'generic "Chatbot wrote: Ask us" [ref=e848] [cursor=pointer]': Ask us
    - button "Button to initiate Chatbot Dialogue" [ref=e849] [cursor=pointer]:
      - img "Open or close chat" [ref=e850]
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
  37  |     await expect(testCard).toBeVisible();
  38  |     await expect(
  39  |       testCard.locator('[class*="ring-red-500"]').first(),
> 40  |     ).toBeVisible();
      |       ^ Error: expect(locator).toBeVisible() failed
  41  | 
  42  |     await adminContext.close();
  43  | 
  44  |     const regContext = await browser.newContext();
  45  |     await setSessionCookie(regContext, requireEnv('REGULAR_TOKEN'), webBase);
  46  |     const regPage = await regContext.newPage();
  47  |     await regPage.goto('/', { waitUntil: 'domcontentloaded' });
  48  |     await expect(regPage.locator(`a[href$="/event/${testEvent.id}"]`)).toHaveCount(0);
  49  | 
  50  |     await regContext.close();
  51  |   });
  52  | 
  53  |   test('Event detail — admin: banner, robots meta, player shell', async ({
  54  |     browser,
  55  |   }) => {
  56  |     const webBase = resolveWebBaseUrl();
  57  |     const ctx = await browser.newContext();
  58  |     await setSessionCookie(ctx, requireEnv('ADMIN_TOKEN'), webBase);
  59  |     const page = await ctx.newPage();
  60  | 
  61  |     await page.goto(`/event/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  62  | 
  63  |     await expect(
  64  |       page.getByRole('status').filter({ hasText: /test event/i }),
  65  |     ).toBeVisible();
  66  | 
  67  |     const robots = await page.locator('meta[name="robots"]').getAttribute('content');
  68  |     expect(robots ?? '').toMatch(/noindex/i);
  69  |     expect(robots ?? '').toMatch(/nofollow/i);
  70  | 
  71  |     const video = page.locator('video, [class*="video-js"]').first();
  72  |     const subscriptionGate = page.getByRole('heading', {
  73  |       name: /Watch with Subscription/i,
  74  |     });
  75  |     const scheduledGate = page.getByRole('heading', {
  76  |       name: /Upcoming Event|Event Delayed/i,
  77  |     });
  78  |     await expect(video.or(subscriptionGate).or(scheduledGate).first()).toBeVisible({
  79  |       timeout: 60_000,
  80  |     });
  81  | 
  82  |     await ctx.close();
  83  |   });
  84  | 
  85  |   test('Event detail — regular: test event URL shows 404 page', async ({
  86  |     browser,
  87  |   }) => {
  88  |     const webBase = resolveWebBaseUrl();
  89  |     const ctx = await browser.newContext();
  90  |     await setSessionCookie(ctx, requireEnv('REGULAR_TOKEN'), webBase);
  91  |     const page = await ctx.newPage();
  92  | 
  93  |     await page.goto(`/event/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  94  |     await expect(
  95  |       page.getByRole('heading', { name: /Page Not Found/i }),
  96  |     ).toBeVisible();
  97  | 
  98  |     await ctx.close();
  99  |   });
  100 | 
  101 |   test('Direct access — /event/:testId and /stream/:testId as regular → 404', async ({
  102 |     browser,
  103 |   }) => {
  104 |     const webBase = resolveWebBaseUrl();
  105 |     const ctx = await browser.newContext();
  106 |     await setSessionCookie(ctx, requireEnv('REGULAR_TOKEN'), webBase);
  107 |     const page = await ctx.newPage();
  108 | 
  109 |     await page.goto(`/event/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  110 |     await expect(
  111 |       page.getByRole('heading', { name: /Page Not Found/i }),
  112 |     ).toBeVisible();
  113 | 
  114 |     await page.goto(`/stream/${testEvent.id}`, { waitUntil: 'domcontentloaded' });
  115 |     await expect(
  116 |       page.getByRole('heading', { name: /Page Not Found/i }),
  117 |     ).toBeVisible();
  118 | 
  119 |     await ctx.close();
  120 |   });
  121 | });
  122 | 
```