# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: ../ui/subscription-duplicate-repro.spec.ts >> Subscription duplicate reproduction (user flows) >> 3DS stall: always-authenticate (4000002760003184), Visa in tab B
- Location: ui/subscription-duplicate-repro.spec.ts:195:9

# Error details

```
Test timeout of 120000ms exceeded.
```

# Page snapshot

```yaml
- generic [ref=e1]:
  - iframe [active] [ref=e3]:
    - dialog [ref=f19e3]:
      - dialog [ref=f19e6]:
        - button "Cancel" [ref=f19e8] [cursor=pointer]
        - iframe [active] [ref=f19e12]:
          - generic [active] [ref=f20e1]:
            - banner [ref=f20e9]:
              - heading "3D Secure 2 Test Page" [level=1] [ref=f20e10]:
                - text: 3D Secure 2
                - text: Test Page
            - text: → →
            - generic [ref=f20e11]:
              - generic [ref=f20e12]:
                - heading "This is a test 3D Secure 2 authentication for a transaction with OVERNGHT.COM STREAMING." [level=3] [ref=f20e13]:
                  - text: This is a test 3D Secure 2 authentication for a transaction with
                  - strong [ref=f20e14]: OVERNGHT.COM STREAMING
                  - text: .
                - paragraph [ref=f20e15]: In live mode, customers will be asked to verify their identity with a push notification, a text message, or another method chosen by their bank.
              - generic [ref=f20e16]:
                - button "Fail" [ref=f20e18] [cursor=pointer]
                - button "Complete" [ref=f20e20] [cursor=pointer]
  - alert [ref=e4]
  - main [ref=e6]:
    - generic [ref=e7]:
      - link "Overnght" [ref=e10] [cursor=pointer]:
        - /url: /
        - img "Overnght" [ref=e12]
      - main [ref=e13]:
        - generic [ref=e22]:
          - heading "Processing your payment" [level=2] [ref=e23]
          - paragraph [ref=e24]: Hang tight — we're confirming everything with your bank
      - generic [ref=e27]:
        - generic [ref=e28]: © Overnght 2026
        - navigation [ref=e29]:
          - link "Terms of Use" [ref=e30] [cursor=pointer]:
            - /url: /legalese/termsOfService
          - link "Privacy Policy" [ref=e31] [cursor=pointer]:
            - /url: /legalese/termsOfService#privacy-policy
          - link "Contact" [ref=e32] [cursor=pointer]:
            - /url: /contact
  - region "Notifications Alt+T"
```