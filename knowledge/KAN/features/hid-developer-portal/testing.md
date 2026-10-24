# HID Developer Portal — Testing Notes

**Issues**: KAN-7 (Task — testing assignment), KAN-6 (Story — DEV portal requirements)  
**Updated**: 2026-10-24  
**Artifacts**: `QA Artifacts/KAN/KAN-7/context/`

## Summary

HID Developer Portal registration for developers via (1) coupon-based registration or (2) product access workflow, with coupon validation, a review step, and retention of entered details across the journey.

## Environment

- Login URL: https://webportal.qa.developercommunity.hidcloud.com/login
- Test email referenced on KAN-7: shruthi00277@gmail.com
- Passwords: store only in Jira — do not commit secrets here

## Areas to test (from KAN-6 AC1–AC7)

1. Create Account page accessibility/load
2. Registration with valid coupon
3. Registration via product access workflow
4. Valid coupon acceptance / continue
5. Invalid coupon validation error
6. Review page shows entered details
7. Data retention across registration steps

## Open must-questions

- Q-001 — valid coupon codes
- Q-002 — product access workflow definition
- Q-003 — Review fields + invalid coupon error copy

See `QA Artifacts/KAN/KAN-7/.state/qa-tracker-KAN-7.md`.
