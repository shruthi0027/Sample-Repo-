# Test Execution Results — KAN-10

| Field | Value |
|-------|-------|
| **Item / Run** | KAN-10 / KAN-10-exec-20261024T123415Z |
| **Project** | KAN |
| **Run Date** | 2026-10-24 |
| **Executed At** | 2026-10-24T12:34:46Z |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 31s (31000 ms) |
| **Base URL(s)** | https://webportal.qa.developercommunity.hidcloud.com/login |
| **Scope** | Smoke |
| **Browser** | agent-browser CLI (Chrome for Testing) |
| **Executed By** | QA Agent (agent-browser) |

---

## Executive Summary

| Result | Count |
|--------|-------|
| Pass | 0 |
| Fail | 0 |
| Blocked | 11 |
| **Total** | **11** |
| **Verdict** | Partial |
| **Total Time Taken** | 31s |

All Smoke test cases were blocked because the QA Login host was unreachable from the agent network (`net::ERR_CONNECTION_REFUSED` on private `10.8.x.x`). No Pass or Fail outcomes were recorded.

---

## Results Overview

| # | Test Case | Result | Run Date | Time Taken | Reason |
|---|-----------|--------|----------|------------|--------|
| TC-001 | Verify Create Account page loads with usable primary registration controls after the Developer clicks `Create Account` on Login | Blocked | 2026-10-24 12:34 UTC | 31s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-003 | Verify `Create Account` on Login opens Create Account when clicked once | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-006 | Verify Product Access option is visible and selectable on Create Account | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-007 | Verify Create Account is reachable from the QA Login URL by clicking `Create Account` | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-008 | Verify the Developer completes Product Access registration from Create Account through `Submit Registration` and sees a success message or account creation confirmation | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-010 | Verify selecting the Product Access option opens the required-details step | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-014 | Verify filling all required Product Access details allows the Developer to continue to Review | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-020 | Verify a success message or account creation confirmation screen appears after `Submit Registration` | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-034 | Verify `Submit Registration` from Review with accurate displayed details reaches a success message or account creation confirmation | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-035 | Verify Create Account access flow completes from QA Login URL through click of `Create Account` to a loaded Create Account page | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |
| TC-036 | Verify Product Access registration flow completes from Login through Product Access option, required details, Review, and `Submit Registration` to a success message or account creation confirmation | Blocked | 2026-10-24 12:34 UTC | 0s | QA Login host unreachable: net::ERR_CONNECTION_REFUSED (private 10.8.x.x) |

---

## Passes

No test cases passed in this run.

---

## Failures

No test cases failed in this run.

---

## Blocked

### TC-001 — Verify Create Account page loads with usable primary registration controls after the Developer clicks `Create Account` on Login

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 31s (31000 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-003 — Verify `Create Account` on Login opens Create Account when clicked once

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-006 — Verify Product Access option is visible and selectable on Create Account

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-007 — Verify Create Account is reachable from the QA Login URL by clicking `Create Account`

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-008 — Verify the Developer completes Product Access registration from Create Account through `Submit Registration` and sees a success message or account creation confirmation

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-010 — Verify selecting the Product Access option opens the required-details step

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-014 — Verify filling all required Product Access details allows the Developer to continue to Review

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-020 — Verify a success message or account creation confirmation screen appears after `Submit Registration`

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-034 — Verify `Submit Registration` from Review with accurate displayed details reaches a success message or account creation confirmation

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-035 — Verify Create Account access flow completes from QA Login URL through click of `Create Account` to a loaded Create Account page

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

### TC-036 — Verify Product Access registration flow completes from Login through Product Access option, required details, Review, and `Submit Registration` to a success message or account creation confirmation

| Field | Detail |
|-------|--------|
| **Result** | Blocked |
| **Run Date** | 2026-10-24 |
| **Started At** | 2026-10-24T12:34:15Z |
| **Finished At** | 2026-10-24T12:34:46Z |
| **Time Taken** | 0s (0 ms) |
| **Reason** | QA Login host unreachable from agent network: agent-browser open https://webportal.qa.developercommunity.hidcloud.com/login failed with net::ERR_CONNECTION_REFUSED (private 10.8.x.x). Cannot reach Login page to execute Create Account flow. |

---

## Artifacts

| Artifact | Path |
|----------|------|
| Results JSON | `execution-results-KAN-10.json` |
| Execution manifest | `execution-manifest-KAN-10.md` |
| Screenshots | `screenshots/` |
| This report (MD) | `test-result-KAN-10.md` |
| This report (HTML) | `test-result-KAN-10.html` |
