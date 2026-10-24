# Context: KAN-10

**Title**: task
**Type**: Task
**Status**: To Do
**Date**: 2026-10-24
**Parent Issue**: KAN-10
**Browse URL**: https://busybug027.atlassian.net/browse/KAN-10
**Project**: KAN (Agent EXP)
**Assignee**: QA Agent
**Reporter**: Main Agent (busybug027@gmail.com)
**Priority**: Medium
**Requirements source (linked Story)**: KAN-8 — dev port

---

## 1. Acceptance Criteria (Primary)

KAN-10 (this Task) has **no acceptance criteria** of its own in Jira. No AC custom field or AC section appears on the issue.

Acceptance criteria below are captured **verbatim** from linked Story **KAN-8** (KAN-10 **blocks** KAN-8). They were not invented or rephrased.

- **AC1:** Create Account page loads successfully and is accessible to users.
- **AC2:** Users can complete registration using a valid coupon code.
- **AC3:** Users can complete registration through the product access workflow.
- **AC4:** Valid coupon codes are accepted and allow users to continue the registration process.
- **AC5:** Invalid coupon codes display an appropriate validation error message.
- **AC6:** Review page displays all entered registration details before submission.
- **AC7:** Registration details entered by the user are retained and accurately displayed throughout the registration journey.

---

## 1-API. API Specification

This feature is a web UI (HID Developer Portal login / registration). No OpenAPI/Swagger file, API contract attachment, or endpoint specification was found in Jira (KAN-10 / KAN-8), `docs/`, `specs/`, or `knowledge/`.

No `context/api-spec/` files were created. Functional tests should target the portal UI flows (create account, coupon, product access, review), not undocumented HTTP APIs.

---

## 2. Description

### Triggered task (KAN-10)

| Field | Value |
|-------|-------|
| Summary | task |
| Issue type | Task |
| Status | To Do |
| Priority | Medium |
| Description (plain text from Jira) | Login URL: https://webportal.qa.developercommunity.hidcloud.com/login — mail: shruthi00277@gmail.com — password: present in Jira description only (not copied into git artifacts) |
| Labels / Components / Fix versions | None set |
| Parent / Epic | None (standalone Task — not a sub-task) |
| Attachments | None |

### Linked story narrative (KAN-8)

The HID Developer Portal enables developers to create an account and register for access using either a coupon-based registration process or a product access workflow. The registration experience should validate coupon codes, support product-based access requests, and provide a review step before final submission.

| Field | Value |
|-------|-------|
| Summary | dev port |
| Issue type | Story |
| Status | To Do |
| Priority | Medium |
| Browse | https://busybug027.atlassian.net/browse/KAN-8 |

---

## 3. Linked Items

### Blocks: KAN-8 — dev port

**Type**: Story  
**Status**: To Do  
**Priority**: Medium  
**Browse**: https://busybug027.atlassian.net/browse/KAN-8  
**Link direction**: KAN-10 **blocks** KAN-8 (outward Blocks); KAN-8 **is blocked by** KAN-10  
**Impact Assessment**: Primary formal requirements source for this testing Task. All acceptance criteria (AC1–AC7) and the feature narrative live on KAN-8. Downstream test design should cover KAN-8 registration journeys; publish/traceability may reference KAN-8 as the requirement Story while the triggered assignment remains KAN-10.  
**Relevant Details**: Two registration paths (coupon-based vs product access workflow); coupon validation (valid accepted / invalid shows error); Review page before submission; registration details retained and shown accurately throughout the journey.

No parent Epic, no other issue links, no sub-tasks, no remote links on KAN-10 or KAN-8.

---

## 4. Attachments

No attachments on KAN-10 (confirmed via `jira_download_attachments`: total 0).  
No attachments on linked KAN-8 (confirmed via `jira_download_attachments`: total 0).  
No files downloaded to `context/attachments/`.

---

## 5. Project Knowledge

