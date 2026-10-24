# Web Test Plan — HID Developer Portal Product Access Registration

**Feature**: HID Developer Portal — Create Account and Product Access registration  
**Date**: 2026-10-24  
**Source**: `QA Artifacts/KAN/KAN-10/context/context-KAN-10.md` (groomed; §10.15 scope) + `knowledge/KAN/features/hid-developer-portal/`  
**Requirement Story**: KAN-8 — dev port  
**Testing Task**: KAN-10  
**Platform**: Web UI only (no API tests)  
**Figma**: None — UI inventory from context Section 8 + resolved clarifications §10.15

---

## 1. Scope Summary

**Primary Pages/Components**:
- Create Account — page loads and is reachable from Login via `Create Account` (AC1)
- Product Access option — path selection after Create Account (AC3)
- Product Access required-details form — enter registration details (AC3, AC7)
- Review — shows all entered registration details before submit (AC6, AC7)
- Success / confirmation — success message or account creation confirmation after `Submit Registration` (AC3)

**Supporting Pages** (flow-only coverage):
- Login — entry only at `https://webportal.qa.developercommunity.hidcloud.com/login`; click `Create Account` to start (Q-004)

**Out of Scope**:
- Coupon code registration path (AC2, AC4) — human grooming: coupon out of scope
- Invalid coupon validation (AC5) — human grooming: not tested
- API / HTTP contract testing — UI-only (A-004 confirmed)
- Security, performance, accessibility, device compatibility, network throttling — excluded by test-style
- Pixel-level visual checks and Figma visual alignment — no Figma designs available
- Login as a full authenticated journey beyond using Login as the registration entry point

---

## 2. AC Inventory

| AC | Criterion Text | In Scope? | Roles | Actions | Expected Outcomes | Mapped Surfaces |
|----|---------------|-----------|-------|---------|-------------------|-----------------|
| AC1 | Create Account page loads successfully and is accessible to users. | Yes | Developer (registrant) | Open Login URL; click `Create Account` | Create Account page loads; primary registration controls are visible and usable | Login → Create Account navigation; Create Account load/accessibility |
| AC2 | Users can complete registration using a valid coupon code. | **No** | — | — | — | Excluded — coupon path out of scope (§10.15 / Q-001) |
| AC3 | Users can complete registration through the product access workflow. | Yes | Developer (registrant) | Select Product Access → enter required details → Review → `Submit Registration` | Registration completes; success message or account creation confirmation screen | Product Access end-to-end flow; details form; submit; success screen |
| AC4 | Valid coupon codes are accepted and allow users to continue the registration process. | **No** | — | — | — | Excluded — coupon path out of scope (§10.15 / Q-001) |
| AC5 | Invalid coupon codes display an appropriate validation error message. | **No** | — | — | — | Excluded — coupon validation not tested (§10.15 / Q-003) |
| AC6 | Review page displays all entered registration details before submission. | Yes | Developer (registrant) | Reach Review after entering Product Access details | Review shows every detail entered on prior steps before submit | Review display surface; pre-submit detail parity |
| AC7 | Registration details entered by the user are retained and accurately displayed throughout the registration journey. | Yes | Developer (registrant) | Enter details; move through Product Access steps to Review (and back if UI allows) | Entered values stay correct across steps without unexpected loss | Retention across Product Access → Review; back-navigation retention if available |

---

## 3. Role Matrix

| Role | Positive Actions (CAN do) | Negative Actions (CANNOT do) |
|------|--------------------------|------------------------------|
| Developer (registrant) | Open Login; click `Create Account`; select Product Access option; enter required registration details; view Review details; submit registration; see success / confirmation | Complete coupon registration (out of scope for this activity — path may exist but is not tested); no Admin or other named portal roles are defined |

**Notes**:
- Single implied actor only (G-009 / knowledge). No multi-role permission matrix to expand.
- Role-based access guideline is lightly applicable (single role happy path only).

---

## 4. Entity/Inventory Combinations

