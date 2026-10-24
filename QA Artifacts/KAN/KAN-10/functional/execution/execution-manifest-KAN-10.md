# Execution Manifest — KAN-10

| Field | Value |
|-------|-------|
| **Issue** | [KAN-10](https://busybug027.atlassian.net/browse/KAN-10) |
| **Project** | KAN |
| **Scope** | Smoke (default — user said "Start web test execution") |
| **Source files** | `functional/test-cases-KAN-10.csv`, `functional/test-cases-KAN-10.md`, `functional/execution/jira-testcase-resolution-KAN-10.md` |
| **Resolution** | Local `TC-*` only — no Jira/TestRail case fetch (`jira-testcase-resolution-KAN-10.md`) |
| **Credentials** | CR-001 PROVIDED · CR-002 PROVIDED · CR-003 PROVIDED · CR-004 OPTIONAL (not required) · none SKIPPED |
| **Created** | 2026-10-24T12:32:00Z |
| **In-scope count** | 11 |
| **Pending** | 11 |
| **Blocked** | 0 |

## Notes

- Live host was unreachable during credential discovery (`net::ERR_CONNECTION_REFUSED` / private `10.8.x.x`). TCs remain **Pending** so execution can attempt; runtime may Block individual TCs if the portal stays unreachable.
- No passwords stored in this manifest.
- CR-004 (login password) is not required for Smoke Create Account / Product Access flows.

## In-scope test cases (Smoke)

| TC ID | Title | Priority | Jira source | Credential profile | Steps | Status |
|-------|-------|----------|-------------|--------------------|-------|--------|
| TC-001 | Verify Create Account page loads with usable primary registration controls after the Developer clicks `Create Account` on Login | Critical | — (local CSV/MD) | CR-001, CR-003 | 4 | Pending |
| TC-003 | Verify `Create Account` on Login opens Create Account when clicked once | Critical | — (local CSV/MD) | CR-001, CR-003 | 3 | Pending |
| TC-006 | Verify Product Access option is visible and selectable on Create Account | Critical | — (local CSV/MD) | CR-001, CR-003 | 4 | Pending |
| TC-007 | Verify Create Account is reachable from the QA Login URL by clicking `Create Account` | Critical | — (local CSV/MD) | CR-001, CR-003 | 3 | Pending |
| TC-008 | Verify the Developer completes Product Access registration from Create Account through `Submit Registration` and sees a success message or account creation confirmation | Critical | — (local CSV/MD) | CR-001, CR-002, CR-003 | 7 | Pending |
| TC-010 | Verify selecting the Product Access option opens the required-details step | Critical | — (local CSV/MD) | CR-001, CR-003 | 4 | Pending |
| TC-014 | Verify filling all required Product Access details allows the Developer to continue to Review | Critical | — (local CSV/MD) | CR-001, CR-002, CR-003 | 6 | Pending |
| TC-020 | Verify a success message or account creation confirmation screen appears after `Submit Registration` | Critical | — (local CSV/MD) | CR-001, CR-002, CR-003 | 7 | Pending |
| TC-034 | Verify `Submit Registration` from Review with accurate displayed details reaches a success message or account creation confirmation | Critical | — (local CSV/MD) | CR-001, CR-002, CR-003 | 7 | Pending |
| TC-035 | Verify Create Account access flow completes from QA Login URL through click of `Create Account` to a loaded Create Account page | Critical | — (local CSV/MD) | CR-001, CR-003 | 3 | Pending |
| TC-036 | Verify Product Access registration flow completes from Login through Product Access option, required details, Review, and `Submit Registration` to a success message or account creation confirmation | Critical | — (local CSV/MD) | CR-001, CR-002, CR-003 | 6 | Pending |

## Out of scope (not Smoke)

TC-002, TC-004, TC-005, TC-009, TC-011, TC-012, TC-013, TC-015, TC-016, TC-017, TC-018, TC-019, TC-021, TC-022, TC-023, TC-024, TC-025, TC-026, TC-027, TC-028, TC-029, TC-030, TC-031, TC-032, TC-033, TC-037, TC-038 (Sanity-only; 27 cases).

## Blocked test cases

None. Required credentials are PROVIDED; all in-scope TCs resolved from local CSV/MD.
