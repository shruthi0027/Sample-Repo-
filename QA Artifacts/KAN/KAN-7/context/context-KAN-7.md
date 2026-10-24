# Context: KAN-7

**Title**: task of testing
**Type**: Task
**Status**: To Do
**Priority**: Medium
**Date**: 2026-10-24
**Parent Issue**: None (standalone Task)
**Requirements source (linked Story)**: **KAN-6** — DEV portal
**Browse URL**: https://busybug027.atlassian.net/browse/KAN-7
**Project**: KAN (Agent EXP)
**Assignee**: QA Agent
**Reporter**: Main Agent (busybug027@gmail.com)

---

## 1. Acceptance Criteria (Primary)

KAN-7 has no acceptance criteria field. Primary ACs are taken **verbatim** from linked Story **KAN-6**:

- **AC1:** Create Account page loads successfully and is accessible to users.
- **AC2:** Users can complete registration using a valid coupon code.
- **AC3:** Users can complete registration through the product access workflow.
- **AC4:** Valid coupon codes are accepted and allow users to continue the registration process.
- **AC5:** Invalid coupon codes display an appropriate validation error message.
- **AC6:** Review page displays all entered registration details before submission.
- **AC7:** Registration details entered by the user are retained and accurately displayed throughout the registration journey.

---

## 1-API. API Specification

This feature is a web UI (Developer Portal registration / login). No OpenAPI/Swagger file, API contract attachment, or endpoint specification was found in Jira (KAN-7 / KAN-6), `docs/`, `specs/`, or `knowledge/`.

No `context/api-spec/` files were created. Functional tests should target the portal UI flows (create account, coupon, product access, review), not undocumented HTTP APIs.

---

## 2. Description

### Triggered task (KAN-7)

| Field | Value |
|-------|-------|
| Summary | task of testing |
| Issue type | Task |
| Status | To Do |
| Priority | Medium |
| Description | Points testers at the QA Developer Community web portal login URL and provides a test mailbox. Credentials are present in the Jira description and are **not** duplicated here (see Environment). |
| Application URL | https://webportal.qa.developercommunity.hidcloud.com/login |
| Labels / Components / Fix versions | None set |
| Attachments | None |

### Linked story requirements (KAN-6)

The HID Developer Portal enables developers to create an account and register for access using either a coupon-based registration process or a product access workflow. The registration experience should validate coupon codes, support product-based access requests, and provide a review step before final submission.

| Field | Value |
|-------|-------|
| Summary | DEV portal |
| Issue type | Story |
| Status | To Do |
| Priority | Medium |
| Browse | https://busybug027.atlassian.net/browse/KAN-6 |

---

## 3. Linked Items

### KAN-6 — DEV portal

**Type**: Story  
**Status**: To Do  
**Link**: KAN-7 **blocks** KAN-6 (KAN-6 is blocked by KAN-7)  
**Impact Assessment**: Sole formal requirements source (AC1–AC7 + feature narrative). Testing of KAN-7 is effectively validation of KAN-6 registration journeys.  
**Relevant Details**: Two registration paths (coupon vs product access), coupon validation (valid/invalid), review page, data retention across steps.

No parent Epic, no other links, no sub-tasks.

---

## 4. Attachments

None on KAN-7 or KAN-6. No files downloaded to `context/attachments/`.

---

## 5. Project Knowledge

| Source | Result |
|--------|--------|
| `docs/` | Not present in sparse checkout / empty |
| `specs/` | Not present / empty |
| `knowledge/` | Empty at session start (no prior HID Developer Portal notes in this repo) |
| User-named spec in comments | None |

Historical repo artifacts under `QA Artifacts/AG/` (AG-1, AG-3) are unrelated (AMP Admin Portal / empty task) and were not used as requirements for KAN-7.

---

## 6. Figma Designs

No Figma designs linked

---

## 7. Environment / Credentials notes

| Item | Value |
|------|-------|
| Base URL | https://webportal.qa.developercommunity.hidcloud.com/login |
| Test email | shruthi00277@gmail.com |
| Password | Present in Jira KAN-7 description only — **not stored in git artifacts** |
| Auth model | Portal login page (email/password implied by description) |

---

## 8. UI Terminology & Navigation Map

Limited — no Figma, no product docs. Derived only from KAN-6 wording and the login URL.

### 8a. Screen / Page Inventory

| Screen | Navigation (known) | Notes |
|--------|-------------------|-------|
| Login | Open https://webportal.qa.developercommunity.hidcloud.com/login | Entry URL from KAN-7 |
| Create Account | Unknown path from Login — **confirm in grooming** | AC1 |
| Coupon registration path | Unknown step sequence | AC2, AC4, AC5 |
| Product access workflow | Unknown steps/fields | AC3 |
| Review | Appears before final submission | AC6, AC7 |

### 8b. Key UI Elements

| Element | Type | Screen | Interaction |
|---------|------|--------|-------------|
| Coupon code field | field | Registration (coupon path) | enter text — exact label unknown |
| Invalid coupon error | message | Registration (coupon path) | displayed on invalid code — exact copy unknown |
| Review summary fields | read-only fields | Review | display entered details — field list unknown |
| Submit / Continue controls | button | Multiple | labels unknown |

### 8c. Terminology Glossary

| Generic term | Product term (confirmed) |
|--------------|--------------------------|
| Developer registration portal | HID Developer Portal / Developer Community web portal |
| Coupon registration | coupon-based registration process (KAN-6) |
| Product request path | product access workflow (KAN-6) |

---

## 9. Open Questions / Gaps (preliminary)

1. Exact navigation from Login → Create Account (AC1).
2. Valid coupon code(s) for QA env (AC2/AC4).
3. Exact invalid-coupon error text (AC5).
4. Product access workflow steps, fields, and success criteria (AC3).
5. Review page field inventory (AC6/AC7).
6. Whether login credentials on KAN-7 are for an existing account or for post-registration sign-in only.
7. Relationship intent of "KAN-7 blocks KAN-6" (testing gate vs dependency modeling).

See `.state/qa-tracker-KAN-7.md` after grooming phase for formal Q/A/R IDs.