| Source | File | Relevance | Key Details |
|--------|------|-----------|-------------|
| knowledge | `knowledge/KAN/features/hid-developer-portal/testing.md` | Living notes for HID Developer Portal testing (prior KAN-7 / KAN-6) | Same portal URL and test email pattern; AC areas AC1–AC7 mirror registration/coupon/product-access/review; open questions on valid coupons, product access workflow definition, review fields, and invalid coupon error copy |
| docs | *(none)* | `docs/` not present on branch `main` (sparse-checkout paths empty) | No static reverse-spec or PRD available |
| specs | *(none)* | `specs/` not present on branch `main` | No feature-spec files to auto-match |

### Feature Specs (`specs/`)

No files under `specs/` on the resolved Git Branch (`main`). No user-named spec in issue comments or the session request.

### Comment-Derived Context

| Author | Date | Insight |
|--------|------|---------|
| Main Agent | 2026-10-24T16:21:28+0530 | Comment "start QA grooming" — workflow trigger only; no requirement change |
| Main Agent | 2026-10-24T16:34:40+0530 | Comment "start QA grooming" — workflow trigger only; no requirement change |
| Main Agent | 2026-10-24T17:05:26+0530 | Comment "Start QA grooming" — workflow trigger only; no requirement change |

No named `spec:` path, no scope decisions, no AC updates in comments.

### Living knowledge extract (`hid-developer-portal`)

- Feature area folder: `knowledge/KAN/features/hid-developer-portal/`
- Environment login URL matches KAN-10 description
- Test email pattern matches KAN-10 (`shruthi00277@gmail.com`); passwords must stay in Jira only
- Prior open must-questions (from KAN-7 grooming notes): valid coupon codes; product access workflow definition; Review fields + invalid coupon error copy

---

## 6. Figma Designs

No Figma designs linked

---

## 7. Functional Setup Details

**Roles and Permissions:**
- Role implied: developer registering / signing in to the HID Developer Portal (no named product roles in Jira)

**Entities and Configuration:**
- Valid coupon code(s) required for coupon registration path (codes not provided in Jira)
- Product access workflow inputs required for the alternate path (fields/steps not specified in Jira)

**Settings and Feature States:**
- None specified in Jira, `docs/`, `specs/`, or knowledge beyond portal availability

**Plans and Subscriptions:**
- None mentioned

**Schedules and Time-Based Config:**
- None mentioned

**Navigation Starting Points:**
- Open https://webportal.qa.developercommunity.hidcloud.com/login
- From Login, reach Create Account (exact control labels unknown — confirm in grooming)
- Proceed through coupon path or product access workflow to Review before submission

**Connectivity and Hardware:**
- None mentioned (web portal only)

**Credentials (tester setup — values from Jira KAN-10 description):**
- Email: shruthi00277@gmail.com
- Password: stored only in Jira KAN-10 description — not duplicated in git artifacts

---

## 8. UI Terminology & Navigation Map

Limited sources: no Figma analysis yet (Section 6 is URL-only / none), no `docs/` or `specs/`. Derived from KAN-8 wording, KAN-10 login URL, and living knowledge.

### 8a. Screen / Page Inventory

| Screen Name | Navigation Path | Visible To |
|-------------|-----------------|------------|
| Login | Open https://webportal.qa.developercommunity.hidcloud.com/login | All (entry URL from KAN-10) |
| Create Account | From Login, click `Create Account` (Q-004 resolved) | All (per AC1) |
| Coupon registration steps | Out of scope for this testing activity (Q-001) | N/A for KAN-10 testing |
| Product access workflow steps | Create Account → Select Product Access option → Enter required details → Review → Submit Registration (Q-002) | Users on product access path (AC3) |
| Review | Before Submit Registration; shows all entered registration details (Q-003) | Users who completed prior registration steps (AC6, AC7) |
| Success / confirmation | After Submit Registration: success message or account creation confirmation screen (Q-007) | Completing registrant |

### 8b. Key UI Elements

