# Test Scenarios — HID Developer Portal Product Access Registration

**Feature**: HID Developer Portal — Create Account and Product Access registration  
**Date**: 2026-10-24  
**Source Plan**: `QA Artifacts/KAN/KAN-10/functional/test-plan-KAN-10.md`  
**Requirement Story**: KAN-8 — dev port  
**Testing Task**: KAN-10  
**Total Scenarios**: 38  
**Scope**: AC1, AC3, AC6, AC7 only — coupon registration (AC2, AC4, AC5) excluded

---

## 1. Summary

| Metric | Count |
|--------|-------|
| Total Scenarios | 38 |
| Critical Priority | 10 |
| High Priority | 20 |
| Medium Priority | 8 |
| Low Priority | 0 |

**In-scope ACs**: AC1, AC3, AC6, AC7  
**Out of scope (no scenarios)**: AC2, AC4, AC5 (coupon registration and invalid coupon validation)

---

## 2. Scenarios by Page/Feature

### [Web - Create Account]

| # | Scenario Title | Requirement | Source | Category | Priority | Guideline Source |
|---|---------------|-------------|--------|----------|----------|------------------|
| 1 | SC-CA-01 — Verify Create Account page loads with usable primary registration controls after the Developer clicks `Create Account` on Login | AC1 | AC #1 + Linked item (KAN-8) + Description (KAN-10) | Positive | Critical | userstory_acceptance_coverage |
| 2 | SC-CA-02 — Verify Login stays on the Login screen and does not show Create Account primary registration controls when the Developer has not clicked `Create Account` | AC1 | AC #1 | Negative | High | userstory_acceptance_coverage |
| 3 | SC-CA-03 — Verify `Create Account` on Login opens Create Account when clicked once | AC1 | AC #1 + Description (KAN-10) | Positive | Critical | interaction_behaviour |
| 4 | SC-CA-04 — Verify browser Back from Create Account returns the Developer to Login | AC1 | AC #1 | Positive | High | navigation_interaction |
| 5 | SC-CA-05 — Verify Create Account still shows primary registration controls after page refresh | AC1 | AC #1 | Positive | High | functional_workflow |
| 6 | SC-CA-06 — Verify Product Access option is visible and selectable on Create Account | AC1, AC3 | AC #1 + AC #3 + Linked item (KAN-8) | Positive | Critical | interaction_behaviour |
| 7 | SC-CA-07 — Verify Create Account is reachable from the QA Login URL by clicking `Create Account` | AC1 | AC #1 + Description (KAN-10) | Positive | Critical | navigation_interaction |

**Descriptions:**
- **1**: Proves AC1 happy path — from Login, `Create Account` opens Create Account and primary registration controls are visible and usable.
- **2**: Opposite of AC1 accessibility — without clicking `Create Account`, Create Account controls are not shown on Login.
- **3**: Confirms the confirmed `Create Account` control fires the expected open action on a single click.
- **4**: Browser Back from Create Account restores Login as the prior screen.
- **5**: Refresh does not leave Create Account inaccessible or stripped of primary controls.
- **6**: Product Access option is present on Create Account so the in-scope registration path can start.
- **7**: Navigation from the documented QA Login URL through `Create Account` reaches Create Account.

---

### [Web - Product Access]

| # | Scenario Title | Requirement | Source | Category | Priority | Guideline Source |
|---|---------------|-------------|--------|----------|----------|------------------|
| 8 | SC-PA-01 — Verify the Developer completes Product Access registration from Create Account through `Submit Registration` and sees a success message or account creation confirmation | AC3 | AC #3 + Linked item (KAN-8) | Positive | Critical | userstory_acceptance_coverage |
| 9 | SC-PA-02 — Verify Product Access registration does not complete when the Developer never selects the Product Access option | AC3 | AC #3 | Negative | High | userstory_acceptance_coverage |
| 10 | SC-PA-03 — Verify selecting the Product Access option opens the required-details step | AC3 | AC #3 + Description | Positive | Critical | functional_workflow |
| 11 | SC-PA-04 — Verify continuing from required details is blocked when every required Product Access field is left empty | AC3 | AC #3 | Negative | High | form_input_validation |
| 12 | SC-PA-05 — Verify each required Product Access field shows its own empty-field message when all required fields are submitted empty | AC3 | AC #3 | Negative | High | form_input_validation |
| 13 | SC-PA-06 — Verify only the empty required Product Access field shows an error while filled required fields keep their values | AC3 | AC #3 | Negative | Medium | form_input_validation |
| 14 | SC-PA-07 — Verify filling all required Product Access details allows the Developer to continue to Review | AC3 | AC #3 | Positive | Critical | form_input_validation |
| 15 | SC-PA-08 — Verify an invalid email format on the Product Access email field shows a format message and blocks continue when that field is required | AC3 | AC #3 | Negative | Medium | field_data_validation |
| 16 | SC-PA-09 — Verify a valid email format on the Product Access email field is accepted when that field is required | AC3 | AC #3 | Positive | Medium | field_data_validation |
| 17 | SC-PA-10 — Verify whitespace-only text in a required Product Access text field is rejected or cleared before continue | AC3 | AC #3 | Boundary | Medium | field_data_validation |
| 18 | SC-PA-11 — Verify `Submit Registration` on Review completes the Product Access path when clicked once | AC3 | AC #3 | Positive | High | interaction_behaviour |
| 19 | SC-PA-12 — Verify rapid double-click on `Submit Registration` does not create a second registration attempt | AC3 | AC #3 | Positive | High | interaction_behaviour |
| 20 | SC-PA-13 — Verify a success message or account creation confirmation screen appears after `Submit Registration` | AC3 | AC #3 + Description | Positive | Critical | notification_email_messaging |
| 21 | SC-PA-14 — Verify Product Access registration can finish with a new email when `shruthi00277@gmail.com` is already registered | AC3 | AC #3 + Description (KAN-10) + Project Knowledge (hid-developer-portal/testing.md) | Positive | Medium | userstory_acceptance_coverage |
| 22 | SC-PA-15 — Verify the Developer cannot skip the required-details step and land on Review without entering required Product Access details | AC3 | AC #3 | Negative | High | workflow_business_logic |
| 23 | SC-PA-16 — Verify leaving Product Access before Review does not show a success message or account creation confirmation | AC3 | AC #3 | Negative | Medium | functional_workflow |
| 24 | SC-PA-17 — Verify a failed `Submit Registration` does not show a success message or account creation confirmation | AC3 | AC #3 | Error | High | data_consistency_integrity |

