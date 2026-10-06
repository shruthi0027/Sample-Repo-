# Context: AG-3

**Title**: AMP Admin Portal
**Type**: Unknown (Jira issue fetch failed; not confirmed)
**Status**: Unknown (Jira issue fetch failed; not confirmed)
**Date**: 2026-10-06
**Parent Issue**: AG-3

> **Source note**: `mcp-atlassian` / Jira MCP tools were not available in this session. Jira REST (`GET /rest/api/3/issue/AG-3`) was attempted with Basic auth from environment variables. Authentication failed (`401 AUTHENTICATED_FAILED` on `/rest/api/3/myself`; issue lookup returned `404` / no permission). Issue type, status, parent/sub-task relationship, description field, custom AC field, comments, links, and attachments could not be read from Jira. The title, description, environment details, and AC1–AC12 below are taken **verbatim** from the triggering comment, which the workflow treats as supplementary context. They could not be verified against the live Jira issue.

---

## 1. Acceptance Criteria (Primary)

All acceptance criteria below are preserved verbatim from the triggering comment (not fetched from Jira fields).

- AC1: Sign-in & Access: Only authorized Super Admin users can sign in. Unauthorized users denied.
- AC2: Navigation: Access modules Products, Teams, Roles, Users, Workflows, Ticket Forms, Service Catalog, Locations.
- AC3: Session Management: Sessions active during navigation, invalid after logout.
- AC4: Product Management: Create, view, update, enable, disable products.
- AC5: Team & Role Management: Create and configure teams, roles, assignments.
- AC6: User & Membership Management: Create desk users, assign memberships, modify permissions, revoke access.
- AC7: Permission Management: Manage role-based permissions, access grants, view configurations.
- AC8: Workflow Management: Create and manage workflow templates.
- AC9: Ticket Forms & Service Catalog: Configure ticket forms and service catalog via TMS.
- AC10: Super Admin Visibility: View Super Admin details; no create/modify/delete Super Admin accounts.
- AC11: Geo & Assignment Group Management: Manage countries, locations, product-country mappings, assignment groups.
- AC12: Validation & Error Handling: Required field validation; clear error messages for invalid entries or backend failures.

---

## 1-API. API Specification

This feature is a web administration console (UI). No OpenAPI/Swagger file, API contract attachment, or endpoint specification was found in Jira (fetch failed), `docs/`, `specs/`, `knowledge/`, or the triggering comment.

No `context/api-spec/` files were created. Downstream API-only planning does not apply. Functional tests should target the Admin Portal UI and SSO sign-in, not undocumented HTTP APIs.

---

## 2. Description

The AMP (Access Management Platform) Admin Portal is a web-based administration console used by Portal Super Admins to manage products, teams, roles, users, permissions, workflows, ticket forms, service catalogs, locations, and assignment groups.

Application URL: https://accessmanagement.dev.platform.hidcloud.com/index.html#/applications

Authentication: SSO sign-in (no password). Test email: shruthi.thandapani@hidglobal.com

| Field | Value |
|-------|-------|
| Summary (from comment) | AMP Admin Portal / Start QA Grooming for AMP Admin Portal |
| Issue type | Unknown — Jira fetch failed; sub-task vs Story/Epic/Feature not confirmed |
| Status | Unknown — Jira fetch failed |
| Priority | Unknown — Jira fetch failed |
| Project | AG |
| Issue key requested | AG-3 |
| Assignee | Unknown — Jira fetch failed |
| Reporter | Unknown — Jira fetch failed |
| Browse URL | https://shruthi00277.atlassian.net/browse/AG-3 |
| Parent | Not confirmed. Treated as AG-3 until Jira returns a parent key |
| Labels | Unknown — Jira fetch failed |
| Components | Unknown — Jira fetch failed |
| Fix versions | Unknown — Jira fetch failed |
| Issue links | Unknown — Jira fetch failed |
| Sub-tasks | Unknown — Jira fetch failed |
| Remote links | Unknown — Jira fetch failed |
| Comments | Jira comments not retrieved. Triggering comment used as supplementary source |
| Attachments | Unknown — Jira fetch failed (0 files downloaded) |

---

## 3. Linked Items

Linked issues could not be listed because Jira authentication failed.

### Unable to fetch: AG-3 issue links / parent / sub-tasks

**Type**: Unknown
**Status**: Unknown
**Impact Assessment**: Parent, epic, blocking, and related work cannot be assessed. If AG-3 is a sub-task, the parent Story/Epic/Feature was not loaded and its ACs (if different from the comment) are missing. Downstream publish linking should use **AG-3** until a parent key is confirmed.
**Relevant Details**: Historical workspace artifact `QA Artifacts/AG/AG-1/` shows AG-1 as a standalone Task titled "test the cases" with empty description and no ACs. AG-1 is not a requirements parent for AMP Admin Portal.

