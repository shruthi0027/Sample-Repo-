# Test Cases — HID Developer Portal Product Access Registration

**Feature**: HID Developer Portal — Create Account and Product Access registration
**Date**: 2026-10-24
**Source Scenarios**: `QA Artifacts/KAN/KAN-10/functional/scenarios-KAN-10.md`
**Requirement Story**: KAN-8 — dev port
**Testing Task**: KAN-10
**Total Test Cases**: 38
**Scope**: AC1, AC3, AC6, AC7 only — no coupon TCs (AC2, AC4, AC5)

---

## 1. Summary

| Metric | Count |
|--------|-------|
| Total Test Cases | 38 |
| Critical Priority | 11 |
| High Priority | 20 |
| Medium Priority | 7 |
| Low Priority | 0 |

**By Test Category:**

| Category | Count |
|----------|-------|
| Boundary | 1 |
| Error | 2 |
| Negative | 9 |
| Positive | 26 |

**By Suite Tag:**

| Tag | Count |
|-----|-------|
| Smoke | 11 |
| Sanity | 38 |

---

## 2. Test Cases

### [Web - Create Account]

#### TC-001: Verify Create Account page loads with usable primary registration controls after the Developer clicks `Create Account` on Login

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 + Linked item (KAN-8) + Description (KAN-10) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click the `Create Account` control on the Login page. | The Create Account page loads. |
| 3 | Check that primary registration controls on Create Account are visible. | Primary registration controls are visible on the Create Account page. |
| 4 | Check that the primary registration controls are usable (not greyed out or blocked). | The Developer can interact with the primary registration controls, including the Product Access option path. |

**Post-conditions:**
- The Create Account page remains open with usable primary registration controls.

#### TC-002: Verify Login stays on the Login screen and does not show Create Account primary registration controls when the Developer has not clicked `Create Account`

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Do not click `Create Account`. | The page stays on Login. |
| 3 | Check the Login page for Create Account primary registration controls (path selection such as the Product Access option and registration detail entry). | Create Account primary registration controls are not shown on the Login page. |
| 4 | Check that Login-related controls remain on the page. | The Login page still shows its sign-in controls and does not switch to the Create Account page. |

**Post-conditions:**
- None

#### TC-003: Verify `Create Account` on Login opens Create Account when clicked once

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 + Description (KAN-10) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed with the `Create Account` control visible. |
| 2 | Click `Create Account` once. | The Create Account page opens after the single click. |
| 3 | Check that the browser is no longer showing only the Login screen as the active registration start page. | Create Account is the active page and primary registration controls are available. |

**Post-conditions:**
- The Developer is on the Create Account page.

#### TC-004: Verify browser Back from Create Account returns the Developer to Login

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Click the browser Back control. | The Login page is displayed again. |
| 4 | Check that the Login page shows the `Create Account` control. | The `Create Account` control is visible on Login. |

**Post-conditions:**
- The Developer is back on the Login page.

#### TC-005: Verify Create Account still shows primary registration controls after page refresh

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads with primary registration controls visible. |
| 3 | Refresh the browser page. | The Create Account page reloads. |
| 4 | Check the primary registration controls after refresh. | Primary registration controls remain visible and usable on Create Account. |

**Post-conditions:**
- Create Account remains accessible after refresh.

#### TC-006: Verify Product Access option is visible and selectable on Create Account

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC1, AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #1 + AC #3 + Linked item (KAN-8) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Check that the Product Access option is visible on Create Account. | The Product Access option is shown on the Create Account page. |
| 4 | Select the Product Access option. | The Product Access option is selected and the registration path can continue. |

**Post-conditions:**
- The Product Access option is selected on Create Account.

#### TC-007: Verify Create Account is reachable from the QA Login URL by clicking `Create Account`

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 + Description (KAN-10) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal is reachable at the documented Login URL.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page loads from the QA Login URL. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Check the page title or main heading area for Create Account content. | The Create Account page is shown and is ready for registration. |