| Element | Type | Screen | Label / Text | Interaction |
|---------|------|--------|--------------|-------------|
| Email / mail field | Field | Login | Exact label unknown | Enter text |
| Password field | Field | Login | Exact label unknown | Enter text |
| Coupon code field | Field | Coupon registration path | Exact label unknown | Enter text |
| Invalid coupon validation message | Message | Coupon registration path | Exact copy unknown (AC5) | None (displayed) |
| Review detail fields | Read-only fields | Review | Field list unknown (AC6) | None (displayed) |
| Continue / Submit controls | Button | Multiple registration steps | Exact labels unknown | Click / tap |

### 8c. Terminology Glossary

| Generic Term | Product Term | Notes |
|--------------|--------------|-------|
| Developer registration portal | HID Developer Portal / Developer Community web portal | From KAN-8 + knowledge |
| Coupon registration | coupon-based registration process | KAN-8 description |
| Product request path | product access workflow | KAN-8 description |
| Review before submit | Review page | AC6 / KAN-8 |

---

## 9. Context Summary

**Total Acceptance Criteria**: 7 (verbatim from linked Story KAN-8; KAN-10 itself has 0 AC fields)  
**Endpoints in API Spec**: N/A (UI feature; no API spec found)  
**Linked Issues Fetched**: 1 / 1 (KAN-8 via Blocks)  
**Attachments Downloaded**: 0 / 0  
**Knowledge Files Scanned**: 1 (`knowledge/KAN/features/hid-developer-portal/testing.md`); `docs/` and `specs/` absent on `main`  
**Warnings**: No AC on KAN-10 itself — requirements sourced from linked KAN-8; no Figma; no attachments; empty `docs/` and `specs/`; UI labels and coupon/product-access details incomplete for full step writing

---

## 10. Grooming Findings (requirement-grooming)

**Groomed**: 2026-10-24  
**Requirement Source**: KAN-10 (Task — environment/credentials) + Linked Story KAN-8 (AC1–AC7, feature narrative)  
**Figma PNGs reviewed**: none (no `context/figma/` images; Section 6 confirms no Figma)  
**Status**: Groomed — gaps documented; proceed with defaults below; do not block

---

### 10.1 Understanding (Capability 1)

**Summary**: A developer opens the HID Developer Portal, reaches Create Account, and finishes registration either with a valid coupon code or through a product access workflow. Before final submit, a Review page shows the details they entered, and those details stay correct as they move through the journey.

**Actors / actions / outcomes**:
| Actor | Action | Expected outcome | Side effects (stated?) |
|-------|--------|------------------|------------------------|
| Developer (implied) | Open Create Account | Page loads and is usable (AC1) | Not stated |
| Developer | Register with valid coupon | Registration completes (AC2); code accepted and journey continues (AC4) | Not stated (email, account creation, entitlements) |
| Developer | Register via product access workflow | Registration completes (AC3) | Not stated |
| Developer | Enter invalid coupon | Sees a validation error (AC5) | Not stated |
| Developer | Reach Review before submit | Sees all entered registration details (AC6); details match what was entered earlier (AC7) | Not stated |

**Restatement**: This work lets a developer create a portal account by either coupon registration or a product access path. On success, registration can finish after a Review step that shows accurate details. If the coupon is invalid, an error appears and the journey should not continue as if the code were valid. Preconditions include reaching Create Account from the QA login host in KAN-10. Downstream: KAN-8 stays blocked until KAN-10 testing completes.

**[NEEDS CLARIFICATION]** What counts as “complete registration” for AC2 and AC3 (account created, confirmation screen, email sent, or Review submit only) — **Source**: Linked item (KAN-8) AC2 / AC3 say “complete registration” with no success screen or post-submit outcome defined.

---

### 10.2 Acceptance Criteria (verbatim — no fabricated ACs)

From Linked item (KAN-8) only. KAN-10 Description has no ACs.

