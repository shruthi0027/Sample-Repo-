# Context: AG-3 (linked / supporting)

**Title**: AMP Admin Portal
**Type**: Unknown (Jira issue fetch failed; not confirmed)
**Status**: Unknown (Jira issue fetch failed; not confirmed)
**Date**: 2026-10-06
**Parent Issue**: AG-3

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
- Triggering comment (session 2026-10-06): Supplies AC1–AC12 listed in the full context bundle Section 1 (sign-in, module navigation, session after logout, product/team/role/user/permission/workflow/form/catalog/geo admin, Super Admin view-only for Super Admin accounts, validation/errors).
- Triggering comment (session 2026-10-06): Ticket Forms and Service Catalog are configured **via TMS** (AC9). TMS is named only as an integration/path; no TMS URL or screens were provided.
- Jira issue comments: not retrieved (auth failure). Any clarifications stored only on the issue are missing from this bundle.

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