**Post-conditions:**
- The Developer reached Create Account from the QA Login URL.

### [Web - Product Access]

#### TC-008: Verify the Developer completes Product Access registration from Create Account through `Submit Registration` and sees a success message or account creation confirmation

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 + Linked item (KAN-8) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The required-details step for Product Access is shown. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Continue from the required-details step to Review using the on-screen continue control. | The Review page opens. |
| 6 | Check that Review shows the registration details just entered. | Review lists the entered Product Access registration details. |
| 7 | Click `Submit Registration` once. | A success message appears, or an account creation confirmation screen is displayed. |

**Post-conditions:**
- Product Access registration completed with a visible success message or account creation confirmation.

#### TC-009: Verify Product Access registration does not complete when the Developer never selects the Product Access option

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Do not select the Product Access option. | The Product Access option stays unselected. |
| 4 | Look for the Product Access required-details step and for `Submit Registration`. | The Product Access required-details step and Review with `Submit Registration` are not completed as a finished Product Access registration. |
| 5 | Check that no success message or account creation confirmation for Product Access registration is shown. | No Product Access registration success message or account creation confirmation is displayed. |

**Post-conditions:**
- None — Product Access registration did not complete.

#### TC-010: Verify selecting the Product Access option opens the required-details step

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 + Description |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Check that required Product Access input fields are shown. | Required Product Access detail fields are visible for entry. |

**Post-conditions:**
- The Developer is on the Product Access required-details step.

#### TC-011: Verify continuing from required details is blocked when every required Product Access field is left empty

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Leave every required Product Access field empty. | Required Product Access fields remain empty. |
| 5 | Click the continue control that moves toward Review. | The Developer does not move to Review. Progress stays on the required-details step. |
| 6 | Check for empty-field guidance on the form. | Messages or other blocking feedback appear for the empty required fields (exact wording as shown on the live page). |

**Post-conditions:**
- None — continue to Review remains blocked.

#### TC-012: Verify each required Product Access field shows its own empty-field message when all required fields are submitted empty

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Leave all required Product Access fields empty. | All required fields are empty. |
| 5 | Click the continue control that moves toward Review. | Continue does not open Review. |
| 6 | Check each required Product Access field for an empty-field message. | Each required Product Access field shows its own empty-field message (exact wording as shown on the live page). |

**Post-conditions:**
- None

#### TC-013: Verify only the empty required Product Access field shows an error while filled required fields keep their values

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill all required Product Access fields with valid values except one required field left empty. Use `shruthi00277@gmail.com` in the email field if present. For other filled fields use values such as `Alex`, `Rivera`, and `HID QA Test` matching each field purpose. | Filled required fields show their values. One required field remains empty. |
| 5 | Click the continue control that moves toward Review. | Continue does not open Review. |
| 6 | Check the empty required field. | An error or empty-field message appears for the empty required field only (exact wording as shown on the live page). |
| 7 | Check the fields that were filled. | Previously entered values remain in the filled required fields. |

**Post-conditions:**
- None

#### TC-014: Verify filling all required Product Access details allows the Developer to continue to Review

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Click the continue control that moves toward Review. | The Review page opens. |
| 6 | Check that Review is shown before `Submit Registration`. | Review is displayed and `Submit Registration` is available. |

**Post-conditions:**
- The Developer is on Review with completed Product Access details.

#### TC-015: Verify an invalid email format on the Product Access email field shows a format message and blocks continue when that field is required

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. The Product Access required-details step includes a required email field on the live page.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Type `not-an-email` in the Product Access email field. | The email field shows `not-an-email`. |
| 5 | Fill every other required Product Access field with valid values (for example `Alex`, `Rivera`, `HID QA Test`) using the exact labels on the live page. | Other required fields show their entered values. |
| 6 | Click the continue control that moves toward Review. | Continue does not open Review. |
| 7 | Check the Product Access email field. | A format message appears for the email field indicating the format is invalid (exact wording as shown on the live page). |

**Post-conditions:**
- None