- **AC1:** Create Account page loads successfully and is accessible to users.
- **AC2:** Users can complete registration using a valid coupon code.
- **AC3:** Users can complete registration through the product access workflow.
- **AC4:** Valid coupon codes are accepted and allow users to continue the registration process.
- **AC5:** Invalid coupon codes display an appropriate validation error message.
- **AC6:** Review page displays all entered registration details before submission.
- **AC7:** Registration details entered by the user are retained and accurately displayed throughout the registration journey.

---

### 10.3 Complete Specification (web UI — as far as sources go)

#### Screens (from Linked item KAN-8 ACs + Description; KAN-10 Description for entry URL)

| Screen | Known from source | Unknown |
|--------|-------------------|---------|
| Login | KAN-10 Description: `https://webportal.qa.developercommunity.hidcloud.com/login` | Field labels, Create Account control |
| Create Account | AC1 | How to reach from Login; layout; required fields |
| Coupon path | AC2, AC4, AC5 | Step order; coupon field label; continue control |
| Product access workflow | AC3; KAN-8 Description: “product-based access requests” | Steps, product list, fields, success criteria |
| Review | AC6, AC7; KAN-8 Description: “review step before final submission” | Field list; edit/back behavior; submit label |

**Visual specifications**: None — no Figma, no design attachment.  
**States defined in source**: Success (load Create Account; accept valid coupon; complete either path; Review shows details). Error only for invalid coupon (AC5) — copy not given. Loading / empty / disabled / duplicate-account states not defined.  
**Validation rules**: Only “valid” vs “invalid” coupon (AC4, AC5). No format, length, case, or expiry rules. No rules for other registration fields.  
**Error messages (exact text)**:

| Scenario | Error Message |
|----------|---------------|
| Invalid coupon | **Not specified** — AC5 says “an appropriate validation error message” only |

---

### 10.4 Business Context

**Business rules** (from Linked item KAN-8 Description + ACs):
1. Two registration paths: coupon-based **or** product access workflow.
2. Coupon codes must be validated (accept valid / error on invalid).
3. Review happens before final submission and must show entered details.
4. Entered details must stay accurate across the registration journey.

**Integration points**: Not specified in KAN-10, KAN-8, docs/, or specs/. Portal host implies HID Developer Community QA environment only.  
**Compliance**: Not mentioned.

---

### 10.5 Impact Analysis (Capability 5)

| Area | Finding | Source |
|------|---------|--------|
| Affected flows | Create Account, coupon registration, product access registration, Review-before-submit | Linked item (KAN-8) Description + AC1–AC7 |
| Login vs register | KAN-10 supplies login URL + mailbox; Story ACs are registration — login may be entry only or a separate existing-account path | Description (KAN-10) vs Linked item (KAN-8) AC1–AC7 |
| Prior same-portal work | Living knowledge from KAN-7 / KAN-6 covers the same AC themes and still-open coupon / product-access / Review questions — parallel or overlapping QA risk on same QA host | Project Knowledge (`knowledge/KAN/features/hid-developer-portal/testing.md`) |
| Regression risk | Changing Create Account or shared registration steps could affect both coupon and product-access paths and any login→register CTA | Linked item (KAN-8) Description (two paths + shared Review) |
| Integration impact | No API/docs/specs — treat as UI-only; unknown backend account/email services | Description (KAN-10/KAN-8); Section 1-API |
| Net-new note | No product docs on branch; treat registration behavior as specified only by KAN-8 ACs — impact beyond those ACs is unknown | Project Knowledge (empty docs/specs) |

---

### 10.6 Dependencies (Capability 6)