| Entity Type | Instances/Types | Interactions With | Combination Coverage Needed |
|-------------|-----------------|-------------------|----------------------------|
| Registration path | Product Access (in scope); Coupon (out of scope) | Create Account entry; Review; Submit | Test Product Access only; do not plan coupon combinations |
| Registrant identity | Test email `shruthi00277@gmail.com`; alternate new email if already registered | Create Account / required details | Happy path with given email; alternate new email when mailbox is already registered (Q-005 / A-006) |
| Registration details | Required fields on Product Access path (exact labels discovered on live QA) | Review display; retention across steps | Each entered field value must appear correctly on Review (AC6) and remain accurate across the journey (AC7) |
| Registration outcome | Success message **or** account creation confirmation screen | Submit Registration | Assert either visible success outcome after submit (Q-007) |

**Notes**:
- Exact Product Access field list is not named in Jira — discover on live QA during scenario/case design; assert parity with whatever was entered (G-006 / Q-003 resolved for Review: show all entered details).
- Coupon entity and invalid-coupon messages are out of scope — no coupon codes required for this plan.
- No capacity / quota limits documented.

---

## 5. Page & Component Inventory

UI from context Section 8 + §10.15. No Figma PNGs — labels marked unknown remain discovery items on live QA; confirmed labels use backticks.

| Page/Component | Elements | States | Form Fields | Navigation Path |
|----------------|----------|--------|-------------|-----------------|
| Login | `Create Account` control (confirmed); Email / mail field; Password field (labels may vary) | Default (signed-out entry) | Email; Password (Login-only — not the registration focus) | Open `https://webportal.qa.developercommunity.hidcloud.com/login` |
| Create Account | Primary registration controls; Product Access option (path choice) | Loaded / accessible (AC1); ready for path selection | Path/option selection for Product Access (exact control type TBD on live UI) | Login → click `Create Account` |
| Product Access — required details | Continue / next control(s) (exact labels TBD); required detail inputs | Empty; filled; validation-blocked if required fields empty (if shown on live UI) | Required registration details for Product Access (exact field set TBD on live QA) | Create Account → Select Product Access option → Enter required details |
| Review | Read-only display of entered registration details; `Submit Registration` (confirmed outcome control from grooming) | Populated with prior-step values before submit | None editable for display assertion — shows all entered details | After required details → Review |
| Success / confirmation | Success message **or** account creation confirmation screen content | Success after submit | None | After `Submit Registration` |

**Excluded from inventory (out of scope)**:
- Coupon registration steps, coupon code field, invalid coupon validation message

---

## 6. Flow Inventory

| Flow | Steps | Entry Point | Completion | Roles |
|------|-------|-------------|------------|-------|
| F-01 Create Account access (AC1) | Open Login URL → click `Create Account` → Create Account loads with usable primary controls | `https://webportal.qa.developercommunity.hidcloud.com/login` | Create Account page is loaded and accessible | Developer (registrant) |
| F-02 Product Access registration happy path (AC3) | Login → `Create Account` → Select Product Access option → Enter required details → Review → `Submit Registration` → success message or confirmation screen | Login URL | Success message **or** account creation confirmation screen | Developer (registrant) |
| F-03 Review details before submit (AC6) | Complete Product Access details → land on Review → check all entered details are shown before submit | Same entry as F-02 through required details | Review displays all entered registration details | Developer (registrant) |
| F-04 Detail retention across journey (AC7) | Enter required details → move forward to Review (and back then forward if UI allows) → confirm values still match | Same entry as F-02 | Values retained and accurately displayed through to Review | Developer (registrant) |

**Abandonment / variation notes** (for later scenario depth; still AC-tied):
- Leave mid-flow before Review — not required by ACs; optional exploratory only
- Already-registered email — use a new email (Q-005); surface under F-02 data variation
- Coupon path branching — out of scope; do not design flows for AC2/AC4/AC5

---

## 7. Coverage Area Mapping

