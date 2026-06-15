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
              - link "European Aquatics Water Polo European Aquatics Water Polo" [ref=e272] [cursor=pointer]:
                - /url: /conferences/european-aquatics-water-polo
                - generic [ref=e273]:
                  - img "European Aquatics Water Polo" [ref=e280]
                  - paragraph [ref=e284]: European Aquatics Water Polo
              - link "USAWP USAWP" [ref=e285] [cursor=pointer]:
                - /url: /conferences/usawp
                - generic [ref=e286]:
                  - img "USAWP" [ref=e293]
                  - paragraph [ref=e297]: USAWP
              - link "USRowing USRowing" [ref=e298] [cursor=pointer]:
                - /url: /conferences/usrowing
                - generic [ref=e299]:
                  - img "USRowing" [ref=e306]
                  - paragraph [ref=e310]: USRowing
          - generic [ref=e311]:
            - generic [ref=e312]:
              - generic [ref=e313]:
                - heading "Featured Past Events" [level=2] [ref=e315]
                - paragraph [ref=e316]: The main competition you can't miss
              - generic [ref=e317]:
                - link "See all" [ref=e318] [cursor=pointer]:
                  - /url: /search?featured=1
                - generic [ref=e319]:
                  - button "Scroll left" [disabled] [ref=e320]:
                    - img [ref=e321]
                  - button "Scroll right" [ref=e323] [cursor=pointer]:
                    - img [ref=e324]
            - generic [ref=e326]:
              - 'link "Men''s Water Polo: Super Cup 2025 - Pro Recco vs. FTC" [ref=e328] [cursor=pointer]':
                - /url: /event/1cf33c12-e9e0-4652-a835-c29574f0fc03
                - generic [ref=e329]:
                  - img "Super Cup 2025 - Pro Recco vs. FTC" [ref=e331]
                  - generic [ref=e333]:
                    - img [ref=e334]
                    - text: Oct 8, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e337]:
                  - generic [ref=e338]: Men's Water Polo
                  - heading "Super Cup 2025 - Pro Recco vs. FTC" [level=3] [ref=e339]
              - 'link "Men''s Water Polo: Princeton vs. FTC Telekom" [ref=e341] [cursor=pointer]':
                - /url: /event/3b1b3223-425c-4845-81a9-a086fe1a8e3a
                - generic [ref=e342]:
                  - img "Princeton vs. FTC Telekom" [ref=e344]
                  - generic [ref=e346]:
                    - img [ref=e347]
                    - text: Sep 3, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e350]:
                  - generic [ref=e351]: Men's Water Polo
                  - heading "Princeton vs. FTC Telekom" [level=3] [ref=e352]
              - 'link "Men''s Water Polo: Pro Recco vs. UCLA" [ref=e354] [cursor=pointer]':
                - /url: /event/c5da92ff-029c-4254-96cc-a9c538074b60
                - generic [ref=e355]:
                  - img "Pro Recco vs. UCLA" [ref=e357]
                  - generic [ref=e359]:
                    - img [ref=e360]
                    - text: Sep 3, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e363]:
                  - generic [ref=e364]: Men's Water Polo
                  - heading "Pro Recco vs. UCLA" [level=3] [ref=e365]
              - 'link "Rowing: 2025 Day 1: USRowing RowFest National Championships" [ref=e367] [cursor=pointer]':
                - /url: /event/ec27439e-c22b-4079-ab8e-3aa0d9f76f16
                - generic [ref=e368]:
                  - 'img "2025 Day 1: USRowing RowFest National Championships" [ref=e370]'
                  - generic [ref=e372]:
                    - img [ref=e373]
                    - text: Jul 12, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e376]:
                  - generic [ref=e377]: Rowing
                  - 'heading "2025 Day 1: USRowing RowFest National Championships" [level=3] [ref=e378]'
              - 'link "Rowing: Day 2: 2025 USRowing Youth National Championships" [ref=e380] [cursor=pointer]':
                - /url: /event/68f89bac-bb5a-4d03-a390-070137b179b3
                - generic [ref=e381]:
                  - 'img "Day 2: 2025 USRowing Youth National Championships" [ref=e383]'
                  - generic [ref=e385]:
                    - img [ref=e386]
                    - text: Jun 13, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e389]:
                  - generic [ref=e390]: Rowing
                  - 'heading "Day 2: 2025 USRowing Youth National Championships" [level=3] [ref=e391]'
              - 'link "Rowing: Day 1: 2025 USRowing Youth National Championships" [ref=e393] [cursor=pointer]':
                - /url: /event/a398171a-d01f-4b99-8cdf-e3c7738f1f07
                - generic [ref=e394]:
                  - 'img "Day 1: 2025 USRowing Youth National Championships" [ref=e396]'
                  - generic [ref=e398]:
                    - img [ref=e399]
                    - text: Jun 12, 2025
                  - generic:
                    - generic:
                      - img
                - generic [ref=e402]:
                  - generic [ref=e403]: Rowing
                  - 'heading "Day 1: 2025 USRowing Youth National Championships" [level=3] [ref=e404]'
          - generic [ref=e405]:
            - generic [ref=e406]:
              - generic [ref=e407]:
                - heading "Featured Overnght Shows" [level=2] [ref=e409]
                - paragraph [ref=e410]: Unique sports talk and behind-the-scenes shows, only here
              - link "See all" [ref=e412] [cursor=pointer]:
                - /url: /search?show=1&featured=1
            - generic [ref=e413]:
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e415] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5
                - article [ref=e416]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e419]
                  - generic [ref=e420]:
                    - generic [ref=e421]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e422]
                    - generic [ref=e423]: Rowing
                    - generic [ref=e424]:
                      - img [ref=e425]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e428] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980
                - article [ref=e429]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e432]
                  - generic [ref=e433]:
                    - generic [ref=e434]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e435]
                    - generic [ref=e436]: Rowing
                    - generic [ref=e437]:
                      - img [ref=e438]
                      - text: Watch Now
          - generic [ref=e440]:
            - generic [ref=e441]:
              - generic [ref=e442]:
                - heading "All Overnght Shows" [level=2] [ref=e444]
                - paragraph [ref=e445]: Late-night sports content and exclusive shows
              - generic [ref=e446]:
                - link "See all" [ref=e447] [cursor=pointer]:
                  - /url: /search?show=1
                - generic [ref=e448]:
                  - button "Scroll left" [disabled] [ref=e449]:
                    - img [ref=e450]
                  - button "Scroll right" [ref=e452] [cursor=pointer]:
                    - img [ref=e453]
            - generic [ref=e455]:
              - link "The Counter Attack ON Overnght Ep 41 | March 4, 2026 — show" [ref=e457] [cursor=pointer]:
                - /url: /event/4ad7c642-76de-4694-a9ed-052243bb959c
                - article [ref=e458]:
                  - img "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [ref=e461]
                  - generic [ref=e462]:
                    - generic [ref=e463]: Mar 5 · 6:15 PM
                    - heading "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [level=3] [ref=e464]
                    - generic [ref=e465]: Water Polo
                    - generic [ref=e466]:
                      - img [ref=e467]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 25, 2026 — show" [ref=e470] [cursor=pointer]:
                - /url: /event/5c84a6fd-6320-4b8d-b159-2c58f8908b15
                - article [ref=e471]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [ref=e474]
                  - generic [ref=e475]:
                    - generic [ref=e476]: Mar 2 · 7:15 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [level=3] [ref=e477]
                    - generic [ref=e478]: Water Polo
                    - generic [ref=e479]:
                      - img [ref=e480]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 26, 2026 — show" [ref=e483] [cursor=pointer]:
                - /url: /event/1635113c-beee-489c-b512-5153efb101e1
                - article [ref=e484]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [ref=e487]
                  - generic [ref=e488]:
                    - generic [ref=e489]: Feb 26 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [level=3] [ref=e490]
                    - generic [ref=e491]: Water Polo
                    - generic [ref=e492]:
                      - img [ref=e493]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.4 — show" [ref=e496] [cursor=pointer]:
                - /url: /event/c4a63e93-2463-42da-8405-c439d7560aa1
                - article [ref=e497]:
                  - img "Rowing Wolf Podcast, Ep1.4" [ref=e500]
                  - generic [ref=e501]:
                    - generic [ref=e502]: Feb 24 · 10:05 PM
                    - heading "Rowing Wolf Podcast, Ep1.4" [level=3] [ref=e503]
                    - generic [ref=e504]: Rowing
                    - generic [ref=e505]:
                      - img [ref=e506]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 39 | February 18, 2026 — show" [ref=e509] [cursor=pointer]:
                - /url: /event/bca89acc-e481-4d23-8e93-df683231f507
                - article [ref=e510]:
                  - img "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [ref=e513]
                  - generic [ref=e514]:
                    - generic [ref=e515]: Feb 20 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [level=3] [ref=e516]
                    - generic [ref=e517]: Water Polo
                    - generic [ref=e518]:
                      - img [ref=e519]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e522] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5
                - article [ref=e523]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e526]
                  - generic [ref=e527]:
                    - generic [ref=e528]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e529]
                    - generic [ref=e530]: Rowing
                    - generic [ref=e531]:
                      - img [ref=e532]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e535] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980
                - article [ref=e536]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e539]
                  - generic [ref=e540]:
                    - generic [ref=e541]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e542]
                    - generic [ref=e543]: Rowing
                    - generic [ref=e544]:
                      - img [ref=e545]
                      - text: Watch Now
              - link "2025 Cutino Awards — show" [ref=e548] [cursor=pointer]:
                - /url: /event/6f99d5e7-fb65-429d-9024-fef463d2f2d4
                - article [ref=e549]:
                  - img "2025 Cutino Awards" [ref=e552]
                  - generic [ref=e553]:
                    - generic [ref=e554]: Jun 8, 2025 · 1:45 AM
                    - heading "2025 Cutino Awards" [level=3] [ref=e555]
                    - generic [ref=e556]: Water Polo
                    - generic [ref=e557]:
                      - img [ref=e558]
                      - text: Watch Now
              - link "JRN IRA National Championship Day Three Review — show" [ref=e561] [cursor=pointer]:
                - /url: /event/1ae42c95-a95b-4e4a-a9cc-99615adc4d67
                - article [ref=e562]:
                  - img "JRN IRA National Championship Day Three Review" [ref=e565]
                  - generic [ref=e566]:
                    - generic [ref=e567]: Jun 1, 2025 · 9:40 PM
                    - heading "JRN IRA National Championship Day Three Review" [level=3] [ref=e568]
                    - generic [ref=e569]: Rowing
                    - generic [ref=e570]:
                      - img [ref=e571]
                      - text: Watch Now
          - generic [ref=e573]:
            - generic [ref=e574]:
              - generic [ref=e575]:
                - heading "All Past Events" [level=2] [ref=e577]
                - paragraph [ref=e578]: Browse every event in one place
              - generic [ref=e579]:
                - link "See all" [ref=e580] [cursor=pointer]:
                  - /url: /search
                - generic [ref=e581]:
                  - button "Scroll left" [ref=e582] [cursor=pointer]:
                    - img [ref=e583]
                  - button "Scroll right" [ref=e585] [cursor=pointer]:
                    - img [ref=e586]
            - generic [ref=e588]:
              - 'link "Water Polo: VOD Test Event Scheduled [STG]" [ref=e590] [cursor=pointer]':
                - /url: /event/27963fc8-f89c-4fed-a2a5-84c6d20060a7
                - generic [ref=e591]:
                  - img "VOD Test Event Scheduled [STG]" [ref=e593]
                  - generic [ref=e595]:
                    - img [ref=e596]
                    - text: May 28
                  - generic:
                    - generic:
                      - img
                - generic [ref=e599]:
                  - generic [ref=e600]: Water Polo
                  - heading "VOD Test Event Scheduled [STG]" [level=3] [ref=e601]
              - 'link "Water Polo: Live test event 0512" [ref=e603] [cursor=pointer]':
                - /url: /event/27aac4b3-ccca-478e-b178-e76424220b40
                - generic [ref=e604]:
                  - img "Live test event 0512" [ref=e606]
                  - generic [ref=e608]:
                    - img [ref=e609]
                    - text: May 12
                  - generic:
                    - generic:
                      - img
                - generic [ref=e612]:
                  - generic [ref=e613]: Water Polo
                  - heading "Live test event 0512" [level=3] [ref=e614]
              - 'link "Water Polo: Live Event for Autotests" [ref=e616] [cursor=pointer]':
                - /url: /event/7dfe92c5-6773-4025-980f-3924167d6114
                - generic [ref=e617]:
                  - generic [ref=e619]:
                    - img "Live Event for Autotests" [ref=e621]
                    - img "Live Event for Autotests" [ref=e623]
                    - generic [ref=e624]: VS
                  - generic [ref=e626]:
                    - img [ref=e627]
                    - text: May 11
                  - generic:
                    - generic:
                      - img
                - generic [ref=e630]:
                  - generic [ref=e631]: Water Polo
                  - heading "Live Event for Autotests" [level=3] [ref=e632]
              - 'link "Water Polo: Test Event VOD [STG]" [ref=e634] [cursor=pointer]':
                - /url: /event/94655734-5203-40b3-9cc4-62892d56c829
                - generic [ref=e635]:
                  - img "Test Event VOD [STG]" [ref=e637]
                  - generic [ref=e639]:
                    - img [ref=e640]
                    - text: Apr 28
                  - generic:
                    - generic:
                      - img
                - generic [ref=e643]:
                  - generic [ref=e644]: Water Polo
                  - heading "Test Event VOD [STG]" [level=3] [ref=e645]
              - 'link "Water Polo: Event B" [ref=e647] [cursor=pointer]':
                - /url: /event/3b4001ce-9481-4f9d-871e-367c8b47d5a7
                - generic [ref=e648]:
                  - img "Event B" [ref=e650]
                  - generic [ref=e652]:
                    - img [ref=e653]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e656]:
                  - generic [ref=e657]: Water Polo
                  - heading "Event B" [level=3] [ref=e658]
              - 'link "Water Polo: Event A" [ref=e660] [cursor=pointer]':
                - /url: /event/d1ea6b2b-f306-4ee2-b893-5b0fe4199522
                - generic [ref=e661]:
                  - img "Event A" [ref=e663]
                  - generic [ref=e665]:
                    - img [ref=e666]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e669]:
                  - generic [ref=e670]: Water Polo
                  - heading "Event A" [level=3] [ref=e671]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [ref=e673] [cursor=pointer]':
                - /url: /event/b2e3f38e-d1e3-45be-a8a3-300b54cdb1a3
                - generic [ref=e674]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [ref=e676]
                  - generic [ref=e678]:
                    - img [ref=e679]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e682]:
                  - generic [ref=e683]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [level=3] [ref=e684]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [ref=e686] [cursor=pointer]':
                - /url: /event/848e2337-26b6-4a7b-ae72-e69cc536c49c
                - generic [ref=e687]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [ref=e689]
                  - generic [ref=e691]:
                    - img [ref=e692]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e695]:
                  - generic [ref=e696]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [level=3] [ref=e697]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [ref=e699] [cursor=pointer]':
                - /url: /event/587976e0-d3e1-4637-9734-4fa364af86dc
                - generic [ref=e700]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [ref=e702]
                  - generic [ref=e704]:
                    - img [ref=e705]
                    - text: Apr 23
                  - generic:
                    - generic:
                      - img
                - generic [ref=e708]:
                  - generic [ref=e709]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [level=3] [ref=e710]
        - generic [ref=e713]:
          - generic [ref=e714]:
            - generic [ref=e715]: Help center
            - heading "Questions? Answered." [level=2] [ref=e717]:
              - text: Questions?
              - text: Answered.
            - paragraph [ref=e718]: The essentials about watching, replays and your membership — in one tap.
            - generic [ref=e719]:
              - heading "Still need a hand?" [level=3] [ref=e721]
              - paragraph [ref=e722]: Support is on the clock worldwide, every matchday.
              - link "Email" [ref=e724] [cursor=pointer]:
                - /url: /contact
                - img
                - generic [ref=e725]: Email
          - generic [ref=e727]:
            - generic [ref=e728]:
              - generic [ref=e729]:
                - button "01 How many devices can I use with my subscription?" [expanded] [ref=e730] [cursor=pointer]:
                  - generic [ref=e731]: "01"
                  - generic [ref=e732]: How many devices can I use with my subscription?
                  - img [ref=e734]
                - paragraph [ref=e739]: Up to 2
              - generic [ref=e740]:
                - button "02 I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?" [ref=e741] [cursor=pointer]:
                  - generic [ref=e742]: "02"
                  - generic [ref=e743]: I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?
                  - img [ref=e745]
                - generic [ref=e747]:
                  - paragraph [ref=e748]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e749]:
                    - listitem [ref=e750]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e751]: Check your internet connection.
                    - listitem [ref=e752]:
                      - text: You can click
                      - link "[this link]" [ref=e753] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                  - paragraph [ref=e754]
                  - paragraph [ref=e755]
              - generic [ref=e756]:
                - button "03 How do I cancel my subscription?" [ref=e757] [cursor=pointer]:
                  - generic [ref=e758]: "03"
                  - generic [ref=e759]: How do I cancel my subscription?
                  - img [ref=e761]
                - list [ref=e764]:
                  - listitem [ref=e765]: Click on My account on the header
                  - listitem [ref=e766]: Select my account
                  - listitem [ref=e767]: Click on cancel subscription
              - generic [ref=e768]:
                - button "04 Why am I still being charged after canceling my subscription?" [ref=e769] [cursor=pointer]:
                  - generic [ref=e770]: "04"
                  - generic [ref=e771]: Why am I still being charged after canceling my subscription?
                  - img [ref=e773]
                - list [ref=e776]:
                  - listitem [ref=e777]: If you are being charged, please check your subscription status and click cancel. Cancel subscription is best done on Chrome of Safari web browser on your mobile, tablet or desktop.
                  - listitem [ref=e778]: You cannot cancel subscription via mobile app at this time.
              - generic [ref=e779]:
                - button "05 I was unable to watch a live event due to a website or technology problem. Can I get a refund?" [ref=e780] [cursor=pointer]:
                  - generic [ref=e781]: "05"
                  - generic [ref=e782]: I was unable to watch a live event due to a website or technology problem. Can I get a refund?
                  - img [ref=e784]
                - generic [ref=e786]:
                  - paragraph [ref=e787]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e788]:
                    - listitem [ref=e789]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e790]: Check your internet connection.
                    - listitem [ref=e791]:
                      - text: You can click
                      - link "[this link]" [ref=e792] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                    - listitem [ref=e793]:
                      - text: If the problem persists, please contact us via email at
                      - strong [ref=e794]:
                        - link "support@overnght.com" [ref=e795] [cursor=pointer]:
                          - /url: mailto:support@overnght.com
                      - text: .
                  - paragraph [ref=e796]
            - link "See all FAQs" [ref=e797] [cursor=pointer]:
              - /url: /faq
              - text: See all FAQs
              - img [ref=e798]
        - generic [ref=e801]:
          - generic [ref=e802]:
            - generic [ref=e803]:
              - generic [ref=e804]:
                - link "Overnght — Home" [ref=e805] [cursor=pointer]:
                  - /url: /
                  - img [ref=e806]
                - paragraph [ref=e809]: Live sports and exclusive content. Watch live or on demand, in HD.
              - generic [ref=e810]:
                - link "Download Overnght on the App Store" [ref=e811] [cursor=pointer]:
                  - /url: https://apps.apple.com/us/app/overnght/id6476713008
                  - img [ref=e812]
                  - generic [ref=e814]:
                    - generic [ref=e815]: Download on the
                    - generic [ref=e816]: App Store
                - link "Get Overnght on Google Play" [ref=e817] [cursor=pointer]:
                  - /url: https://play.google.com/store/apps/details?id=com.overnght.app
                  - img [ref=e818]
                  - generic [ref=e820]:
                    - generic [ref=e821]: Get it on
                    - generic [ref=e822]: Google Play
            - navigation "Footer" [ref=e823]:
              - generic [ref=e824]:
                - heading "Watch" [level=3] [ref=e825]
                - list [ref=e826]:
                  - listitem [ref=e827]:
                    - link "Home" [ref=e828] [cursor=pointer]:
                      - /url: /
                  - listitem [ref=e829]:
                    - link "Schedule" [ref=e830] [cursor=pointer]:
                      - /url: /schedule
                  - listitem [ref=e831]:
                    - link "On Demand" [ref=e832] [cursor=pointer]:
                      - /url: /search
              - generic [ref=e833]:
                - heading "Account" [level=3] [ref=e834]
                - list [ref=e835]:
                  - listitem [ref=e836]:
                    - link "My account" [ref=e837] [cursor=pointer]:
                      - /url: /account
                  - listitem [ref=e838]:
                    - link "Subscription" [ref=e839] [cursor=pointer]:
                      - /url: /subscription
              - generic [ref=e840]:
                - heading "Support" [level=3] [ref=e841]
                - list [ref=e842]:
                  - listitem [ref=e843]:
                    - link "FAQ" [ref=e844] [cursor=pointer]:
                      - /url: /faq
                  - listitem [ref=e845]:
                    - link "Contact" [ref=e846] [cursor=pointer]:
                      - /url: /contact
          - generic [ref=e847]:
            - paragraph [ref=e848]: © Overnght 2026
            - navigation "Legal" [ref=e849]:
              - link "Privacy Policy" [ref=e850] [cursor=pointer]:
                - /url: /legalese/termsOfService#privacy-policy
              - link "Terms of Use" [ref=e851] [cursor=pointer]:
                - /url: /legalese/termsOfService
  - alert [ref=e852]
  - generic [ref=e857]:
    - generic [ref=e858]:
      - img [ref=e860]
      - paragraph [ref=e862]:
        - text: We use cookies to improve your experience and analyze platform usage.
        - link "Privacy Policy" [ref=e863] [cursor=pointer]:
          - /url: /legalese/termsOfService#privacy-policy
    - generic [ref=e864]:
      - button "Decline" [ref=e865]
      - button "Accept Cookies" [ref=e866]
  - region "Notifications Alt+T"
  - generic:
    - list [ref=e867]:
      - img [ref=e869] [cursor=pointer]
      - listitem [ref=e871]:
        - 'generic "Chatbot wrote: Ask us" [ref=e872] [cursor=pointer]': Ask us
    - button "Button to initiate Chatbot Dialogue" [ref=e873] [cursor=pointer]:
      - img "Open or close chat" [ref=e874]
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