| Dependency | Type | Status | Source |
|------------|------|--------|--------|
| QA portal at login URL reachable | Service / Environment | Assumed available (URL given) | Description (KAN-10): login URL |
| Valid coupon code(s) in QA | Data | **Unknown / missing** | Linked item (KAN-8) AC2, AC4 — “valid coupon code(s)” with no sample values |
| Product access workflow (products, steps, fields) | Feature / Data | **Unknown** | Linked item (KAN-8) AC3 + Description (“product access workflow”) |
| Path from Login → Create Account | UI / Navigation | **Unknown** | Linked item (KAN-8) AC1 + Description (KAN-10) only gives `/login` |
| Test mailbox / credentials | Data | Email given; password only in Jira | Description (KAN-10) |
| KAN-8 Story implementation | Feature | To Do; KAN-10 **blocks** KAN-8 | Linked item (KAN-8) link direction |
| Prior open answers from KAN-7 grooming | Cross-team / Prior QA | Still open per living knowledge | Project Knowledge (`testing.md` Open must-questions Q-001–Q-003) |
| Figma / docs / specs | Design / Spec | Not available on branch | Section 5–6; empty docs/specs |

---

### 10.7 Gaps (Capability 2)

| ID | Gap | Priority | Why it matters for testing | Recommended default | Source |
|----|-----|----------|----------------------------|---------------------|--------|
| G-001 | No sample **valid** coupon code(s) for QA | must-resolve | Cannot write/execute AC2/AC4 happy path with concrete data | Block coupon happy-path execution until a code is provided; keep scenarios sketched | Linked item (KAN-8) AC2: “valid coupon code”; AC4: “Valid coupon codes are accepted” — no values in Description or knowledge |
| G-002 | **Product access workflow** steps, fields, and success criteria undefined | must-resolve | Cannot write concrete AC3 steps or expected results | Treat as alternate path ending at same Review; mark steps TBD until clarified | Linked item (KAN-8) AC3 + Description (“product access workflow” / “product-based access requests”) with no field list |
| G-003 | Exact **invalid coupon** error text and placement unknown | must-resolve | AC5 assertion cannot be objective (“appropriate” is subjective) | Assert a visible coupon-field validation error that blocks continue; exact copy TBD | Linked item (KAN-8) AC5: “appropriate validation error message” |
| G-004 | **Review** field list (“all entered registration details”) unknown | must-resolve | Cannot assert AC6 field-by-field | Assert Review shows every field the tester entered on prior steps once those fields are known | Linked item (KAN-8) AC6 |
| G-005 | Login → **Create Account** navigation / labels unknown | should-resolve | AC1 entry path incomplete; KAN-10 only gives Login URL | Discover on live QA: look for Create Account / Sign up / Register control on Login | Linked item (KAN-8) AC1 + Description (KAN-10) URL only |
| G-006 | Registration **form fields** (name, email, password, org, etc.) not listed | should-resolve | Cannot cover data/validation dimensions or AC7 retention field list | Infer from live UI during exploratory pass; do not invent required fields in formal ACs | Linked item (KAN-8) AC6/AC7 mention “registration details” without listing them |
| G-007 | Sad/edge paths missing: duplicate email, expired coupon, empty coupon, product-access failures, submit failure | should-resolve | Only invalid coupon is an explicit sad path | Add exploratory coverage; formal cases stay AC-scoped until product answers | Linked item (KAN-8) AC5 only explicit negative; Description does not list other failures |
| G-008 | Post-submit outcome (confirmation, auto-login, email) not defined | should-resolve | “Complete registration” (AC2/AC3) end state unclear | Default: success = reaching Review and completing final submit without error, unless product defines more | Linked item (KAN-8) AC2, AC3 |
| G-009 | Role model not defined beyond implied developer | nice-to-resolve | No Admin/other-role variants to design | Single actor: developer registrant | Linked item (KAN-8) Description (“developers”); no roles in KAN-10 |
| G-010 | No loading / empty / disabled UI states specified | nice-to-resolve | State coverage thin for UI plan | Out of formal AC scope; note only if seen in exploratory | No Figma; ACs have no state matrix |

---

### 10.8 Testability (Capability 3)

