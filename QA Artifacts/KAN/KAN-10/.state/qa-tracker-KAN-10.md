# Q&A Tracker — #KAN-10

## Meta
- **Issue**: KAN-10
- **Requirements Story**: KAN-8
- **Round**: 1 (answers received)
- **Status**: all-must-resolved — awaiting scope confirmation / GROOMING_COMPLETE
- **Updated**: 2026-10-24T11:56:13Z
- **Answer source**: Jira comment 10109

## Round 1

| ID | Type | Priority | Item | Source | Status | Answer |
|----|------|----------|------|--------|--------|--------|
| Q-001 | Question | must | What valid coupon code(s) should QA use in the QA environment to prove AC2 and AC4? | Linked: KAN-8 AC2 / AC4 | RESOLVED | Coupon code registration is out of scope for this testing activity. Testing will focus on the Create Account and Product Access workflows only. |
| Q-002 | Question | must | What are the exact steps, fields, and success criteria for the product access workflow in AC3? | Linked: KAN-8 AC3 + Description | RESOLVED | Product access workflow: Create Account → Select Product Access option → Enter required details → Review → Submit Registration. |
| Q-003 | Question | must | What fields appear on the Review page (AC6), and what is the exact on-screen text for an invalid coupon (AC5)? | Linked: KAN-8 AC5 / AC6 | RESOLVED | Review page should display all entered registration details. Invalid coupon validation is not being tested as coupon registration is out of scope. |
| Q-004 | Question | should | How does a developer go from the Login URL to the Create Account page (AC1)? What are the exact control labels? | Linked: KAN-8 AC1 + Description (KAN-10) | RESOLVED | From the Login page, click "Create Account" to start registration. |
| Q-005 | Question | should | Is shruthi00277@gmail.com an existing portal login for testing, or an identity to use when registering? | Description (KAN-10) | RESOLVED | shruthi00277@gmail.com can be used as a test account. If already registered, use a new email address. |
| Q-006 | Question | nice | Is the "KAN-10 blocks KAN-8" link intentional as a testing gate, or should KAN-10 be a child/sub-task of KAN-8? | Linked: KAN-8 Blocks relationship | RESOLVED | Relationship is intentional for testing purposes. |
| Q-007 | Question | should | After Review submission, what visible success outcome proves "complete registration" for AC2 and AC3? | Linked: KAN-8 AC2 / AC3 | RESOLVED | Successful registration is confirmed by a success message or successful account creation confirmation screen. |
| A-001 | Assumption | — | KAN-8 AC1–AC7 are the full formal test scope for KAN-10 | Linked: KAN-8 ACs; Description (KAN-10) | RESOLVED | Confirmed. (Testing activity then narrows: coupon AC2/AC4/AC5 out of scope per Q-001/Q-003.) |
| A-002 | Assumption | — | Registration is reachable from the given login host | Description (KAN-10) + Linked: KAN-8 AC1 | RESOLVED | Confirmed. |
| A-003 | Assumption | — | Coupon path and product-access path are alternatives that both can reach Review | Linked: KAN-8 Description + AC6/AC7 | RESOLVED | Confirmed (product has both paths; this testing activity covers Product Access only). |
| A-004 | Assumption | — | No API-contract testing required | Context Section 1-API | RESOLVED | Confirmed. |
| A-005 | Assumption | — | "Appropriate" invalid-coupon error means a visible validation message that blocks continue | Linked: KAN-8 AC5 | RESOLVED | Not applicable. Coupon flow is out of scope. |
| A-006 | Assumption | — | Provided email may be used for login checks; registration may need a unique address if already registered | Description (KAN-10) vs Linked: KAN-8 | RESOLVED | Confirmed. |
| R-001 | Risk | High | No valid QA coupon → AC2/AC4 happy paths blocked | Linked: KAN-8 AC2, AC4 | RESOLVED | Mitigated — coupon registration out of scope (Q-001). |
| R-002 | Risk | High | Product access workflow unspecified → AC3 guessed or blocked | Linked: KAN-8 AC3 | RESOLVED | Mitigated — workflow steps provided (Q-002). |
| R-003 | Risk | Medium | Weak/flaky AC5 if "appropriate" error is asserted without exact copy | Linked: KAN-8 AC5 | RESOLVED | Mitigated — AC5 / invalid coupon not tested (Q-003). |
| R-004 | Risk | Medium | Password in Jira Description could be copied into git artifacts | Description (KAN-10) | OPEN | Accepted — continue keeping password out of git artifacts. |
| R-005 | Risk | Medium | Same QA host/email as KAN-7 — parallel registration may collide | Knowledge: testing.md + Description (KAN-10) | RESOLVED | Mitigated — use new email if already registered (Q-005 / A-006). |
| R-006 | Risk | Medium | Unknown post-registration side effects may leave accounts/mailboxes in bad state | Linked: KAN-8 AC2/AC3 | RESOLVED | Mitigated — success = success message or account creation confirmation (Q-007); still prefer unique emails when needed. |
| R-007 | Risk | Low | Empty docs/specs/Figma → UI label drift in written cases | Context Sections 5–6 | OPEN | Accepted — discover remaining field labels on QA build; Create Account label confirmed (Q-004). |

## Round History

### Round 1
- Posted ALM Grooming Review Round 1 (comment 10108)
- Awaiting human answers to must items Q-001, Q-002, Q-003

### Resume 2026-10-24T11:48:23Z
- Trigger content was a **re-paste** of QA Agent Round 1 comment (no `Q-00N:` answers, no `GROOMING_COMPLETE`)
- No tracker Status/Answer changes; must items remain OPEN
- No Jira follow-up comment (qa-agent Step 6 — re-paste / duplicate)

### Resume 2026-10-24T11:56:13Z
- Human answers in comment 10109 — all Q-001–Q-007 and A-001–A-006 resolved
- Must items cleared → Path B (grooming scope confirmation)
- Coupon registration (AC2, AC4, AC5) out of test scope; in-scope: Create Account + Product Access (AC1, AC3, AC6, AC7)
