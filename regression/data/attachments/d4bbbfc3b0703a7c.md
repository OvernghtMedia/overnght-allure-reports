# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../auth/sign-in.spec.ts >> Sign In >> TC-AUTH-004: logout clears token and leaves guest header
- Location: auth/sign-in.spec.ts:247:7

# Error details

```
TimeoutError: locator.click: Timeout 30000ms exceeded.
Call log:
  - waiting for getByRole('button', { name: 'Account menu' })
    - locator resolved to <button type="button" aria-haspopup="true" aria-expanded="false" aria-label="Account menu" class="rounded-full outline-none ring-offset-2 ring-offset-surface-header transition-shadow ring-0">…</button>
  - attempting click action
    2 × waiting for element to be visible, enabled and stable
      - element is visible, enabled and stable
      - scrolling into view if needed
      - done scrolling
      - <div class="absolute inset-0 bg-black/70 backdrop-blur-sm"></div> from <div class="fixed inset-0 z-[100] flex items-end">…</div> subtree intercepts pointer events
    - retrying click action
    - waiting 20ms
    2 × waiting for element to be visible, enabled and stable
      - element is visible, enabled and stable
      - scrolling into view if needed
      - done scrolling
      - <div class="absolute inset-0 bg-black/70 backdrop-blur-sm"></div> from <div class="fixed inset-0 z-[100] flex items-end">…</div> subtree intercepts pointer events
    - retrying click action
      - waiting 100ms
    37 × waiting for element to be visible, enabled and stable
       - element is visible, enabled and stable
       - scrolling into view if needed
       - done scrolling
       - <div class="absolute inset-0 bg-black/70 backdrop-blur-sm"></div> from <div class="fixed inset-0 z-[100] flex items-end">…</div> subtree intercepts pointer events
     - retrying click action
       - waiting 500ms

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
          - link "Subscribe" [ref=e22] [cursor=pointer]:
            - /url: /subscription
          - button "Account menu" [ref=e24] [cursor=pointer]:
            - generic [ref=e25]: TU
          - link "Help" [ref=e26] [cursor=pointer]:
            - /url: /faq
            - img
    - main [ref=e27]:
      - generic [ref=e30]:
        - region "Featured" [ref=e31]:
          - generic [ref=e32] [cursor=pointer]:
            - img "OVERNGHT AND INDOOR FOOTBALL LEAGUE ANNOUNCE MULTI-YEAR AGREEMENT" [ref=e35]
            - img [ref=e38]
            - img [ref=e41]
            - generic:
              - generic:
                - generic:
                  - generic:
                    - generic:
                      - heading "OVERNGHT AND INDOOR FOOTBALL LEAGUE ANNOUNCE MULTI-YEAR AGREEMENT" [level=1]
                      - paragraph: March 9, 2026 Overnght and the Indoor Football League (IFL) today announced a landmark multi-year, multi-million-dollar media rights agreement that will make Overnght a premier national broadcast partner of the league for the 2026, 2027, and 2028 seasons.
                  - generic:
                    - button "Learn more" [ref=e42]:
                      - text: Learn more
                      - img
                    - button "Share" [ref=e43]:
                      - img
                      - text: Share
            - generic:
              - generic:
                - generic [ref=e44]:
                  - button "Go to slide 1" [ref=e45]
                  - button "Go to slide 2" [ref=e48]
                  - button "Go to slide 3" [ref=e49]
                - generic [ref=e50]:
                  - button "Previous slide" [ref=e51]:
                    - img [ref=e52]
                  - button "Next slide" [ref=e54]:
                    - img [ref=e55]
        - generic [ref=e57]:
          - generic [ref=e58]:
            - generic [ref=e59]:
              - generic [ref=e60]:
                - heading "On the Horizon" [level=2] [ref=e62]
                - paragraph [ref=e63]: Exciting competitions and events coming your way - set your calendar
              - generic [ref=e64]:
                - link "See all" [ref=e65] [cursor=pointer]:
                  - /url: /schedule/search
                - generic [ref=e66]:
                  - button "Scroll left" [disabled] [ref=e67]:
                    - img [ref=e68]
                  - button "Scroll right" [ref=e70] [cursor=pointer]:
                    - img [ref=e71]
            - generic [ref=e73]:
              - 'link "Rowing: San Diego Crew Classic" [ref=e75] [cursor=pointer]':
                - /url: /event/88834c9e-1bb1-42d0-afc5-403026dfbbc7
                - generic [ref=e76]:
                  - img "San Diego Crew Classic" [ref=e78]
                  - generic [ref=e80]: DELAYED
                  - generic [ref=e82]:
                    - img [ref=e83]
                    - text: Mar 28 · 2:00 PM
                  - img "Subscription required" [ref=e87]:
                    - img [ref=e88]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e91]:
                  - generic [ref=e92]: Rowing
                  - heading "San Diego Crew Classic" [level=3] [ref=e93]
              - 'link "Women''s Water Polo: featured 1" [ref=e95] [cursor=pointer]':
                - /url: /event/c2454e40-5040-4f06-a0e7-d4dfa066e0e6
                - generic [ref=e96]:
                  - img "featured 1" [ref=e98]
                  - generic [ref=e100]: DELAYED
                  - generic [ref=e102]:
                    - img [ref=e103]
                    - text: Jun 1 · 3:00 PM
                  - img "Subscription required" [ref=e107]:
                    - img [ref=e108]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e111]:
                  - generic [ref=e112]: Women's Water Polo
                  - heading "featured 1" [level=3] [ref=e113]
              - 'link "Women''s Water Polo: featured 2" [ref=e115] [cursor=pointer]':
                - /url: /event/f7c30c7f-f495-4492-813d-ce4654a60ec5
                - generic [ref=e116]:
                  - img "featured 2" [ref=e118]
                  - generic [ref=e120]: DELAYED
                  - generic [ref=e122]:
                    - img [ref=e123]
                    - text: Jun 2 · 4:00 PM
                  - img "Subscription required" [ref=e127]:
                    - img [ref=e128]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e131]:
                  - generic [ref=e132]: Women's Water Polo
                  - heading "featured 2" [level=3] [ref=e133]
              - 'link "Women''s Water Polo: featured 3" [ref=e135] [cursor=pointer]':
                - /url: /event/8a8afe75-674c-4c35-9d3c-60c2a7dbc30d
                - generic [ref=e136]:
                  - img "featured 3" [ref=e138]
                  - generic [ref=e140]: DELAYED
                  - generic [ref=e142]:
                    - img [ref=e143]
                    - text: Jun 3 · 5:00 PM
                  - img "Subscription required" [ref=e147]:
                    - img [ref=e148]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e151]:
                  - generic [ref=e152]: Women's Water Polo
                  - heading "featured 3" [level=3] [ref=e153]
              - 'link "Men''s Rowing: test events" [ref=e155] [cursor=pointer]':
                - /url: /event/a9e0cedb-1bf6-4cff-91f3-e7b63ae530af
                - generic [ref=e156]:
                  - img "test events" [ref=e158]
                  - generic [ref=e160]: DELAYED
                  - generic [ref=e162]:
                    - img [ref=e163]
                    - text: Wed · 6:00 PM
                  - img "Subscription required" [ref=e167]:
                    - img [ref=e168]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e171]:
                  - generic [ref=e172]: Men's Rowing
                  - heading "test events" [level=3] [ref=e173]
              - 'link "Water Polo: event 2" [ref=e175] [cursor=pointer]':
                - /url: /event/5f0bef70-09f8-4400-9d16-8d9b22066701
                - generic [ref=e176]:
                  - img "event 2" [ref=e178]
                  - generic [ref=e180]: DELAYED
                  - generic [ref=e182]:
                    - img [ref=e183]
                    - text: Thu · 7:00 PM
                  - img "Subscription required" [ref=e187]:
                    - img [ref=e188]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e191]:
                  - generic [ref=e192]: Water Polo
                  - heading "event 2" [level=3] [ref=e193]
              - 'link "Women''s Water Polo: event 3" [ref=e195] [cursor=pointer]':
                - /url: /event/0ccbc356-3ea4-48b1-a4bc-cc0245cca381
                - generic [ref=e196]:
                  - generic [ref=e198]:
                    - img "event 3" [ref=e200]
                    - img "event 3" [ref=e202]
                    - generic [ref=e203]: VS
                  - generic [ref=e205]: DELAYED
                  - generic [ref=e207]:
                    - img [ref=e208]
                    - text: Sat · 5:00 PM
                  - img "Subscription required" [ref=e212]:
                    - img [ref=e213]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e216]:
                  - generic [ref=e217]: Women's Water Polo
                  - heading "event 3" [level=3] [ref=e218]
          - generic [ref=e219]:
            - generic [ref=e221]:
              - heading "Popular Sports" [level=2] [ref=e223]
              - paragraph [ref=e224]: Explore world-class events and competitions across different sporting disciplines
            - generic [ref=e225]:
              - link "Water Polo" [ref=e226] [cursor=pointer]:
                - /url: /sports/water-polo
                - img [ref=e229]
                - heading "Water Polo" [level=3] [ref=e233]
              - link "Rowing" [ref=e234] [cursor=pointer]:
                - /url: /sports/rowing
                - img [ref=e237]
                - heading "Rowing" [level=3] [ref=e241]
              - link "Football" [ref=e242] [cursor=pointer]:
                - /url: /sports/football
                - img [ref=e245]
                - heading "Football" [level=3] [ref=e249]
          - generic [ref=e250]:
            - generic [ref=e252]:
              - heading "Conferences" [level=2] [ref=e254]
              - paragraph [ref=e255]: Explore sports conferences and leagues
            - generic [ref=e256]:
              - link "European Aquatics Water Polo European Aquatics Water Polo" [ref=e257] [cursor=pointer]:
                - /url: /conferences/european-aquatics-water-polo
                - generic [ref=e258]:
                  - img "European Aquatics Water Polo" [ref=e265]
                  - paragraph [ref=e269]: European Aquatics Water Polo
              - link "USAWP USAWP" [ref=e270] [cursor=pointer]:
                - /url: /conferences/usawp
                - generic [ref=e271]:
                  - img "USAWP" [ref=e278]
                  - paragraph [ref=e282]: USAWP
              - link "USRowing USRowing" [ref=e283] [cursor=pointer]:
                - /url: /conferences/usrowing
                - generic [ref=e284]:
                  - img "USRowing" [ref=e291]
                  - paragraph [ref=e295]: USRowing
          - generic [ref=e296]:
            - generic [ref=e297]:
              - generic [ref=e298]:
                - heading "Featured Past Events" [level=2] [ref=e300]
                - paragraph [ref=e301]: The main competition you can't miss
              - generic [ref=e302]:
                - link "See all" [ref=e303] [cursor=pointer]:
                  - /url: /search?featured=1
                - generic [ref=e304]:
                  - button "Scroll left" [disabled] [ref=e305]:
                    - img [ref=e306]
                  - button "Scroll right" [ref=e308] [cursor=pointer]:
                    - img [ref=e309]
            - generic [ref=e311]:
              - 'link "Men''s Water Polo: Super Cup 2025 - Pro Recco vs. FTC" [ref=e313] [cursor=pointer]':
                - /url: /event/1cf33c12-e9e0-4652-a835-c29574f0fc03
                - generic [ref=e314]:
                  - img "Super Cup 2025 - Pro Recco vs. FTC" [ref=e316]
                  - generic [ref=e318]:
                    - img [ref=e319]
                    - text: Oct 8, 2025
                  - img "Subscription required" [ref=e323]:
                    - img [ref=e324]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e327]:
                  - generic [ref=e328]: Men's Water Polo
                  - heading "Super Cup 2025 - Pro Recco vs. FTC" [level=3] [ref=e329]
              - 'link "Men''s Water Polo: Princeton vs. FTC Telekom" [ref=e331] [cursor=pointer]':
                - /url: /event/3b1b3223-425c-4845-81a9-a086fe1a8e3a
                - generic [ref=e332]:
                  - img "Princeton vs. FTC Telekom" [ref=e334]
                  - generic [ref=e336]:
                    - img [ref=e337]
                    - text: Sep 3, 2025
                  - img "Subscription required" [ref=e341]:
                    - img [ref=e342]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e345]:
                  - generic [ref=e346]: Men's Water Polo
                  - heading "Princeton vs. FTC Telekom" [level=3] [ref=e347]
              - 'link "Men''s Water Polo: Pro Recco vs. UCLA" [ref=e349] [cursor=pointer]':
                - /url: /event/c5da92ff-029c-4254-96cc-a9c538074b60
                - generic [ref=e350]:
                  - img "Pro Recco vs. UCLA" [ref=e352]
                  - generic [ref=e354]:
                    - img [ref=e355]
                    - text: Sep 3, 2025
                  - img "Subscription required" [ref=e359]:
                    - img [ref=e360]
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
                  - img "Subscription required" [ref=e377]:
                    - img [ref=e378]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e381]:
                  - generic [ref=e382]: Rowing
                  - 'heading "2025 Day 1: USRowing RowFest National Championships" [level=3] [ref=e383]'
              - 'link "Rowing: Day 2: 2025 USRowing Youth National Championships" [ref=e385] [cursor=pointer]':
                - /url: /event/68f89bac-bb5a-4d03-a390-070137b179b3
                - generic [ref=e386]:
                  - 'img "Day 2: 2025 USRowing Youth National Championships" [ref=e388]'
                  - generic [ref=e390]:
                    - img [ref=e391]
                    - text: Jun 13, 2025
                  - img "Subscription required" [ref=e395]:
                    - img [ref=e396]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e399]:
                  - generic [ref=e400]: Rowing
                  - 'heading "Day 2: 2025 USRowing Youth National Championships" [level=3] [ref=e401]'
              - 'link "Rowing: Day 1: 2025 USRowing Youth National Championships" [ref=e403] [cursor=pointer]':
                - /url: /event/a398171a-d01f-4b99-8cdf-e3c7738f1f07
                - generic [ref=e404]:
                  - 'img "Day 1: 2025 USRowing Youth National Championships" [ref=e406]'
                  - generic [ref=e408]:
                    - img [ref=e409]
                    - text: Jun 12, 2025
                  - img "Subscription required" [ref=e413]:
                    - img [ref=e414]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e417]:
                  - generic [ref=e418]: Rowing
                  - 'heading "Day 1: 2025 USRowing Youth National Championships" [level=3] [ref=e419]'
          - generic [ref=e420]:
            - generic [ref=e421]:
              - generic [ref=e422]:
                - heading "Featured Overnght Shows" [level=2] [ref=e424]
                - paragraph [ref=e425]: Unique sports talk and behind-the-scenes shows, only here
              - link "See all" [ref=e427] [cursor=pointer]:
                - /url: /search?show=1&featured=1
            - generic [ref=e428]:
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e430] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5
                - article [ref=e431]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e434]
                  - generic [ref=e435]:
                    - generic [ref=e436]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e437]
                    - generic [ref=e438]: Rowing
                    - generic [ref=e439]:
                      - img [ref=e440]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e443] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980
                - article [ref=e444]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e447]
                  - generic [ref=e448]:
                    - generic [ref=e449]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e450]
                    - generic [ref=e451]: Rowing
                    - generic [ref=e452]:
                      - img [ref=e453]
                      - text: Watch Now
          - generic [ref=e455]:
            - generic [ref=e456]:
              - generic [ref=e457]:
                - heading "All Overnght Shows" [level=2] [ref=e459]
                - paragraph [ref=e460]: Late-night sports content and exclusive shows
              - generic [ref=e461]:
                - link "See all" [ref=e462] [cursor=pointer]:
                  - /url: /search?show=1
                - generic [ref=e463]:
                  - button "Scroll left" [disabled] [ref=e464]:
                    - img [ref=e465]
                  - button "Scroll right" [ref=e467] [cursor=pointer]:
                    - img [ref=e468]
            - generic [ref=e470]:
              - link "The Counter Attack ON Overnght Ep 41 | March 4, 2026 — show" [ref=e472] [cursor=pointer]:
                - /url: /event/4ad7c642-76de-4694-a9ed-052243bb959c
                - article [ref=e473]:
                  - img "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [ref=e476]
                  - generic [ref=e477]:
                    - generic [ref=e478]: Mar 5 · 6:15 PM
                    - heading "The Counter Attack ON Overnght Ep 41 | March 4, 2026" [level=3] [ref=e479]
                    - generic [ref=e480]: Water Polo
                    - generic [ref=e481]:
                      - img [ref=e482]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 25, 2026 — show" [ref=e485] [cursor=pointer]:
                - /url: /event/5c84a6fd-6320-4b8d-b159-2c58f8908b15
                - article [ref=e486]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [ref=e489]
                  - generic [ref=e490]:
                    - generic [ref=e491]: Mar 2 · 7:15 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 25, 2026" [level=3] [ref=e492]
                    - generic [ref=e493]: Water Polo
                    - generic [ref=e494]:
                      - img [ref=e495]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 40 | February 26, 2026 — show" [ref=e498] [cursor=pointer]:
                - /url: /event/1635113c-beee-489c-b512-5153efb101e1
                - article [ref=e499]:
                  - img "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [ref=e502]
                  - generic [ref=e503]:
                    - generic [ref=e504]: Feb 26 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 40 | February 26, 2026" [level=3] [ref=e505]
                    - generic [ref=e506]: Water Polo
                    - generic [ref=e507]:
                      - img [ref=e508]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.4 — show" [ref=e511] [cursor=pointer]:
                - /url: /event/c4a63e93-2463-42da-8405-c439d7560aa1
                - article [ref=e512]:
                  - img "Rowing Wolf Podcast, Ep1.4" [ref=e515]
                  - generic [ref=e516]:
                    - generic [ref=e517]: Feb 24 · 10:05 PM
                    - heading "Rowing Wolf Podcast, Ep1.4" [level=3] [ref=e518]
                    - generic [ref=e519]: Rowing
                    - generic [ref=e520]:
                      - img [ref=e521]
                      - text: Watch Now
              - link "The Counter Attack ON Overnght Ep 39 | February 18, 2026 — show" [ref=e524] [cursor=pointer]:
                - /url: /event/bca89acc-e481-4d23-8e93-df683231f507
                - article [ref=e525]:
                  - img "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [ref=e528]
                  - generic [ref=e529]:
                    - generic [ref=e530]: Feb 20 · 3:10 PM
                    - heading "The Counter Attack ON Overnght Ep 39 | February 18, 2026" [level=3] [ref=e531]
                    - generic [ref=e532]: Water Polo
                    - generic [ref=e533]:
                      - img [ref=e534]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.2 — show" [ref=e537] [cursor=pointer]:
                - /url: /event/1b8d4fdc-ff71-46af-8161-cef3f3b260e5
                - article [ref=e538]:
                  - img "Rowing Wolf Podcast, Ep1.2" [ref=e541]
                  - generic [ref=e542]:
                    - generic [ref=e543]: Nov 27, 2025 · 7:50 AM
                    - heading "Rowing Wolf Podcast, Ep1.2" [level=3] [ref=e544]
                    - generic [ref=e545]: Rowing
                    - generic [ref=e546]:
                      - img [ref=e547]
                      - text: Watch Now
              - link "Rowing Wolf Podcast, Ep1.1 — show" [ref=e550] [cursor=pointer]:
                - /url: /event/aa9d4549-142f-4ab1-aa69-c06300c48980
                - article [ref=e551]:
                  - img "Rowing Wolf Podcast, Ep1.1" [ref=e554]
                  - generic [ref=e555]:
                    - generic [ref=e556]: Nov 5, 2025 · 3:00 AM
                    - heading "Rowing Wolf Podcast, Ep1.1" [level=3] [ref=e557]
                    - generic [ref=e558]: Rowing
                    - generic [ref=e559]:
                      - img [ref=e560]
                      - text: Watch Now
              - link "2025 Cutino Awards — show" [ref=e563] [cursor=pointer]:
                - /url: /event/6f99d5e7-fb65-429d-9024-fef463d2f2d4
                - article [ref=e564]:
                  - img "2025 Cutino Awards" [ref=e567]
                  - generic [ref=e568]:
                    - generic [ref=e569]: Jun 8, 2025 · 1:45 AM
                    - heading "2025 Cutino Awards" [level=3] [ref=e570]
                    - generic [ref=e571]: Water Polo
                    - generic [ref=e572]:
                      - img [ref=e573]
                      - text: Watch Now
              - link "JRN IRA National Championship Day Three Review — show" [ref=e576] [cursor=pointer]:
                - /url: /event/1ae42c95-a95b-4e4a-a9cc-99615adc4d67
                - article [ref=e577]:
                  - img "JRN IRA National Championship Day Three Review" [ref=e580]
                  - generic [ref=e581]:
                    - generic [ref=e582]: Jun 1, 2025 · 9:40 PM
                    - heading "JRN IRA National Championship Day Three Review" [level=3] [ref=e583]
                    - generic [ref=e584]: Rowing
                    - generic [ref=e585]:
                      - img [ref=e586]
                      - text: Watch Now
          - generic [ref=e588]:
            - generic [ref=e589]:
              - generic [ref=e590]:
                - heading "All Past Events" [level=2] [ref=e592]
                - paragraph [ref=e593]: Browse every event in one place
              - generic [ref=e594]:
                - link "See all" [ref=e595] [cursor=pointer]:
                  - /url: /search
                - generic [ref=e596]:
                  - button "Scroll left" [disabled] [ref=e597]:
                    - img [ref=e598]
                  - button "Scroll right" [ref=e600] [cursor=pointer]:
                    - img [ref=e601]
            - generic [ref=e603]:
              - 'link "Water Polo: Live test event 0512" [ref=e605] [cursor=pointer]':
                - /url: /event/27aac4b3-ccca-478e-b178-e76424220b40
                - generic [ref=e606]:
                  - img "Live test event 0512" [ref=e608]
                  - generic [ref=e610]:
                    - img [ref=e611]
                    - text: May 12
                  - img "Subscription required" [ref=e615]:
                    - img [ref=e616]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e619]:
                  - generic [ref=e620]: Water Polo
                  - heading "Live test event 0512" [level=3] [ref=e621]
              - 'link "Water Polo: Live Event for Autotests" [ref=e623] [cursor=pointer]':
                - /url: /event/7dfe92c5-6773-4025-980f-3924167d6114
                - generic [ref=e624]:
                  - generic [ref=e626]:
                    - img "Live Event for Autotests" [ref=e628]
                    - img "Live Event for Autotests" [ref=e630]
                    - generic [ref=e631]: VS
                  - generic [ref=e633]:
                    - img [ref=e634]
                    - text: May 11
                  - img "Subscription required" [ref=e638]:
                    - img [ref=e639]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e642]:
                  - generic [ref=e643]: Water Polo
                  - heading "Live Event for Autotests" [level=3] [ref=e644]
              - 'link "Water Polo: Event B" [ref=e646] [cursor=pointer]':
                - /url: /event/3b4001ce-9481-4f9d-871e-367c8b47d5a7
                - generic [ref=e647]:
                  - img "Event B" [ref=e649]
                  - generic [ref=e651]:
                    - img [ref=e652]
                    - text: Apr 23
                  - img "Subscription required" [ref=e656]:
                    - img [ref=e657]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e660]:
                  - generic [ref=e661]: Water Polo
                  - heading "Event B" [level=3] [ref=e662]
              - 'link "Water Polo: Event A" [ref=e664] [cursor=pointer]':
                - /url: /event/d1ea6b2b-f306-4ee2-b893-5b0fe4199522
                - generic [ref=e665]:
                  - img "Event A" [ref=e667]
                  - generic [ref=e669]:
                    - img [ref=e670]
                    - text: Apr 23
                  - img "Subscription required" [ref=e674]:
                    - img [ref=e675]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e678]:
                  - generic [ref=e679]: Water Polo
                  - heading "Event A" [level=3] [ref=e680]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [ref=e682] [cursor=pointer]':
                - /url: /event/b2e3f38e-d1e3-45be-a8a3-300b54cdb1a3
                - generic [ref=e683]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [ref=e685]
                  - generic [ref=e687]:
                    - img [ref=e688]
                    - text: Apr 23
                  - img "Subscription required" [ref=e692]:
                    - img [ref=e693]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e696]:
                  - generic [ref=e697]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 4" [level=3] [ref=e698]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [ref=e700] [cursor=pointer]':
                - /url: /event/848e2337-26b6-4a7b-ae72-e69cc536c49c
                - generic [ref=e701]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [ref=e703]
                  - generic [ref=e705]:
                    - img [ref=e706]
                    - text: Apr 23
                  - img "Subscription required" [ref=e710]:
                    - img [ref=e711]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e714]:
                  - generic [ref=e715]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 3" [level=3] [ref=e716]
              - 'link "Water Polo: TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [ref=e718] [cursor=pointer]':
                - /url: /event/587976e0-d3e1-4637-9734-4fa364af86dc
                - generic [ref=e719]:
                  - img "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [ref=e721]
                  - generic [ref=e723]:
                    - img [ref=e724]
                    - text: Apr 23
                  - img "Subscription required" [ref=e728]:
                    - img [ref=e729]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e732]:
                  - generic [ref=e733]: Water Polo
                  - heading "TC-10. Overlap of two events on one channel - checking the dedupe EVENT 1" [level=3] [ref=e734]
              - 'link "Water Polo: TC-9. Recording End arrived, but End Stream wasn''t pressed v2" [ref=e736] [cursor=pointer]':
                - /url: /event/6b8424be-0734-47ab-ae82-689bd3dad1b7
                - generic [ref=e737]:
                  - img "TC-9. Recording End arrived, but End Stream wasn't pressed v2" [ref=e739]
                  - generic [ref=e741]:
                    - img [ref=e742]
                    - text: Apr 23
                  - img "Subscription required" [ref=e746]:
                    - img [ref=e747]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e750]:
                  - generic [ref=e751]: Water Polo
                  - heading "TC-9. Recording End arrived, but End Stream wasn't pressed v2" [level=3] [ref=e752]
              - 'link "Water Polo: TC-9. Recording End arrived, but End Stream wasn''t pressed." [ref=e754] [cursor=pointer]':
                - /url: /event/360f6ed0-42e0-4cc5-81cd-44338f66e6d6
                - generic [ref=e755]:
                  - img "TC-9. Recording End arrived, but End Stream wasn't pressed." [ref=e757]
                  - generic [ref=e759]:
                    - img [ref=e760]
                    - text: Apr 23
                  - img "Subscription required" [ref=e764]:
                    - img [ref=e765]
                  - generic:
                    - generic:
                      - img
                - generic [ref=e768]:
                  - generic [ref=e769]: Water Polo
                  - heading "TC-9. Recording End arrived, but End Stream wasn't pressed." [level=3] [ref=e770]
        - generic [ref=e773]:
          - generic [ref=e774]:
            - generic [ref=e775]: Help center
            - heading "Questions? Answered." [level=2] [ref=e777]:
              - text: Questions?
              - text: Answered.
            - paragraph [ref=e778]: The essentials about watching, replays and your membership — in one tap.
            - generic [ref=e779]:
              - heading "Still need a hand?" [level=3] [ref=e781]
              - paragraph [ref=e782]: Support is on the clock worldwide, every matchday.
              - link "Email" [ref=e784] [cursor=pointer]:
                - /url: /contact
                - img
                - generic [ref=e785]: Email
          - generic [ref=e787]:
            - generic [ref=e788]:
              - generic [ref=e789]:
                - button "01 How many devices can I use with my subscription?" [expanded] [ref=e790] [cursor=pointer]:
                  - generic [ref=e791]: "01"
                  - generic [ref=e792]: How many devices can I use with my subscription?
                  - img [ref=e794]
                - paragraph [ref=e799]: Up to 2
              - generic [ref=e800]:
                - button "02 I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?" [ref=e801] [cursor=pointer]:
                  - generic [ref=e802]: "02"
                  - generic [ref=e803]: I'm experiencing connection problems, audio quality issues, or full-screen viewing problems. What should I do?
                  - img [ref=e805]
                - generic [ref=e807]:
                  - paragraph [ref=e808]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e809]:
                    - listitem [ref=e810]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e811]: Check your internet connection.
                    - listitem [ref=e812]:
                      - text: You can click
                      - link "[this link]" [ref=e813] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                  - paragraph [ref=e814]
                  - paragraph [ref=e815]
              - generic [ref=e816]:
                - button "03 How do I cancel my subscription?" [ref=e817] [cursor=pointer]:
                  - generic [ref=e818]: "03"
                  - generic [ref=e819]: How do I cancel my subscription?
                  - img [ref=e821]
                - list [ref=e824]:
                  - listitem [ref=e825]: Click on My account on the header
                  - listitem [ref=e826]: Select my account
                  - listitem [ref=e827]: Click on cancel subscription
              - generic [ref=e828]:
                - button "04 Why am I still being charged after canceling my subscription?" [ref=e829] [cursor=pointer]:
                  - generic [ref=e830]: "04"
                  - generic [ref=e831]: Why am I still being charged after canceling my subscription?
                  - img [ref=e833]
                - list [ref=e836]:
                  - listitem [ref=e837]: If you are being charged, please check your subscription status and click cancel. Cancel subscription is best done on Chrome of Safari web browser on your mobile, tablet or desktop.
                  - listitem [ref=e838]: You cannot cancel subscription via mobile app at this time.
              - generic [ref=e839]:
                - button "05 I was unable to watch a live event due to a website or technology problem. Can I get a refund?" [ref=e840] [cursor=pointer]:
                  - generic [ref=e841]: "05"
                  - generic [ref=e842]: I was unable to watch a live event due to a website or technology problem. Can I get a refund?
                  - img [ref=e844]
                - generic [ref=e846]:
                  - paragraph [ref=e847]: "Sorry that you had issues. But to watch events here are some tips:"
                  - list [ref=e848]:
                    - listitem [ref=e849]: Make sure you are using Google Chrome or Safari.
                    - listitem [ref=e850]: Check your internet connection.
                    - listitem [ref=e851]:
                      - text: You can click
                      - link "[this link]" [ref=e852] [cursor=pointer]:
                        - /url: https://fiber.google.com/speedtest/
                      - text: to test your connection—issues with connectivity often affect the quality of the transmission.
                    - listitem [ref=e853]:
                      - text: If the problem persists, please contact us via email at
                      - strong [ref=e854]:
                        - link "support@overnght.com" [ref=e855] [cursor=pointer]:
                          - /url: mailto:support@overnght.com
                      - text: .
                  - paragraph [ref=e856]
            - link "See all FAQs" [ref=e857] [cursor=pointer]:
              - /url: /faq
              - text: See all FAQs
              - img [ref=e858]
        - generic [ref=e861]:
          - generic [ref=e862]:
            - generic [ref=e863]:
              - generic [ref=e864]:
                - link "Overnght — Home" [ref=e865] [cursor=pointer]:
                  - /url: /
                  - img [ref=e866]
                - paragraph [ref=e869]: Live sports and exclusive content. Watch live or on demand, in HD.
              - generic [ref=e870]:
                - link "Download Overnght on the App Store" [ref=e871] [cursor=pointer]:
                  - /url: https://apps.apple.com/us/app/overnght/id6476713008
                  - img [ref=e872]
                  - generic [ref=e874]:
                    - generic [ref=e875]: Download on the
                    - generic [ref=e876]: App Store
                - link "Get Overnght on Google Play" [ref=e877] [cursor=pointer]:
                  - /url: https://play.google.com/store/apps/details?id=com.overnght.app
                  - img [ref=e878]
                  - generic [ref=e880]:
                    - generic [ref=e881]: Get it on
                    - generic [ref=e882]: Google Play
            - navigation "Footer" [ref=e883]:
              - generic [ref=e884]:
                - heading "Watch" [level=3] [ref=e885]
                - list [ref=e886]:
                  - listitem [ref=e887]:
                    - link "Home" [ref=e888] [cursor=pointer]:
                      - /url: /
                  - listitem [ref=e889]:
                    - link "Schedule" [ref=e890] [cursor=pointer]:
                      - /url: /schedule
                  - listitem [ref=e891]:
                    - link "On Demand" [ref=e892] [cursor=pointer]:
                      - /url: /search
              - generic [ref=e893]:
                - heading "Account" [level=3] [ref=e894]
                - list [ref=e895]:
                  - listitem [ref=e896]:
                    - link "My account" [ref=e897] [cursor=pointer]:
                      - /url: /account
                  - listitem [ref=e898]:
                    - link "Subscription" [ref=e899] [cursor=pointer]:
                      - /url: /subscription
              - generic [ref=e900]:
                - heading "Support" [level=3] [ref=e901]
                - list [ref=e902]:
                  - listitem [ref=e903]:
                    - link "FAQ" [ref=e904] [cursor=pointer]:
                      - /url: /faq
                  - listitem [ref=e905]:
                    - link "Contact" [ref=e906] [cursor=pointer]:
                      - /url: /contact
          - generic [ref=e907]:
            - paragraph [ref=e908]: © Overnght 2026
            - navigation "Legal" [ref=e909]:
              - link "Privacy Policy" [ref=e910] [cursor=pointer]:
                - /url: /legalese/termsOfService#privacy-policy
              - link "Terms of Use" [ref=e911] [cursor=pointer]:
                - /url: /legalese/termsOfService
  - alert [ref=e912]: Overnght - Live Sports Streaming | Overnght
  - generic [ref=e919]:
    - generic [ref=e920]:
      - img [ref=e922]
      - generic [ref=e925]:
        - heading "We've Updated Our Terms of Service" [level=2] [ref=e926]
        - paragraph [ref=e927]:
          - text: Please review and accept the updated terms to continue using Overnght.
          - link "Read full terms" [ref=e928] [cursor=pointer]:
            - /url: /legalese/termsOfService
            - text: Read full terms
            - img [ref=e929]
    - generic [ref=e933]:
      - generic [ref=e934]:
        - generic [ref=e935] [cursor=pointer]:
          - checkbox "I agree to the updated Terms*" [ref=e936]
          - generic [ref=e937]: I agree to the updated Terms*
        - generic [ref=e938] [cursor=pointer]:
          - checkbox "Allow analytics cookies" [ref=e939]
          - generic [ref=e940]: Allow analytics cookies
      - button "Accept & Continue" [disabled] [ref=e941]
  - region "Notifications Alt+T"
  - generic:
    - list [ref=e942]:
      - img [ref=e944] [cursor=pointer]
      - listitem [ref=e946]:
        - 'generic "Chatbot wrote: Ask us" [ref=e947] [cursor=pointer]': Ask us
    - button "Button to initiate Chatbot Dialogue" [ref=e948] [cursor=pointer]:
      - img "Open or close chat" [ref=e949]
```

