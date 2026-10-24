# task

**Issue**: KAN-10
**Date**: 2026-10-24
**Status**: To Do

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

### Business Rules

1. Two registration paths: coupon-based **or** product access workflow.
2. Coupon codes must be validated (accept valid / show error on invalid).
3. Review happens before final submission and must show entered details.
4. Entered details must stay accurate across the registration journey.
5. Formal requirements live on Story KAN-8; KAN-10 supplies QA environment (login URL) and credentials only.
6. Feature is web UI only — no API contract, OpenAPI, docs/, or specs/ available on branch `main`.
7. Same QA portal host and test email pattern as prior portal work (KAN-7 / KAN-6); see `testing.md` in this folder.

### Flows

1. **Entry** — Open Login at `https://webportal.qa.developercommunity.hidcloud.com/login`, then reach Create Account (exact control labels unknown).
2. **Coupon registration** — On Create Account / coupon path, enter a valid coupon, continue through registration steps, reach Review, submit.
3. **Product access registration** — On Create Account / product access path, complete the product access workflow, reach Review, submit.
4. **Invalid coupon** — Enter an invalid coupon; a validation error appears and the journey does not continue as if the code were valid.
5. **Review before submit** — Before final submission, Review shows all entered registration details; details match what was entered earlier in the journey.

### Field Constraints

- Coupon: only “valid” vs “invalid” is defined (AC4, AC5). No format, length, case, or expiry rules given.
- Invalid coupon error text: not specified (AC5 says “an appropriate validation error message”).
- Review field list: not specified (AC6 says “all entered registration details”).
- Other registration fields (name, email, password, org, etc.): not listed in Jira.
- Test email on KAN-10: `shruthi00277@gmail.com`. Password stays in Jira only — do not copy into git artifacts.

### Roles & Permissions

- Single implied actor: developer registering / signing in to the HID Developer Portal.
- No named product roles (Admin, Manager, etc.) in KAN-10 or KAN-8.

---

## Concerns & Decisions

- [#Q-001] Valid QA coupon code(s) for AC2/AC4 are still unknown — OPEN (same gap as `testing.md` Q-001 for KAN-7/KAN-6).
- [#Q-002] Product access workflow steps, fields, and success criteria for AC3 are undefined — OPEN (same gap as `testing.md` Q-002).
- [#Q-003] Review field list (AC6) and exact invalid-coupon error text (AC5) are unknown — OPEN (same gap as `testing.md` Q-003).
- [#Q-004] Login → Create Account navigation and control labels are unknown — OPEN.
- [#Q-005] Whether `shruthi00277@gmail.com` is an existing login, a registration identity, or both is unclear — OPEN.
- [#Q-006] “KAN-10 blocks KAN-8” may be intentional as a testing gate (same pattern as KAN-7 blocks KAN-6) — OPEN / nice.
- [#Q-007] Post-Review success outcome that proves “complete registration” (AC2/AC3) is not defined — OPEN.
- [#A-001] Decision: treat KAN-8 AC1–AC7 as full formal test scope; KAN-10 is env/credentials wrapper only.
- [#A-002] Decision: start every case at the QA login URL, then open Create Account.
- [#A-003] Decision: coupon and product-access paths are alternatives; both can reach Review (AC6/AC7 shared).
- [#A-004] Decision: UI-only functional coverage; no API-contract testing.
- [#A-005] Decision: until exact copy is known, “appropriate” invalid-coupon error means a visible validation message that blocks continue.
- [#A-006] Decision: use given email for login checks; prefer a unique approved address for new registration if the mailbox is already registered.
- [#D-001] KAN-10 body is login/credentials while KAN-8 ACs are registration — KAN-8 is authoritative for requirements.
- [#D-002] AC2 (end-to-end coupon registration) overlaps AC4 (mid-flow accept/continue) — test AC4 as mid-step and AC2 as full path unless product says otherwise.
- [#D-004] Living knowledge open questions (coupon / product access / Review+error) recur on KAN-10/KAN-8 with no answers yet — do not assume KAN-7 answers exist.
- [#R-001] No valid QA coupon blocks AC2/AC4 happy-path execution (High).
- [#R-002] Unspecified product access workflow blocks or forces guessing AC3 (High).
- [#R-003] Soft AC5 assertions may be flaky without exact error copy (Medium).
- [#R-004] Do not copy the Jira password into git artifacts (Medium).
- [#R-005] Same QA host/email as KAN-7 risks duplicate-email or shared-coupon collisions (Medium).
- [#R-006] Unknown post-registration side effects (email verify, entitlements) may leave test data dirty (Medium).
- [#Conflict note] No contradiction with `testing.md` — same portal, URL, email pattern, and still-open must-questions; this file is the KAN-10/KAN-8 issue capture, `testing.md` remains prior KAN-7/KAN-6 notes.