| AC | Write-the-test result | Severity | Proposed testable rewrite (for clarification — not a new AC) | Source |
|----|----------------------|----------|---------------------------------------------------------------|--------|
| AC1 | Partial — “loads successfully” / “accessible” lack measurable checks (URL, title, key controls) | Reduces assertion precision | Given Login URL opened, when Create Account is opened, then Create Account URL/title loads and primary registration controls are visible and enabled | Linked item (KAN-8) AC1 |
| AC2 | **Fails** — no valid coupon; “complete registration” end state undefined | Blocks test design | Given a known-good coupon `<CODE>`, when the developer finishes all coupon-path steps and submits Review, then `<stated success outcome>` appears | Linked item (KAN-8) AC2 |
| AC3 | **Fails** — workflow undefined | Blocks test design | Given product access path steps `<list>`, when the developer completes them and submits Review, then `<stated success outcome>` appears | Linked item (KAN-8) AC3 |
| AC4 | **Fails** — no valid coupon; “continue” screen/control undefined | Blocks specific test cases | Given coupon `<CODE>`, when applied, then the next registration step `<screen>` is shown and no coupon error is visible | Linked item (KAN-8) AC4 |
| AC5 | **Fails** — “appropriate” is subjective; exact message missing | Blocks specific test cases | Given invalid coupon `<BAD>`, when applied, then message `"<exact copy>"` appears at `<location>` and continue is blocked | Linked item (KAN-8) AC5 |
| AC6 | **Fails** — “all entered registration details” list unknown | Blocks specific test cases | Given details `<field=value…>` entered earlier, when Review opens, then each `<field>` shows the same `<value>` | Linked item (KAN-8) AC6 |
| AC7 | Partial — “throughout the registration journey” does not name steps or fields | Reduces assertion precision | Given details entered on step N, when moving to steps N+1…Review, then those values still match without re-entry | Linked item (KAN-8) AC7 |

**[NEEDS CLARIFICATION]** Exact invalid-coupon message text and Review field list — without these, AC5 and AC6 cannot be asserted character-for-character. **Source**: Linked item (KAN-8) AC5, AC6.

---

### 10.9 Discrepancies (Capability 4)

| ID | What conflicts | Severity | Recommendation | Source |
|----|----------------|----------|----------------|--------|
| D-001 | KAN-10 Description is login URL + credentials; KAN-8 ACs are create-account / coupon / product-access / Review — task body does not restate registration scope | Important | Treat KAN-8 as authoritative requirements; KAN-10 as environment + assignment wrapper | Description (KAN-10) vs Linked item (KAN-8) AC1–AC7 |
| D-002 | AC2 (“complete registration using a valid coupon”) overlaps AC4 (“valid coupon codes are accepted and allow users to continue”) — unclear if AC4 is mid-flow only and AC2 is end-to-end | Important | Test AC4 as mid-step accept/continue; AC2 as full path to completion; confirm with product if both needed | Linked item (KAN-8) AC2 vs AC4 |
| D-003 | KAN-10 **blocks** KAN-8 (testing Task blocks Story) — unusual vs parent/child; same pattern as prior KAN-7 blocks KAN-6 in living knowledge | Minor | Keep link as testing gate; trace Requirement_ID to KAN-8 | Linked item (KAN-8) link; Project Knowledge (`testing.md` Issues KAN-7/KAN-6) |
| D-004 | Living knowledge open questions still list valid coupon / product access / Review+error copy — same gaps recur on KAN-10/KAN-8 with no answers yet | Important | Re-ask as Q-001–Q-003 on this ticket; do not assume KAN-7 answers exist | Project Knowledge (`testing.md` Open must-questions) vs Linked item (KAN-8) AC2–AC6 |
| D-005 | No Figma vs ACs that imply multi-screen journey — nothing to visually cross-check | Minor (expected) | No design discrepancy to flag; UI labels remain discovery items | Section 6 Figma; Linked item (KAN-8) AC1–AC7 |

---

### 10.10 Risks (Capability 7)