#### TC-016: Verify a valid email format on the Product Access email field is accepted when that field is required

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. The Product Access required-details step includes a required email field on the live page.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Type `shruthi00277@gmail.com` in the Product Access email field. | The email field shows `shruthi00277@gmail.com`. |
| 5 | Fill every other required Product Access field with valid values (for example `Alex`, `Rivera`, `HID QA Test`) using the exact labels on the live page. | Other required fields show their entered values. |
| 6 | Click the continue control that moves toward Review. | The Review page opens with no email-format error on the email field. |

**Post-conditions:**
- Valid email format was accepted and Review is reachable.

#### TC-017: Verify whitespace-only text in a required Product Access text field is rejected or cleared before continue

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Boundary |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Type only spaces in one required Product Access text field. | The field shows only whitespace. |
| 5 | Fill every other required Product Access field with valid values, including `shruthi00277@gmail.com` in the email field if present. | Other required fields show valid values. |
| 6 | Click the continue control that moves toward Review. | Continue does not treat whitespace-only text as a completed value. Review does not open, or the whitespace is cleared and the field is treated as empty. |
| 7 | Check the whitespace-only required field. | An empty-field or invalid-value message appears for that field, or the whitespace was cleared (behavior as shown on the live page). |

**Post-conditions:**
- None

#### TC-018: Verify `Submit Registration` on Review completes the Product Access path when clicked once

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Click `Submit Registration` once. | The Product Access registration completes. A success message appears, or an account creation confirmation screen is displayed. |

**Post-conditions:**
- Registration completed after a single click of `Submit Registration`.

#### TC-019: Verify rapid double-click on `Submit Registration` does not create a second registration attempt

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Continue to Review. | The Review page opens with `Submit Registration` visible. |
| 6 | Rapidly double-click `Submit Registration`. | Only one registration completion runs. A single success message or one account creation confirmation screen appears. No second conflicting success outcome or duplicate registration attempt is shown. |

**Post-conditions:**
- A single registration outcome is shown after the double-click.

#### TC-020: Verify a success message or account creation confirmation screen appears after `Submit Registration`

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 + Description |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Click `Submit Registration`. | A success message is shown, or an account creation confirmation screen is displayed. |
| 7 | Read the success message or confirmation screen content. | The visible outcome clearly confirms successful account creation or completed registration. |

**Post-conditions:**
- Success message or account creation confirmation is visible.

#### TC-021: Verify Product Access registration can finish with a new email when `shruthi00277@gmail.com` is already registered

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 + Description (KAN-10) + Project Knowledge (hid-developer-portal/testing.md) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. `shruthi00277@gmail.com` is already registered on the portal.
4. A new unused email `hid.qa.product.access.001@example.com` is available for registration.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter `hid.qa.product.access.001@example.com` in the Product Access email field if email is required. | The email field shows `hid.qa.product.access.001@example.com`. |
| 5 | Fill every other required Product Access field with valid values (for example `Alex`, `Rivera`, `HID QA Test`) using the exact labels on the live page. | All required fields show valid values. |
| 6 | Continue to Review. | The Review page opens and shows the new email among the entered details. |
| 7 | Click `Submit Registration`. | A success message appears, or an account creation confirmation screen is displayed. |

**Post-conditions:**
- Registration completed using new email `hid.qa.product.access.001@example.com`.

#### TC-022: Verify the Developer cannot skip the required-details step and land on Review without entering required Product Access details

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Without filling required Product Access details, try any available control or URL change that would jump ahead to Review. | Review does not open with empty required Product Access details. |
| 5 | Check the current page. | The Developer remains on Create Account or the Product Access required-details step, not on an empty Review ready for `Submit Registration`. |

**Post-conditions:**
- None — skip to Review without required details is blocked.