# Test source

```ts
  177 |     });
  178 | 
  179 |     const login = new LoginPage(page);
  180 |     await login.waitForLoginScreen();
  181 |     await login.login(email, INVALID_LOGIN_PASSWORD);
  182 | 
  183 |     await expect(page).toHaveURL(/\/auth\/login(\/|\?|$)/);
  184 |     await expectToastWithText(page, /invalid email or password/i);
  185 |   });
  186 | 
  187 |   test('TC-AUTH-003: forgot password sends reset and shows inbox confirmation', async ({
  188 |     page,
  189 |     baseURL,
  190 |   }) => {
  191 |     test.skip(!baseURL, 'Playwright baseURL must be set (BASE_URL / PW_ENV)');
  192 | 
  193 |     const { email } = resolveSignInCredentials();
  194 | 
  195 |     await page.context().clearCookies();
  196 |     await page.goto(`${baseURL!.replace(/\/$/, '')}/auth/login`, {
  197 |       waitUntil: 'domcontentloaded',
  198 |     });
  199 | 
  200 |     const login = new LoginPage(page);
  201 |     await login.waitForLoginScreen();
  202 | 
  203 |     const forgot = new ForgotPasswordPage(page);
  204 |     await forgot.openFromLogin();
  205 |     await forgot.submitRegisteredEmail(email);
  206 | 
  207 |     // Toast is transient — check it optimistically, but don't fail if it disappears first.
  208 |     // The "Check your inbox" heading is the authoritative success indicator.
  209 |     const toastVisible = await page
  210 |       .getByRole('alert')
  211 |       .filter({ hasText: /reset link sent/i })
  212 |       .or(page.locator('.Toastify__toast-body').filter({ hasText: /reset link sent/i }))
  213 |       .or(page.getByText(/reset link sent/i))
  214 |       .first()
  215 |       .waitFor({ state: 'visible', timeout: 8_000 })
  216 |       .then(() => true)
  217 |       .catch(() => false);
  218 | 
  219 |     if (!toastVisible) {
  220 |       // Toast may have already disappeared — verify via heading instead
  221 |       await expect(
  222 |         page.getByRole('heading', { name: /check your inbox/i }),
  223 |       ).toBeVisible({ timeout: 20_000 });
  224 |     }
  225 | 
  226 |     await expect(
  227 |       page.getByRole('heading', { name: /check your inbox/i }),
  228 |     ).toBeVisible({ timeout: 20_000 });
  229 |     await expect(
  230 |       page.getByText('We emailed you a special link to:', { exact: true }),
  231 |     ).toBeVisible();
  232 |     await expect(
  233 |       page.getByText('Click to verify your email address', { exact: true }),
  234 |     ).toBeVisible();
  235 |     await expect(
  236 |       page.getByText(
  237 |         'Please check your inbox and follow the link to reset your password.',
  238 |         { exact: true },
  239 |       ),
  240 |     ).toBeVisible();
  241 |     await expect(
  242 |       page.getByRole('link', { name: /back to login/i }),
  243 |     ).toBeVisible();
  244 |     await expect(page.getByRole('button', { name: /try again/i })).toBeVisible();
  245 |   });
  246 | 
  247 |   test('TC-AUTH-004: logout clears token and leaves guest header', async ({
  248 |     page,
  249 |     baseURL,
  250 |   }) => {
  251 |     test.skip(!baseURL, 'Playwright baseURL must be set (BASE_URL / PW_ENV)');
  252 | 
  253 |     const { email, password } = resolveSignInCredentials();
  254 | 
  255 |     await page.context().clearCookies();
  256 |     await page.goto(`${baseURL!.replace(/\/$/, '')}/auth/login`, {
  257 |       waitUntil: 'domcontentloaded',
  258 |     });
  259 | 
  260 |     const login = new LoginPage(page);
  261 |     await login.waitForLoginScreen();
  262 |     await login.login(email, password);
  263 | 
  264 |     await expect(page).toHaveURL(
  265 |       new RegExp(`^${baseURL!.replace(/\/$/, '')}/?`),
  266 |     );
  267 | 
  268 |     await expect(page.locator('#main-content')).toBeVisible();
  269 | 
  270 |     // UPDATED for the header redesign (web PR #194): the old round UserMenu
  271 |     // avatar (`header div.cursor-pointer.rounded-full`) was replaced by the DS
  272 |     // `ProfileMenu` — trigger is `button[aria-label="Account menu"]`, the item
  273 |     // is "Logout". The logged-out header now shows a "Log in" LINK (not a
  274 |     // "Sign in" button).
  275 |     await page
  276 |       .getByRole('button', { name: 'Account menu' })
> 277 |       .click({ timeout: 30_000 });
      |        ^ TimeoutError: locator.click: Timeout 30000ms exceeded.
  278 |     await page.getByRole('button', { name: /^logout$/i }).click();
  279 | 
  280 |     await expect(page).toHaveURL(
  281 |       new RegExp(`^${baseURL!.replace(/\/$/, '')}/?$`),
  282 |     );
  283 | 
  284 |     const cookies = await page.context().cookies();
  285 |     expect(cookies.find((c) => c.name === 'token')).toBeUndefined();
  286 | 
  287 |     // Scope to the header — the footer also has a "Log in" link, so an
  288 |     // unscoped name match hits two elements (strict-mode violation).
  289 |     await expect(
  290 |       page.getByRole('banner').getByRole('link', { name: /^log in$/i }),
  291 |     ).toBeVisible({ timeout: 30_000 });
  292 |   });
  293 | });
  294 | 
```