| ID | Risk | Category | Severity | Mitigation | Source |
|----|------|----------|----------|------------|--------|
| R-001 | No valid QA coupon → AC2/AC4 happy paths blocked | Testability | High | Obtain code from product/ops before execution; keep cases drafted | Linked item (KAN-8) AC2, AC4 |
| R-002 | Product access workflow unspecified → AC3 guessed or blocked | Testability | High | Get step/field/success definition before case design finalization | Linked item (KAN-8) AC3 |
| R-003 | Weak/flaky AC5 if “appropriate” error is asserted without exact copy | Testability | Medium | Lock exact message text; until then assert presence of blocking validation only | Linked item (KAN-8) AC5 |
| R-004 | Password in Jira Description could be copied into git artifacts | Security / Data | Medium | Keep password only in Jira (already practiced in context bundle) | Description (KAN-10) credentials note |
| R-005 | Same QA host/email pattern as KAN-7 — parallel registration may collide (duplicate email, shared coupons) | Data / Regression | Medium | Coordinate test data with any KAN-7 runs; prefer unique emails if registration creates accounts | Project Knowledge (`testing.md` Environment) + Description (KAN-10) same email |
| R-006 | Unknown post-registration side effects (email verify, entitlements) may leave accounts or mailboxes in bad state | Blast radius / Data | Medium | Prefer disposable or approved test mailboxes; document cleanup if product provides it | Linked item (KAN-8) AC2/AC3 “complete registration” without side-effect rules |
| R-007 | Empty docs/specs/Figma → UI label drift and incomplete navigation in written cases | Testability | Low | Discover labels on QA build; update knowledge after first pass | Section 5–6; Project Knowledge |

---

### 10.11 Edge Cases & Boundaries (from gap sweep — not new ACs)

- Empty coupon submitted — **Source**: Inverse of Linked item (KAN-8) AC4/AC5 (valid/invalid named; empty not named)
- Expired or already-redeemed coupon — **Source**: Inverse of Linked item (KAN-8) AC2/AC4 “valid coupon”
- Case sensitivity / whitespace in coupon — **Source**: Linked item (KAN-8) AC4/AC5 without format rules
- Switching between coupon path and product access mid-journey — **Source**: Linked item (KAN-8) Description (“either … or”) — exclusivity not stated
- Back navigation from Review then return — data still accurate — **Source**: Linked item (KAN-8) AC7
- Double-submit on final Review — **Source**: Implicit concurrency; not in ACs
- Already-registered email using KAN-10 mailbox — **Source**: Description (KAN-10) credentials vs Linked item (KAN-8) create-account ACs

---

### 10.12 Assumptions (Capability 8 support)

| # | Assumption | Default We'll Use | Source | Rationale |
|---|------------|-------------------|--------|-----------|
| A-001 | KAN-8 AC1–AC7 are the full formal test scope for KAN-10 | Design all functional coverage from KAN-8 ACs; KAN-10 supplies env/credentials only | Linked item (KAN-8) ACs; Description (KAN-10) has no ACs | Same pattern as prior Task/Story pairing in living knowledge |
| A-002 | Registration is reachable from the given login host | Start every case at `https://webportal.qa.developercommunity.hidcloud.com/login` then open Create Account | Description (KAN-10) URL + Linked item (KAN-8) AC1 | Only entry URL provided |
| A-003 | Coupon path and product-access path are alternatives that both can reach Review | Separate scenario groups per path; both include Review (AC6) and retention (AC7) | Linked item (KAN-8) Description (“either … or”) + AC6/AC7 | Description frames two ways to register; Review is shared language |
| A-004 | No API-contract testing required | UI-only functional tests | Section 1-API; no OpenAPI in Jira/docs/specs | No API source exists |
| A-005 | “Appropriate” invalid-coupon error means a visible validation message that blocks continue | Soft assert on visible error + blocked continue until exact copy is known | Linked item (KAN-8) AC5 | Allows partial coverage without inventing copy |
| A-006 | Provided email may be used for login checks; registration may need a unique address if the mailbox is already registered | Prefer login with given email for Login-only checks; for new registration use a unique approved address when product confirms | Description (KAN-10) vs Linked item (KAN-8) AC1–AC3 | Avoid false failures on duplicate account |