#### TC-023: Verify leaving Product Access before Review does not show a success message or account creation confirmation

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter `shruthi00277@gmail.com` in the email field if present and enter `Alex` in one other required text field, then stop without continuing to Review. | Partial details are entered. Review is not open. |
| 5 | Leave the Product Access flow (for example go back to Login with browser Back, or open the Login URL again). | The Developer leaves the Product Access required-details step without reaching Review. |
| 6 | Check the page for a registration success message or account creation confirmation. | No success message and no account creation confirmation screen is shown. |

**Post-conditions:**
- None — registration was not completed.

#### TC-024: Verify a failed `Submit Registration` does not show a success message or account creation confirmation

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Error |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. A condition that causes `Submit Registration` to fail is available (for example an already-registered email that the portal rejects on submit, or another live submit failure shown on QA).

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill all required Product Access fields using values that will fail on submit when available (for example already-registered email `shruthi00277@gmail.com` if the portal rejects it at submit). Otherwise fill valid values and note the live failure condition used. | Required fields show the entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Click `Submit Registration`. | Submit fails. An error or failure message is shown (exact wording as on the live page), or the Developer stays on Review without completion. |
| 7 | Check for a success message or account creation confirmation screen. | No success message and no account creation confirmation screen is displayed. |

**Post-conditions:**
- None — failed submit did not show success confirmation.

### [Web - Review]

#### TC-025: Verify Review shows every registration detail the Developer entered on Product Access before `Submit Registration`

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC6 |
| Requirement_ID | KAN-8 |
| Source | AC #6 + Linked item (KAN-8) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter known values in every required Product Access field: email `shruthi00277@gmail.com` if present; first name `Alex`; last name `Rivera`; organization `HID QA Test` for fields that match those purposes; use matching clear values for any other required fields using their live labels. Write down each entered value. | All required fields show the entered values. |
| 5 | Continue to Review. | The Review page opens before `Submit Registration`. |
| 6 | Compare every value on Review to the values written down from Product Access. | Review shows every registration detail that was entered on Product Access. No entered detail is missing. |

**Post-conditions:**
- Review displays all entered Product Access details before submit.

#### TC-026: Verify Review does not omit a registration detail that the Developer entered on Product Access

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Negative |
| Suite Tags | Sanity |
| Requirement | AC6 |
| Requirement_ID | KAN-8 |
| Source | AC #6 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter distinct values in every required Product Access field (email `shruthi00277@gmail.com` if present; `Alex`, `Rivera`, `HID QA Test`, and other clear unique values for remaining required fields). Record the full list. | All required fields show the distinct entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Check Review against the recorded list field by field. | Every recorded Product Access value appears on Review. No entered registration detail is omitted. |

**Post-conditions:**
- None

#### TC-027: Verify each value on Review matches the exact value entered on the Product Access required-details step

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC6, AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #6 + AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter exact values: email `shruthi00277@gmail.com` if present; first name `Alex`; last name `Rivera`; organization `HID QA Review Match`; and matching exact values for any other required fields. Record each exact string. | Required fields show the exact entered strings. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Compare each Review value to the recorded exact string from Product Access. | Each Review value matches the exact string entered on Product Access with no truncation, swap, or change. |

**Post-conditions:**
- Review values match Product Access entry exactly.

#### TC-028: Verify Review is populated with entered details and is not blank after a valid Product Access details step

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC6 |
| Requirement_ID | KAN-8 |
| Source | AC #6 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Check the Review detail area. | Review is populated with the entered registration details and is not blank. |

**Post-conditions:**
- Review shows populated registration details.

#### TC-029: Verify registration details stay accurate when the Developer moves from Product Access required details to Review

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter and record values on Product Access required details (email `shruthi00277@gmail.com` if present; `Alex`, `Rivera`, `HID QA Retain`). | Required fields show the entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Check that Review still shows the same values recorded on Product Access. | Registration details on Review match the Product Access entries with no loss or change. |

**Post-conditions:**
- Details remained accurate from Product Access to Review.