**Descriptions:**
- **8**: Full AC3 happy path — Product Access option → required details → Review → `Submit Registration` → success message or confirmation.
- **9**: Opposite of AC3 — without choosing Product Access, registration through that workflow does not complete.
- **10**: Path selection moves the Developer into the required-details step.
- **11**: Required-field gate — empty required details block progress toward Review.
- **12**: All-empty submit shows a message for each required field at once.
- **13**: Single missing required field errors only that field and keeps other entered values.
- **14**: Valid complete details unlock continue to Review.
- **15**: Email format rule on Product Access (when email is a required live field) — invalid pattern blocked.
- **16**: Valid email format accepted on the same field.
- **17**: Whitespace-only required text is not treated as a real value.
- **18**: Single click on `Submit Registration` finishes the path once.
- **19**: Double-click protection on final submit.
- **20**: Visible success outcome after submit (message or confirmation screen).
- **21**: Alternate email when the known test mailbox is already registered.
- **22**: Wizard rule — cannot skip required details and reach Review empty-handed.
- **23**: Abandon before Review must not look like completed registration.
- **24**: Failed submit must not leave a false success confirmation.

---

### [Web - Review]

| # | Scenario Title | Requirement | Source | Category | Priority | Guideline Source |
|---|---------------|-------------|--------|----------|----------|------------------|
| 25 | SC-RV-01 — Verify Review shows every registration detail the Developer entered on Product Access before `Submit Registration` | AC6 | AC #6 + Linked item (KAN-8) | Positive | High | userstory_acceptance_coverage |
| 26 | SC-RV-02 — Verify Review does not omit a registration detail that the Developer entered on Product Access | AC6 | AC #6 | Negative | High | userstory_acceptance_coverage |
| 27 | SC-RV-03 — Verify each value on Review matches the exact value entered on the Product Access required-details step | AC6, AC7 | AC #6 + AC #7 | Positive | High | data_consistency_integrity |
| 28 | SC-RV-04 — Verify Review is populated with entered details and is not blank after a valid Product Access details step | AC6 | AC #6 | Positive | High | ui_error_state_validation |
| 29 | SC-RV-05 — Verify registration details stay accurate when the Developer moves from Product Access required details to Review | AC7 | AC #7 | Positive | High | userstory_acceptance_coverage |
| 30 | SC-RV-06 — Verify Product Access required-details fields still hold the earlier values after Back from Review | AC7 | AC #7 | Positive | High | workflow_business_logic |
| 31 | SC-RV-07 — Verify Review still shows the original entered details after Back to Product Access details and then forward to Review again | AC7 | AC #7 | Positive | High | workflow_business_logic |
| 32 | SC-RV-08 — Verify browser Back during the Product Access journey keeps previously entered registration details | AC7 | AC #7 | Positive | High | navigation_interaction |
| 33 | SC-RV-09 — Verify Review shows the updated value after the Developer changes a detail on Product Access and returns to Review | AC6, AC7 | AC #6 + AC #7 | Positive | Medium | data_consistency_integrity |
| 34 | SC-RV-10 — Verify `Submit Registration` from Review with accurate displayed details reaches a success message or account creation confirmation | AC6, AC3 | AC #6 + AC #3 | Positive | Critical | functional_workflow |

**Descriptions:**
- **25**: AC6 happy path — Review lists all entered registration details before submit.
- **26**: Opposite of AC6 — no silent omission of an entered detail on Review.
- **27**: Field-by-field parity between Product Access entry and Review display (AC6 + AC7).
- **28**: Review populated state after valid prior entry (not an empty Review).
- **29**: AC7 retention when moving forward to Review.
- **30**: Wizard back from Review restores prior Product Access field values.
- **31**: Round-trip Back then forward keeps Review accurate.
- **32**: Browser Back mid-journey does not wipe entered registration details.
- **33**: Edited values after Back are what Review shows on return.
- **34**: Accurate Review content plus submit yields the AC3 success outcome.