| AC/Surface | Applicable Guidelines |
|-----------|----------------------|
| AC1 — Create Account load via Login → `Create Account` | userstory_acceptance, functional_workflow, navigation_interaction, interaction_behaviour |
| AC3 — Product Access end-to-end (select → details → Review → Submit → success) | userstory_acceptance, functional_workflow, workflow_business_logic, form_input_validation, interaction_behaviour, navigation_interaction, notification (success message / confirmation), data_consistency |
| AC3 — Product Access required-details form | userstory_acceptance, form_input_validation, field_data_validation (as field rules appear on live UI), interaction_behaviour |
| AC6 — Review shows all entered details | userstory_acceptance, functional_workflow, data_consistency, ui_error_state (populated Review state) |
| AC7 — Retention across Product Access → Review | userstory_acceptance, workflow_business_logic, data_consistency, navigation_interaction |
| F-02 success outcome (message or confirmation) | userstory_acceptance, notification, functional_workflow |
| Role — single Developer registrant | userstory_acceptance (no multi-role RBAC expansion) |

**Not mapped (by design)**:
- AC2, AC4, AC5 surfaces — out of scope
- ui_ux_visual_figma — no Figma; skip visual guideline surfaces
- security_session_management — no authenticated-session ACs in scope; exclude standalone security scenarios per test-style
- Coupon form validation / field_data_validation for coupon — excluded

---

## 8. Risk Assessment

| Page/Flow | Business Impact | Complexity | Frequency | Priority |
|-----------|----------------|------------|-----------|----------|
| F-02 Product Access registration happy path (AC3) | Developers cannot finish Product Access registration; portal onboarding blocked | Multi-step wizard; unknown field set until live discovery; unique email handling | Primary registration path for this activity | Critical |
| F-01 Create Account access (AC1) | Registration never starts if Create Account is unreachable | Low — single navigation hop | Every new registrant | Critical |
| F-03 Review details (AC6) | Wrong details submitted; trust / data accuracy failure before account creation | Medium — depends on live field list | Every successful Product Access attempt | High |
| F-04 Detail retention (AC7) | Data loss mid-journey forces re-entry or wrong submit | Medium — multi-step state | Every multi-step registration | High |
| Product Access required-details form validation | Incomplete or wrong data reaches Review | Medium — field rules TBD on live UI | Every registrant on this path | Medium |
| Success / confirmation visibility | Ambiguous “complete registration” if neither success message nor confirmation appears | Low — outcome check only | End of every happy path | High |
| Duplicate / already-registered email | False failure if `shruthi00277@gmail.com` is already registered | Low — data prep | Occasional | Medium |

---

## 9. Test Data & Environment

| Data / Resource | Type | Details |
|----------------|------|---------|
| QA Login URL | Environment | `https://webportal.qa.developercommunity.hidcloud.com/login` |
| Test email | Prerequisite | `shruthi00277@gmail.com` — use for registration; if already registered, use a new email address |
| Password | Prerequisite | Stored only in Jira KAN-10 description — do not copy into git artifacts |
| Product Access required details | Dynamic | Enter realistic values for whatever required fields appear on the live Product Access form; record them for Review assertions |
| Coupon codes | N/A | Not required — coupon path out of scope |
| Roles | Prerequisite | Developer (registrant) — unauthenticated visitor starting from Login |

**Environment Prerequisites**:
- QA HID Developer Community web portal reachable at the Login URL above
- Browser UI testing only — no API tools or contract checks
- No Figma comparison assets — do not block on design screenshots
- Prefer a fresh or known-unused email when Create Account rejects an already-registered address
- Traceability: Requirement_ID for published cases = KAN-8 (Story); testing assignment = KAN-10

---

## 10. Planning Notes (for scenario / case design)

1. **In-scope AC set only**: AC1, AC3, AC6, AC7. Do not generate scenarios or cases for AC2, AC4, or AC5.
2. **Canonical flow** (Q-002): Login → click `Create Account` → Select Product Access option → Enter required details → Review → `Submit Registration` → success message or confirmation screen.
3. **UI labels**: Use confirmed labels (`Create Account`, Product Access option, `Submit Registration`). Discover remaining field labels on live QA; do not invent coupon-related labels.
4. **Success assertion** (Q-007): After submit, the Developer sees a success message **or** an account creation confirmation screen.
5. **Review assertion** (AC6/AC7): Compare Review content to the exact values entered on the Product Access details step(s).
6. **Depth**: Critical/High surfaces → full expansion in scenario design; Medium → standard.
)
