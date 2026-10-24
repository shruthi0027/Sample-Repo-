# Credential Requirements — KAN-10

**Prerequisite**: Resolve or skip before test-case browser execution.  
**Scope of this Step 0 write**: test case signals section only (no live auth discovery yet).

## Test case signals

Scanned sources: `functional/test-cases-KAN-10.csv` (all 261 rows / 38 TCs) and companion `functional/test-cases-KAN-10.md`. No additional steps were fetched from Jira issue keys (local `TC-*` IDs only).

### URLs

| URL | Where seen | Signal |
|-----|------------|--------|
| `https://webportal.qa.developercommunity.hidcloud.com/login` | Every TC Action step 1 (and titles/preconditions referencing QA Login) | **Base URL / Login URL** — primary app entry |

No other `http(s)` URLs appear in Action, Expected Result, Preconditions, or Tags.

### Roles

| Role | Signal |
|------|--------|
| **Developer** | Primary actor in titles, preconditions (“The Developer is not signed in”), and steps across TC-001–TC-038 |

No Admin, Owner, Manager, or other named roles appear in the scanned rows.

### Login / session signals

| Signal | Detail | TCs |
|--------|--------|-----|
| Unauthenticated start | Preconditions: Developer is **not signed in** | All 38 TCs |
| Login page as entry | Open Login URL, then click `Create Account` (registration path — not “log in with password” steps) | All 38 TCs |
| Existing-account login steps | No CSV/MD steps that type username/password into Login to authenticate | None in attachment |
| Registration email | Use `shruthi00277@gmail.com` when an email field is required; if already registered, use a new unused email | TC-008, TC-013, TC-014, TC-016–TC-021, TC-023–TC-034, TC-036–TC-038 |
| Alternate registration email | `hid.qa.product.access.001@example.com` when primary mailbox is already registered | TC-021 (and related already-registered flows) |

### OAuth / SSO / OTP / invitation / captcha

| Signal type | Found in CSV/MD? |
|-------------|------------------|
| OAuth (Google / Apple / social) | **No** |
| SSO / SAML / IdP | **No** |
| OTP / verification code / inbox access | **No** |
| Invitation / temporary password | **No** |
| Captcha | **No** |
| Password field in test steps | **No** (no `password` text in CSV/MD steps) |

### Implied CR-* candidates (names only — from test case signals)

| ID | Type | Detail | Source |
|----|------|--------|--------|
| CR-001 | Base URL | `https://webportal.qa.developercommunity.hidcloud.com/login` | All TC open-URL steps |
| CR-002 | Registration test email | Named mailbox for Product Access email field; alternate unused email if already registered | TC-008+ registration flows |
| CR-003 | Isolated / signed-out session | Fresh unauthenticated browser session (Developer not signed in) | All TC preconditions |

> Do not store password values in this file. Live auth discovery and Status (`PROVIDED` / `MISSING` / …) are filled in a later credential-analysis step.