#### TC-030: Verify Product Access required-details fields still hold the earlier values after Back from Review

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. The live UI provides a Back control from Review to Product Access required details, or browser Back returns to that step.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter values: email `shruthi00277@gmail.com` if present; first name `Alex`; last name `Rivera`; organization `HID QA Back`. Record them. | Required fields show the entered values. |
| 5 | Continue to Review. | The Review page opens with those details shown. |
| 6 | Go Back to the Product Access required-details step (in-app Back if present, otherwise browser Back). | The Product Access required-details step is shown again. |
| 7 | Check each required field that was filled earlier. | Each field still holds the earlier entered value. |

**Post-conditions:**
- Product Access fields retained values after Back from Review.

#### TC-031: Verify Review still shows the original entered details after Back to Product Access details and then forward to Review again

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Back from Review to Product Access required details is available on the live UI or via browser Back.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter and record original values (email `shruthi00277@gmail.com` if present; `Alex`, `Rivera`, `HID QA RoundTrip`). | Required fields show the original values. |
| 5 | Continue to Review. | Review shows the original entered details. |
| 6 | Go Back to Product Access required details. | Product Access required details are shown with the original values still present. |
| 7 | Continue forward to Review again without changing the values. | The Review page opens again. |
| 8 | Check Review against the original recorded values. | Review still shows the original entered details accurately. |

**Post-conditions:**
- Review remains accurate after Back then forward.

#### TC-032: Verify browser Back during the Product Access journey keeps previously entered registration details

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter and record values on required details (email `shruthi00277@gmail.com` if present; `Alex`, `Rivera`, `HID QA BrowserBack`). | Required fields show the entered values. |
| 5 | Continue to Review if continue is available from the filled form. | Review opens, or the next Product Access step after details is shown. |
| 6 | Click the browser Back control once. | The previous Product Access step is shown. |
| 7 | Check the registration detail fields that were filled earlier. | Previously entered registration details are still present and accurate. |

**Post-conditions:**
- Entered details remained after browser Back.

#### TC-033: Verify Review shows the updated value after the Developer changes a detail on Product Access and returns to Review

| Field | Value |
|-------|-------|
| Priority | Medium |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC6, AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #6 + AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Back from Review to Product Access required details is available on the live UI or via browser Back.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter initial values including organization `HID QA Original` (and email `shruthi00277@gmail.com` if present; `Alex`; `Rivera`). | Required fields show the initial values. |
| 5 | Continue to Review. | Review shows `HID QA Original` for the organization detail (or the matching field). |
| 6 | Go Back to Product Access required details. | Product Access required details open with the earlier values. |
| 7 | Change the organization field (or another chosen detail field) to `HID QA Updated`. | The field shows `HID QA Updated`. |
| 8 | Continue to Review again. | The Review page opens. |
| 9 | Check the changed detail on Review. | Review shows `HID QA Updated` for that detail, not `HID QA Original`. |

**Post-conditions:**
- Review reflects the updated Product Access value.

#### TC-034: Verify `Submit Registration` from Review with accurate displayed details reaches a success message or account creation confirmation

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC6, AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #6 + AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. Record the values. | All required fields show the entered values. |
| 5 | Continue to Review. | The Review page opens. |
| 6 | Confirm Review shows the same details that were entered on Product Access. | Review details match the Product Access entries. |
| 7 | Click `Submit Registration`. | A success message appears, or an account creation confirmation screen is displayed. |

**Post-conditions:**
- Registration completed from an accurate Review display.

### [Web - Flows]

#### TC-035: Verify Create Account access flow completes from QA Login URL through click of `Create Account` to a loaded Create Account page

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC1 |
| Requirement_ID | KAN-8 |
| Source | AC #1 + Description (KAN-10) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal is reachable at the documented Login URL.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page loads from the QA Login URL. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Check that Create Account primary registration controls are visible and usable. | Create Account access flow is complete: the page is loaded with usable primary registration controls. |

**Post-conditions:**
- Create Account access flow completed.

#### TC-036: Verify Product Access registration flow completes from Login through Product Access option, required details, Review, and `Submit Registration` to a success message or account creation confirmation