---

## 3. Flow Scenarios

### F-01 Create Account access (AC1)

| # | Scenario Title | Requirement | Source | Category | Priority |
|---|---------------|-------------|--------|----------|----------|
| 35 | SC-FL-01 — Verify Create Account access flow completes from QA Login URL through click of `Create Account` to a loaded Create Account page | AC1 | AC #1 + Description (KAN-10) | Positive | Critical |

### F-02 Product Access registration happy path (AC3)

| # | Scenario Title | Requirement | Source | Category | Priority |
|---|---------------|-------------|--------|----------|----------|
| 36 | SC-FL-02 — Verify Product Access registration flow completes from Login through Product Access option, required details, Review, and `Submit Registration` to a success message or account creation confirmation | AC3 | AC #3 + Linked item (KAN-8) | Positive | Critical |
| 37 | SC-FL-03 — Verify Product Access registration flow recovers when required details are incomplete then corrected before Review | AC3 | AC #3 | Error | High |

### F-03 Review details before submit (AC6) and F-04 detail retention (AC7)

| # | Scenario Title | Requirement | Source | Category | Priority |
|---|---------------|-------------|--------|----------|----------|
| 38 | SC-FL-04 — Verify the registration journey keeps entered Product Access details accurate through Review and still accurate after Back then forward before `Submit Registration` | AC6, AC7 | AC #6 + AC #7 | Positive | High |

---

## 4. Role-Based Scenarios

Single implied role only (Developer registrant). No Admin, Viewer, or other portal roles are defined for this feature. Multi-role positive/negative matrix does not apply.

| # | Scenario Title | Role | Category | Priority |
|---|---------------|------|----------|----------|
| — | Covered by SC-CA-01, SC-PA-01, and SC-FL-02 as the Developer (registrant) | Developer (registrant) | Positive | Critical |

---

## 5. Coverage Summary

**ACs covered**: 4 of 4 in-scope (AC1, AC3, AC6, AC7)  
**ACs explicitly out of scope**: AC2, AC4, AC5 — **zero coupon scenarios**  
**Pages/components covered**: Login (entry only), Create Account, Product Access required details, Review, Success / confirmation  
**Flows covered**: F-01, F-02, F-03, F-04  
**Coverage gaps**: Exact Product Access field labels and live validation copy remain discovery items on QA (G-006) — scenarios use “required Product Access fields” and parity assertions rather than invented labels. No Figma visual scenarios (none available). No coupon path coverage by design.

| AC | Positive | Negative / Error | Notes |
|----|----------|------------------|-------|
| AC1 | SC-CA-01, SC-CA-03, SC-CA-04, SC-CA-05, SC-CA-06, SC-CA-07, SC-FL-01 | SC-CA-02 | Create Account load and access from Login |
| AC3 | SC-PA-01, SC-PA-03, SC-PA-07, SC-PA-09, SC-PA-11, SC-PA-12, SC-PA-13, SC-PA-14, SC-RV-10, SC-FL-02 | SC-PA-02, SC-PA-04, SC-PA-05, SC-PA-06, SC-PA-08, SC-PA-15, SC-PA-16, SC-PA-17, SC-FL-03 | Product Access end-to-end only — no coupon |
| AC6 | SC-RV-01, SC-RV-03, SC-RV-04, SC-RV-09, SC-RV-10, SC-FL-04 | SC-RV-02 | Review shows all entered details |
| AC7 | SC-RV-03, SC-RV-05, SC-RV-06, SC-RV-07, SC-RV-08, SC-RV-09, SC-FL-04 | — (loss of retention covered via SC-RV-02 omission check and SC-PA-16 abandon) | Retention across Product Access → Review and back |
| AC2 | — | — | Out of scope — no scenarios |
| AC4 | — | — | Out of scope — no scenarios |
| AC5 | — | — | Out of scope — no scenarios |

**Guideline depth applied (in-scope only):**
- `userstory_acceptance_coverage` — every in-scope AC
- `functional_workflow` — AC1 load, AC3 journey, Review submit
- `workflow_business_logic` — skip-step block, wizard Back/forward
- `form_input_validation` — Product Access required details
- `field_data_validation` — email format and whitespace (as live fields allow)
- `interaction_behaviour` — `Create Account`, Product Access option, `Submit Registration` single/double click
- `navigation_interaction` — Login → Create Account, browser Back, retention on Back
- `notification_email_messaging` — success message / confirmation after submit
- `data_consistency_integrity` — Review parity, failed submit, edit-then-return
- `ui_error_state_validation` — populated Review state only (no network/loading edge cases)

**Not applied (by design):** `ui_ux_visual_figma` (no Figma), `security_session_management` / standalone security, `rolebased_access_permission` multi-role matrix (single role), coupon-related form/field guidelines for AC2/AC4/AC5.
