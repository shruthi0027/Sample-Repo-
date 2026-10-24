# task

**Issue**: KAN-10
**Date**: 2026-10-24
**Status**: To Do (grooming — awaiting GROOMING_COMPLETE)

---

## Specification

### Acceptance Criteria

KAN-10 (this Task) has no acceptance criteria of its own in Jira. Acceptance criteria below are captured verbatim from linked Story **KAN-8** (KAN-10 **blocks** KAN-8).

- **AC1:** Create Account page loads successfully and is accessible to users.
- **AC2:** Users can complete registration using a valid coupon code.
- **AC3:** Users can complete registration through the product access workflow.
- **AC4:** Valid coupon codes are accepted and allow users to continue the registration process.
- **AC5:** Invalid coupon codes display an appropriate validation error message.
- **AC6:** Review page displays all entered registration details before submission.
- **AC7:** Registration details entered by the user are retained and accurately displayed throughout the registration journey.

### Testing scope (human Round 1 — 2026-10-24)

| AC | In this testing activity? |
|----|---------------------------|
| AC1 | Yes — Create Account |
| AC2 | No — coupon out of scope |
| AC3 | Yes — Product Access workflow |
| AC4 | No — coupon out of scope |
| AC5 | No — coupon out of scope |
| AC6 | Yes — Review shows entered details |
| AC7 | Yes — details retained across journey |

### Business Rules

1. Product has two registration paths (coupon **or** product access); **this testing activity covers Product Access only**.
2. Review happens before final submission and must show all entered registration details.
3. Entered details must stay accurate across the registration journey.
4. Successful registration is confirmed by a success message or account creation confirmation screen.
5. Formal requirements live on Story KAN-8; KAN-10 supplies QA environment (login URL) and credentials; Blocks link is intentional for testing.
6. Feature is web UI only — no API-contract testing.
7. Test email `shruthi00277@gmail.com` may be used; if already registered, use a new email. Password stays in Jira only.

### Flows

1. **Entry** — Open Login at `https://webportal.qa.developercommunity.hidcloud.com/login`, click **Create Account**.
2. **Product access registration** — Create Account → Select Product Access option → Enter required details → Review → Submit Registration → success message or confirmation screen.
3. **Review before submit** — Review shows all entered registration details; details match earlier steps (AC6/AC7).
4. **Coupon registration** — Out of scope for KAN-10 testing activity.

### Field Constraints

- Review: display all entered registration details (exact field list discovered on live QA; assert parity with what was entered).
- Product Access “required details”: not individually named — discover on live UI during design/execution.
- Coupon / invalid-coupon copy: not applicable for this activity.
- Test email: `shruthi00277@gmail.com` (or a new address if already registered).

### Roles & Permissions

- Single implied actor: developer registering / signing in to the HID Developer Portal.

---

## Concerns & Decisions

- [#Q-001] RESOLVED — Coupon registration out of scope; focus Create Account + Product Access.
- [#Q-002] RESOLVED — Flow: Create Account → Select Product Access → Enter required details → Review → Submit Registration.
- [#Q-003] RESOLVED — Review shows all entered details; invalid coupon not tested.
- [#Q-004] RESOLVED — Login → click `Create Account`.
- [#Q-005] RESOLVED — Given email usable as test account; new email if already registered.
- [#Q-006] RESOLVED — KAN-10 blocks KAN-8 is intentional for testing.
- [#Q-007] RESOLVED — Success = success message or account creation confirmation screen.
- [#A-001] Confirmed (then narrowed by Q-001 for execution scope).
- [#A-002] Confirmed.
- [#A-003] Confirmed (both paths exist; test Product Access only).
- [#A-004] Confirmed — UI-only.
- [#A-005] N/A — coupon out of scope.
- [#A-006] Confirmed.
- [#R-001] Mitigated — coupon out of scope.
- [#R-002] Mitigated — workflow defined.
- [#R-003] Mitigated — AC5 not tested.
- [#R-004] Accepted — keep password out of git.
- [#R-005] Mitigated — new email if needed.
- [#R-007] Accepted — discover remaining labels on QA build.