| Field | Value |
|-------|-------|
| Priority | Critical |
| Test Category | Positive |
| Suite Tags | Smoke | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 + Linked item (KAN-8) |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required Product Access fields show the entered values. |
| 5 | Continue to Review. | The Review page opens and shows the entered details. |
| 6 | Click `Submit Registration`. | A success message appears, or an account creation confirmation screen is displayed. |

**Post-conditions:**
- Full Product Access registration flow completed successfully.

#### TC-037: Verify Product Access registration flow recovers when required details are incomplete then corrected before Review

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Error |
| Suite Tags | Sanity |
| Requirement | AC3 |
| Requirement_ID | KAN-8 |
| Source | AC #3 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Email `shruthi00277@gmail.com` is available for registration, or a new unused email is ready if that mailbox is already registered.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Leave required Product Access fields empty and click the continue control toward Review. | Continue is blocked. Empty-field messages appear (exact wording as on the live page). |
| 5 | Fill every required Product Access field with valid values. Use `shruthi00277@gmail.com` in the email field if one is required. For other required fields enter values that match each field purpose (for example first name `Alex`, last name `Rivera`, organization `HID QA Test`). Use the exact field labels shown on the live page. | All required fields now show valid values. |
| 6 | Click the continue control toward Review again. | The Review page opens. |
| 7 | Click `Submit Registration`. | A success message appears, or an account creation confirmation screen is displayed. |

**Post-conditions:**
- Flow recovered after correcting incomplete details and completed registration.

#### TC-038: Verify the registration journey keeps entered Product Access details accurate through Review and still accurate after Back then forward before `Submit Registration`

| Field | Value |
|-------|-------|
| Priority | High |
| Test Category | Positive |
| Suite Tags | Sanity |
| Requirement | AC6, AC7 |
| Requirement_ID | KAN-8 |
| Source | AC #6 + AC #7 |

**Preconditions:**
1. The Developer is not signed in.
2. The QA HID Developer Portal Login page is reachable.
3. Back from Review to Product Access required details is available on the live UI or via browser Back.

**Steps:**
| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open `https://webportal.qa.developercommunity.hidcloud.com/login` in the browser. | The Login page is displayed. |
| 2 | Click `Create Account`. | The Create Account page loads. |
| 3 | Select the Product Access option. | The Product Access required-details step opens. |
| 4 | Enter and record values (email `shruthi00277@gmail.com` if present; `Alex`, `Rivera`, `HID QA Journey`). | Required fields show the entered values. |
| 5 | Continue to Review. | Review shows the recorded values accurately. |
| 6 | Go Back to Product Access required details. | Product Access fields still show the recorded values. |
| 7 | Continue forward to Review again without changing values. | Review again shows the same recorded values accurately. |
| 8 | Confirm details on Review still match the original recorded values before clicking `Submit Registration`. | Details remain accurate on Review. `Submit Registration` is available for the next action. |

**Post-conditions:**
- Journey retained accurate details through Review, Back, and forward before submit.

---

## 3. Coverage Summary

**Test cases generated**: 38
**Scenarios received**: 38
**Traceability mapping**: Confirmed — every SC ID maps to exactly one TC ID

