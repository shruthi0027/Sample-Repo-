# Q&A Tracker — #KAN-10

## Meta
- **Issue**: KAN-10
- **Requirements Story**: KAN-8
- **Round**: 1
- **Status**: awaiting-human
- **Updated**: 2026-10-24T11:48:23Z

## Round 1

| ID | Type | Priority | Item | Source | Status | Answer |
|----|------|----------|------|--------|--------|--------|
| Q-001 | Question | must | What valid coupon code(s) should QA use in the QA environment to prove AC2 and AC4? | Linked: KAN-8 AC2 / AC4 | OPEN | — |
| Q-002 | Question | must | What are the exact steps, fields, and success criteria for the product access workflow in AC3? | Linked: KAN-8 AC3 + Description | OPEN | — |
| Q-003 | Question | must | What fields appear on the Review page (AC6), and what is the exact on-screen text for an invalid coupon (AC5)? | Linked: KAN-8 AC5 / AC6 | OPEN | — |
| Q-004 | Question | should | How does a developer go from the Login URL to the Create Account page (AC1)? What are the exact control labels? | Linked: KAN-8 AC1 + Description (KAN-10) | OPEN | — |
| Q-005 | Question | should | Is shruthi00277@gmail.com an existing portal login for testing, or an identity to use when registering? | Description (KAN-10) | OPEN | — |
| Q-006 | Question | nice | Is the "KAN-10 blocks KAN-8" link intentional as a testing gate, or should KAN-10 be a child/sub-task of KAN-8? | Linked: KAN-8 Blocks relationship | OPEN | — |
| Q-007 | Question | should | After Review submission, what visible success outcome proves "complete registration" for AC2 and AC3? | Linked: KAN-8 AC2 / AC3 | OPEN | — |
| A-001 | Assumption | — | KAN-8 AC1–AC7 are the full formal test scope for KAN-10 (default: design coverage from KAN-8 ACs; KAN-10 supplies env/credentials only) | Linked: KAN-8 ACs; Description (KAN-10) | PENDING | — |
| A-002 | Assumption | — | Registration is reachable from the given login host (default: start at the QA login URL then open Create Account) | Description (KAN-10) + Linked: KAN-8 AC1 | PENDING | — |
| A-003 | Assumption | — | Coupon path and product-access path are alternatives that both can reach Review (default: separate scenario groups; both include Review and retention) | Linked: KAN-8 Description + AC6/AC7 | PENDING | — |
| A-004 | Assumption | — | No API-contract testing required (default: UI-only functional tests) | Context Section 1-API | PENDING | — |
| A-005 | Assumption | — | "Appropriate" invalid-coupon error means a visible validation message that blocks continue (default: soft assert until exact copy known) | Linked: KAN-8 AC5 | PENDING | — |
| A-006 | Assumption | — | Provided email may be used for login checks; registration may need a unique address if already registered (default: unique approved address for new registration when confirmed) | Description (KAN-10) vs Linked: KAN-8 | PENDING | — |
| R-001 | Risk | High | No valid QA coupon → AC2/AC4 happy paths blocked | Linked: KAN-8 AC2, AC4 | OPEN | — |
| R-002 | Risk | High | Product access workflow unspecified → AC3 guessed or blocked | Linked: KAN-8 AC3 | OPEN | — |
| R-003 | Risk | Medium | Weak/flaky AC5 if "appropriate" error is asserted without exact copy | Linked: KAN-8 AC5 | OPEN | — |
| R-004 | Risk | Medium | Password in Jira Description could be copied into git artifacts | Description (KAN-10) | OPEN | — |
| R-005 | Risk | Medium | Same QA host/email as KAN-7 — parallel registration may collide | Knowledge: testing.md + Description (KAN-10) | OPEN | — |
| R-006 | Risk | Medium | Unknown post-registration side effects may leave accounts/mailboxes in bad state | Linked: KAN-8 AC2/AC3 | OPEN | — |
| R-007 | Risk | Low | Empty docs/specs/Figma → UI label drift in written cases | Context Sections 5–6 | OPEN | — |

## Round History

### Round 1
- Posted ALM Grooming Review Round 1 (comment 10108)
- Awaiting human answers to must items Q-001, Q-002, Q-003

### Resume 2026-10-24T11:48:23Z
- Trigger content was a **re-paste** of QA Agent Round 1 comment (no `Q-00N:` answers, no `GROOMING_COMPLETE`)
- No tracker Status/Answer changes; must items remain OPEN
- No Jira follow-up comment (qa-agent Step 6 — re-paste / duplicate)