**[NEEDS CLARIFICATION]** Whether `shruthi00277@gmail.com` is an existing login account, a registration identity, or both — **Source**: Description (KAN-10) credentials on Login URL while Linked item (KAN-8) ACs describe Create Account / registration.

---

### 10.13 Open Questions

| # | Question | Priority | Status | Answer (2026-10-24 comment 10109) | Source & Reason |
|---|----------|----------|--------|-----------------------------------|-----------------|
| Q-001 | What valid coupon code(s) should QA use in the QA environment to prove AC2 and AC4? | must | RESOLVED | Coupon code registration is **out of scope** for this testing activity. Focus on Create Account and Product Access workflows only. | Linked item (KAN-8) AC2 / AC4 |
| Q-002 | What are the exact steps, fields, and success criteria for the product access workflow in AC3? | must | RESOLVED | Create Account → Select Product Access option → Enter required details → Review → Submit Registration. | Linked item (KAN-8) AC3 |
| Q-003 | What fields appear on the Review page (AC6), and what is the exact on-screen text for an invalid coupon (AC5)? | must | RESOLVED | Review displays all entered registration details. Invalid coupon validation **not tested** (coupon out of scope). | Linked item (KAN-8) AC5 / AC6 |
| Q-004 | How does a developer go from the Login URL to the Create Account page (AC1)? What are the exact control labels? | should | RESOLVED | From the Login page, click **Create Account** to start registration. | Linked item (KAN-8) AC1 + Description (KAN-10) |
| Q-005 | Is `shruthi00277@gmail.com` an existing portal login for testing, or an identity to use when registering? | should | RESOLVED | Can be used as a test account. If already registered, use a new email address. | Description (KAN-10) |
| Q-006 | Is the “KAN-10 blocks KAN-8” link intentional as a testing gate, or should KAN-10 be a child/sub-task of KAN-8? | nice | RESOLVED | Relationship is intentional for testing purposes. | Linked item (KAN-8) |
| Q-007 | After Review submission, what visible success outcome proves “complete registration” for AC2 and AC3? | should | RESOLVED | Success message or successful account creation confirmation screen. | Linked item (KAN-8) AC2 / AC3 |

---

### 10.15 Resolved Clarifications & Test Scope (human Round 1 answers)

**In scope for this testing activity**
- **AC1** — Create Account page loads and is accessible (entry: Login → click `Create Account`)
- **AC3** — Product access registration: Create Account → Select Product Access option → Enter required details → Review → Submit Registration
- **AC6** — Review shows all entered registration details before submission
- **AC7** — Registration details retained and accurately displayed throughout the journey
- Success for complete registration: success message **or** account creation confirmation screen

**Out of scope for this testing activity**
- Coupon code registration (**AC2**, **AC4**)
- Invalid coupon validation (**AC5**)

**Confirmed assumptions**
- A-001 Confirmed (formal ACs from KAN-8; testing activity then excludes coupon per Q-001)
- A-002 Confirmed — start at QA login URL
- A-003 Confirmed — both product paths exist; this activity tests Product Access only
- A-004 Confirmed — UI-only
- A-005 N/A — coupon out of scope
- A-006 Confirmed — use given email; new email if already registered

**UI / navigation updates**
- Login → `Create Account` control (exact label confirmed)
- Product Access option on Create Account path
- Review before Submit Registration

---

### 10.14 Attachments & References

- https://busybug027.atlassian.net/browse/KAN-10 — triggered Task (env/credentials)
- https://busybug027.atlassian.net/browse/KAN-8 — requirements Story (AC1–AC7)
- https://webportal.qa.developercommunity.hidcloud.com/login — QA Login entry
- `knowledge/KAN/features/hid-developer-portal/testing.md` — prior portal testing notes (KAN-7/KAN-6)
- Figma: none
- Attachments: none
- docs/ / specs/: none on branch `main`