| Scenario ID | Test Case ID | Title |
|-------------|--------------|-------|
| SC-CA-01 | TC-001 | Verify Create Account page loads with usable primary registration controls after the Developer clicks `Create Account` on Login |
| SC-CA-02 | TC-002 | Verify Login stays on the Login screen and does not show Create Account primary registration controls when the Developer has not clicked `Create Account` |
| SC-CA-03 | TC-003 | Verify `Create Account` on Login opens Create Account when clicked once |
| SC-CA-04 | TC-004 | Verify browser Back from Create Account returns the Developer to Login |
| SC-CA-05 | TC-005 | Verify Create Account still shows primary registration controls after page refresh |
| SC-CA-06 | TC-006 | Verify Product Access option is visible and selectable on Create Account |
| SC-CA-07 | TC-007 | Verify Create Account is reachable from the QA Login URL by clicking `Create Account` |
| SC-PA-01 | TC-008 | Verify the Developer completes Product Access registration from Create Account through `Submit Registration` and sees a success message or account creation confirmation |
| SC-PA-02 | TC-009 | Verify Product Access registration does not complete when the Developer never selects the Product Access option |
| SC-PA-03 | TC-010 | Verify selecting the Product Access option opens the required-details step |
| SC-PA-04 | TC-011 | Verify continuing from required details is blocked when every required Product Access field is left empty |
| SC-PA-05 | TC-012 | Verify each required Product Access field shows its own empty-field message when all required fields are submitted empty |
| SC-PA-06 | TC-013 | Verify only the empty required Product Access field shows an error while filled required fields keep their values |
| SC-PA-07 | TC-014 | Verify filling all required Product Access details allows the Developer to continue to Review |
| SC-PA-08 | TC-015 | Verify an invalid email format on the Product Access email field shows a format message and blocks continue when that field is required |
| SC-PA-09 | TC-016 | Verify a valid email format on the Product Access email field is accepted when that field is required |
| SC-PA-10 | TC-017 | Verify whitespace-only text in a required Product Access text field is rejected or cleared before continue |
| SC-PA-11 | TC-018 | Verify `Submit Registration` on Review completes the Product Access path when clicked once |
| SC-PA-12 | TC-019 | Verify rapid double-click on `Submit Registration` does not create a second registration attempt |
| SC-PA-13 | TC-020 | Verify a success message or account creation confirmation screen appears after `Submit Registration` |
| SC-PA-14 | TC-021 | Verify Product Access registration can finish with a new email when `shruthi00277@gmail.com` is already registered |
| SC-PA-15 | TC-022 | Verify the Developer cannot skip the required-details step and land on Review without entering required Product Access details |
| SC-PA-16 | TC-023 | Verify leaving Product Access before Review does not show a success message or account creation confirmation |
| SC-PA-17 | TC-024 | Verify a failed `Submit Registration` does not show a success message or account creation confirmation |
| SC-RV-01 | TC-025 | Verify Review shows every registration detail the Developer entered on Product Access before `Submit Registration` |
| SC-RV-02 | TC-026 | Verify Review does not omit a registration detail that the Developer entered on Product Access |
| SC-RV-03 | TC-027 | Verify each value on Review matches the exact value entered on the Product Access required-details step |
| SC-RV-04 | TC-028 | Verify Review is populated with entered details and is not blank after a valid Product Access details step |
| SC-RV-05 | TC-029 | Verify registration details stay accurate when the Developer moves from Product Access required details to Review |
| SC-RV-06 | TC-030 | Verify Product Access required-details fields still hold the earlier values after Back from Review |
| SC-RV-07 | TC-031 | Verify Review still shows the original entered details after Back to Product Access details and then forward to Review again |
| SC-RV-08 | TC-032 | Verify browser Back during the Product Access journey keeps previously entered registration details |
| SC-RV-09 | TC-033 | Verify Review shows the updated value after the Developer changes a detail on Product Access and returns to Review |
| SC-RV-10 | TC-034 | Verify `Submit Registration` from Review with accurate displayed details reaches a success message or account creation confirmation |
| SC-FL-01 | TC-035 | Verify Create Account access flow completes from QA Login URL through click of `Create Account` to a loaded Create Account page |
| SC-FL-02 | TC-036 | Verify Product Access registration flow completes from Login through Product Access option, required details, Review, and `Submit Registration` to a success message or account creation confirmation |
| SC-FL-03 | TC-037 | Verify Product Access registration flow recovers when required details are incomplete then corrected before Review |
| SC-FL-04 | TC-038 | Verify the registration journey keeps entered Product Access details accurate through Review and still accurate after Back then forward before `Submit Registration` |

**Suite tag coverage**: All test cases tagged Yes
**Coupon TCs**: None (AC2, AC4, AC5 out of scope)
**ACs covered**: AC1, AC3, AC6, AC7
