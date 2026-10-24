# Credential Requirements — KAN-10

**Prerequisite**: Resolve or skip before test-case browser execution.  
**Last updated**: 2026-10-24T12:30:00Z (Step 1 — live discovery + status merge)

## Auth surfaces discovered (live)

| Surface | URL | Methods visible |
|---------|-----|-----------------|
| Login (attempted) | `https://webportal.qa.developercommunity.hidcloud.com/login` | **Unreachable** — `net::ERR_CONNECTION_REFUSED` (DNS resolves to private `10.8.72.41` / `10.8.72.27`; curl connect timeout). No login form, SSO, OAuth, OTP, or magic-link controls could be cataloged. |
| Expected from TC/context (not live-confirmed) | Same Login URL | Login page with `Create Account` control; sign-in controls implied by page name and Jira credentials note. No OAuth/SSO/OTP/captcha signals in TCs. |

Browser closed after discovery attempts. No passwords or session tokens stored.

## Test case signals (from Step 0)

Scanned sources: `functional/test-cases-KAN-10.csv` (261 rows / 38 TCs) and `functional/test-cases-KAN-10.md`.

| Signal | Detail |
|--------|--------|
| URLs | Only `https://webportal.qa.developercommunity.hidcloud.com/login` |
| Role | Developer (unauthenticated start) |
| Path | Open Login → click `Create Account` → Product Access registration (no password-login steps in CSV) |
| Registration email | `shruthi00277@gmail.com`; alternate unused email if already registered |
| OAuth / SSO / OTP / invitation / captcha | None in CSV/MD |

## Resolution sources checked

| Source | Result |
|--------|--------|
| `QA Artifacts/credentials/credentials.json` | **Absent** (credentials folder does not exist) |
| Env `WEB_APP_BASE_URL` / `QA_TEST_EMAIL` / `QA_TEST_PASSWORD` | All unset |
| Context Section 7 | Login URL + email `shruthi00277@gmail.com`; password exists only in Jira description (not copied here) |
| Human reply / SKIP | None for execution credentials yet |

## CR-* requirements (deduplicated)

| ID | Type | Detail | Source | Live match | Status |
|----|------|--------|--------|------------|--------|
| CR-001 | Base URL | `https://webportal.qa.developercommunity.hidcloud.com/login` | All TC open-URL steps + Context Section 7 | Host unresolved from agent network (connection refused) — URL value known | **PROVIDED** |
| CR-002 | Registration test email | `shruthi00277@gmail.com` (use a new unused email if already registered; alternate example `hid.qa.product.access.001@example.com`) | TC-008+ preconditions + Context Section 7 + grooming Q-005 | N/A (form not reachable) | **PROVIDED** |
| CR-003 | Isolated / signed-out session | Fresh unauthenticated browser session (Developer not signed in) | All TC preconditions | agent-browser fresh session available | **PROVIDED** |
| CR-004 | Login (default) email + password | Existing-account sign-in — **not used** by Create Account / Product Access TC steps | Context Section 7 credentials note; Jira description only for password | Live form not visible (host unreachable) | **OPTIONAL** (MISSING value in env/shared file — not required for scoped TCs; do not ask) |

> Do not store password values in this file.

## Gate decision

| Check | Result |
|-------|--------|
| Required CR-* all PROVIDED or SKIPPED? | **Yes** — CR-001, CR-002, CR-003 are PROVIDED; CR-004 is OPTIONAL |
| Credential request comment needed? | **No** — no required CR-* is MISSING |
| Proceed to execution manifest? | **Yes** (hard gate clear). Live host reachability remains a runtime risk — TCs may Block if the portal stays unreachable from the agent network. |
