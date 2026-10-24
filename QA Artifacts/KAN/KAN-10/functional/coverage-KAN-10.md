# Coverage Verification — KAN-10

**Date**: 2026-10-24  
**Requirement Story**: KAN-8  
**Testing Task**: KAN-10

## AC Coverage Matrix

| AC | Acceptance Criterion | In Scope? | Covered By | Status |
|----|---------------------|-----------|------------|--------|
| AC1 | Create Account page loads successfully and is accessible to users. | Yes | TC-001–TC-007, TC-035 | COVERED |
| AC2 | Users can complete registration using a valid coupon code. | No (out of scope) | — | N/A |
| AC3 | Users can complete registration through the product access workflow. | Yes | TC-008–TC-024, TC-034, TC-036–TC-037 | COVERED |
| AC4 | Valid coupon codes are accepted and allow users to continue the registration process. | No (out of scope) | — | N/A |
| AC5 | Invalid coupon codes display an appropriate validation error message. | No (out of scope) | — | N/A |
| AC6 | Review page displays all entered registration details before submission. | Yes | TC-025–TC-028, TC-033–TC-034, TC-038 | COVERED |
| AC7 | Registration details entered by the user are retained and accurately displayed throughout the registration journey. | Yes | TC-027, TC-029–TC-033, TC-038 | COVERED |

## UI Surface Coverage Matrix

| Page/Component | Positive TCs | Negative TCs | Boundary TCs | Error TCs | Status |
|----------------|--------------|--------------|--------------|-----------|--------|
| Login → Create Account | TC-001,003,005–007,035 | TC-002 | — | — | COVERED |
| Product Access option / details | TC-008,010,014,016,018–021,036 | TC-009,011–013,015,022–023 | TC-017 | TC-024,037 | COVERED |
| Review | TC-025,027–034,038 | TC-026 | — | — | COVERED |
| Success / confirmation | TC-008,018–020,034,036 | TC-023–024 | — | — | COVERED |
| Coupon path | — | — | — | — | N/A (out of scope) |

## Gaps

None for in-scope ACs. Exact Product Access field labels remain discovery items on live QA (documented in context G-006) — TCs use “required Product Access fields” and value-parity assertions.

## Result

**PASS** — proceed to publish.
