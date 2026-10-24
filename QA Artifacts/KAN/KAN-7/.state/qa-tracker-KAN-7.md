# Q&A Tracker: KAN-7

## Meta
- **Issue**: KAN-7
- **Requirements Story**: KAN-6
- **Round**: 1
- **Status**: awaiting-human
- **Updated**: 2026-10-24T10:36:00Z

## Questions
| ID | Priority | Status | Question | Source & Reason | Answer |
|----|----------|--------|----------|-----------------|--------|
| Q-001 | must | OPEN | What valid coupon code(s) should QA use in the QA environment for AC2/AC4? | **[KAN-6 AC2/AC4]**: "valid coupon code" / "Valid coupon codes are accepted" — cannot execute happy-path coupon registration without a known-good code | |
| Q-002 | must | OPEN | What are the exact steps, fields, and success criteria for the **product access workflow** (AC3)? | **[KAN-6 AC3]**: "product access workflow" — path/fields/success not specified beyond the name | |
| Q-003 | must | OPEN | What fields appear on the **Review** page (AC6), and what is the exact **invalid coupon** error text (AC5)? | **[KAN-6 AC5/AC6]**: error message and review field list are not specified — cannot assert pass/fail objectively | |
| Q-004 | should | OPEN | How does a user navigate from the login URL to the **Create Account** page (AC1)? Exact control labels? | **[KAN-6 AC1]** + **[KAN-7 URL]**: only `/login` URL provided — Create Account entry path unknown | |
| Q-005 | should | OPEN | Is `shruthi00277@gmail.com` an existing portal account for login testing, or only for use after registration? | **[KAN-7 description]**: credentials on login URL — relationship to registration ACs unclear | |
| Q-006 | could | OPEN | Is the "KAN-7 blocks KAN-6" link intentional (testing gate), or should KAN-7 be a sub-task/child of KAN-6? | **[Issue link]**: Blocks relationship is unusual for a pure test assignment | |

## Assumptions
| ID | Priority | Status | Assumption | Default if unconfirmed | Answer |
|----|----------|--------|------------|------------------------|--------|
| A-001 | must | OPEN | KAN-6 AC1–AC7 define the full test scope for KAN-7 | Proceed treating KAN-6 as the requirements parent for design/execution | |
| A-002 | should | OPEN | Registration is reachable from the provided login URL (create-account CTA or equivalent on that host) | Use https://webportal.qa.developercommunity.hidcloud.com/login as the only entry URL | |
| A-003 | should | OPEN | Coupon path and product-access path are alternative registration journeys sharing the Review step | Design separate scenario groups per path, both ending at Review/submit | |
| A-004 | could | OPEN | No API-contract testing is required for this story | UI-only functional coverage unless an API spec is provided later | |

## Risks
| ID | Priority | Status | Risk | Impact | Answer |
|----|----------|--------|------|--------|--------|
| R-001 | must | OPEN | No valid coupon available in QA | Blocks AC2/AC4 automation and manual happy path | |
| R-002 | must | OPEN | Product access workflow unspecified | AC3 scenarios will be guessed or blocked | |
| R-003 | should | OPEN | Invalid-coupon copy unknown | AC5 assertions may be weak or flaky | |
| R-004 | should | OPEN | Password committed risk if copied from Jira into git | Credentials kept out of artifacts; still visible in Jira | |
| R-005 | could | OPEN | Empty `docs/`/`specs/`/`knowledge/` for this portal | UI labels and navigation may be incomplete until Figma/docs appear | |

## Round History
### Round 1
- Context gathered from KAN-7 + linked Story KAN-6
- Figma analysis skipped (no URLs)
- Posted ALM Round 1 comment on KAN-7
- Awaiting human answers