---

## 4. Attachments

No attachments downloaded.

Jira attachment metadata was not available (`GET /rest/api/3/issue/AG-3` failed). Folder `QA Artifacts/AG/AG-3/context/attachments/` is empty. No text specs, mockups, or API contracts were available to extract.

---

## 5. Project Knowledge

No relevant project knowledge found in the cloned repo on branch `main`.

| Source | File | Relevance | Key Details |
|--------|------|-----------|-------------|
| specs | *(folder not present in HEAD on `main`)* | Not available | Sparse-checkout includes `specs/` but `git ls-tree` has no `specs/` files |
| docs | *(folder not present in HEAD on `main`)* | Not available | Sparse-checkout includes `docs/` but `git ls-tree` has no `docs/` files |
| knowledge | `knowledge/AG/` | Not available | No living knowledge files under `knowledge/` for project AG |
| QA Artifacts | `QA Artifacts/AG/AG-1/context/` | Historical only | Prior AG-1 context is an empty Task; does not describe AMP Admin Portal |

### Feature Specs (`specs/`)

No feature specs available. No user-named spec file (`spec:`, `spec=`, `use spec`, `spec file:`, or a bare `.md` filename under `specs/`) was referenced in the triggering comment.

### Comment-Derived Context

- Triggering comment (session 2026-10-06): Instructs QA Grooming for AMP Admin Portal; identifies the product as Access Management Platform; names Portal Super Admin as the administering role; lists managed domains (products, teams, roles, users, permissions, workflows, ticket forms, service catalogs, locations, assignment groups).
- Triggering comment (session 2026-10-06): Application URL is `https://accessmanagement.dev.platform.hidcloud.com/index.html#/applications` (hash route `#/applications`).
- Triggering comment (session 2026-10-06): Authentication is SSO with no password. Authorized test email given: `shruthi.thandapani@hidglobal.com`.
- Triggering comment (session 2026-10-06): Supplies AC1–AC12 listed in Section 1 (sign-in, module navigation, session after logout, product/team/role/user/permission/workflow/form/catalog/geo admin, Super Admin view-only for Super Admin accounts, validation/errors).
- Triggering comment (session 2026-10-06): Ticket Forms and Service Catalog are configured **via TMS** (AC9). TMS is named only as an integration/path; no TMS URL or screens were provided.
- Jira issue comments: not retrieved (auth failure). Any clarifications stored only on the issue are missing from this bundle.

---

## 6. Figma Designs

No Figma designs linked

---

## 7. Functional Setup Details

**Roles and Permissions:**
- Portal Super Admin is the role that uses the Admin Portal.
- Only authorized Super Admin users can sign in; unauthorized users are denied (AC1).
- Super Admin details can be viewed; Super Admin accounts must not be created, modified, or deleted from this portal (AC10).
- Desk users can be created; memberships assigned; permissions modified; access revoked (AC6).
- Role-based permissions, access grants, and view configurations are managed in the portal (AC7).
- Teams, roles, and assignments can be created and configured (AC5).

**Entities and Configuration:**
- Products: create, view, update, enable, disable (AC4).
- Teams, roles, assignments (AC5).
- Desk users and memberships (AC6).
- Workflow templates (AC8).
- Ticket forms and service catalog, configured via TMS (AC9).
- Countries, locations, product-country mappings, assignment groups (AC11).
- Modules named for navigation: Products, Teams, Roles, Users, Workflows, Ticket Forms, Service Catalog, Locations (AC2). Assignment groups and countries are called out in AC11 but are not in the AC2 module list.

**Settings and Feature States:**
- Products have enable and disable states (AC4).
- Sessions remain valid while navigating modules and become invalid after logout (AC3).
- SSO is the sign-in method; there is no password field for this flow.

**Plans and Subscriptions:**
- Not specified in available sources.

**Schedules and Time-Based Config:**
- Not specified in available sources.

**Navigation Starting Points:**
- Open `https://accessmanagement.dev.platform.hidcloud.com/index.html#/applications`.
- Complete SSO sign-in as an authorized Super Admin (test email `shruthi.thandapani@hidglobal.com`).
- After sign-in, use module navigation to Products, Teams, Roles, Users, Workflows, Ticket Forms, Service Catalog, and Locations.

**Connectivity and Hardware:**
- Web application in a browser. No hardware, Bluetooth, or device pairing is specified.

---

## 8. UI Terminology & Navigation Map

Extracted from the triggering comment and AC module names only. Exact visible labels, icons, and menus were not confirmed in Figma or product specs. Do not invent additional button names.

### 8a. Screen / Page Inventory

