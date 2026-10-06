# Context: AG-3

**Title**: AMP Admin Portal
**Type**: Unknown (Jira issue fetch failed; not confirmed)
**Status**: Unknown (Jira issue fetch failed; not confirmed)
**Date**: 2026-10-06
**Parent Issue**: AG-3

> **Source note**: Jira MCP was unavailable and Jira REST authentication failed. Title, description, and AC1–AC12 are from the triggering comment, not live Jira fields.

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

## 6. Figma Designs

No Figma designs linked

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