| Screen Name | Navigation Path | Visible To |
|---|---|---|
| Applications (hash route `#/applications`) | Open `https://accessmanagement.dev.platform.hidcloud.com/index.html#/applications` | Portal Super Admin (authorized); unauthorized users denied at sign-in |
| SSO sign-in | Open the application URL; complete SSO (no password) | Authorized Super Admin users; unauthorized users denied |
| Products | After sign-in, open the `Products` module | Portal Super Admin |
| Teams | After sign-in, open the `Teams` module | Portal Super Admin |
| Roles | After sign-in, open the `Roles` module | Portal Super Admin |
| Users | After sign-in, open the `Users` module | Portal Super Admin |
| Workflows | After sign-in, open the `Workflows` module | Portal Super Admin |
| Ticket Forms | After sign-in, open the `Ticket Forms` module (configuration via TMS per AC9) | Portal Super Admin |
| Service Catalog | After sign-in, open the `Service Catalog` module (configuration via TMS per AC9) | Portal Super Admin |
| Locations | After sign-in, open the `Locations` module | Portal Super Admin |
| Super Admin details (view) | Path not specified beyond viewing Super Admin details without create/modify/delete | Portal Super Admin (view only for Super Admin accounts) |
| Countries / product-country mappings / assignment groups | Not listed as separate AC2 modules; managed under geo and assignment group behavior (AC11). Exact menu labels unknown | Portal Super Admin |

### 8b. Key UI Elements

| Element | Type | Screen | Label / Text | Interaction |
|---|---|---|---|---|
| SSO sign-in | Button / identity-provider flow | SSO sign-in | Not specified (no password field) | Click / complete SSO |
| Products | Menu item / module | Admin Portal | `Products` | Click |
| Teams | Menu item / module | Admin Portal | `Teams` | Click |
| Roles | Menu item / module | Admin Portal | `Roles` | Click |
| Users | Menu item / module | Admin Portal | `Users` | Click |
| Workflows | Menu item / module | Admin Portal | `Workflows` | Click |
| Ticket Forms | Menu item / module | Admin Portal | `Ticket Forms` | Click |
| Service Catalog | Menu item / module | Admin Portal | `Service Catalog` | Click |
| Locations | Menu item / module | Admin Portal | `Locations` | Click |
| Product enable/disable | Control (type not specified) | Products | Enable / Disable (wording not confirmed in UI) | Click / toggle |
| Logout | Control (type not specified) | Any signed-in screen | Logout (exact label not confirmed) | Click |

### 8c. Terminology Glossary

| Generic Term | Product Term | Notes |
|---|---|---|
| Admin console / admin app | AMP Admin Portal | Access Management Platform web administration console |
| Admin user | Portal Super Admin | Only authorized Super Admin users may sign in |
| Login with password | SSO sign-in (no password) | Test email `shruthi.thandapani@hidglobal.com` |
| Applications home | `#/applications` | Path on the provided application URL |
| Support tickets setup | Ticket Forms | Configured via TMS (AC9) |
| Catalog of services | Service Catalog | Configured via TMS (AC9) |
| Helpdesk staff account | Desk user | Created and membership-managed in User & Membership Management (AC6) |
| Admin account | Super Admin | View details only; no create, modify, or delete Super Admin accounts (AC10) |
| Geographic sites | Locations / countries / product-country mappings | AC11; Locations is an AC2 module |
| Routing / queue group | Assignment group | AC11; not named as its own AC2 module |
| Process template | Workflow template | AC8 |

---

## 9. Context Summary

**Total Acceptance Criteria**: 12 (from triggering comment; not verified on the Jira issue)
**Endpoints in API Spec**: N/A (web UI feature; no API specification found)
**Linked Issues Fetched**: 0 / unknown (Jira fetch failed)
**Attachments Downloaded**: 0 / unknown (Jira fetch failed)
**Knowledge Files Scanned**: 0 (`docs/`, `specs/`, and `knowledge/AG/` empty or absent on `main`)
**Warnings**:
- Jira MCP (`mcp-atlassian`) was not in the available tool catalog
- Jira REST Basic auth failed (`401 AUTHENTICATED_FAILED`); `/rest/api/3/issue/AG-3` returned issue does not exist or no permission
- Parent vs sub-task relationship was not confirmed; **Parent Issue** recorded as AG-3
- Title, description, and AC1–AC12 taken from the triggering comment, not from Jira fields
- Jira comments, issue links, and attachments were not retrieved
- No Figma URLs in the triggering comment or other available text
- `docs/` and `specs/` are not populated on branch `main`
- No user-named spec file in the comment
- UI labels beyond module names in AC2 are not confirmed by Figma or specs
- TMS (AC9) has no URL, screens, or field list in available sources
