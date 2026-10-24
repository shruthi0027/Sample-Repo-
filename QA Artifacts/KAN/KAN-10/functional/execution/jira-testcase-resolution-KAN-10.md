# Jira Test Case Resolution — KAN-10

**Issue**: [KAN-10](https://busybug027.atlassian.net/browse/KAN-10)  
**Attachment scanned**: `test-cases-KAN-10.csv` (1 CSV; 0 Excel)  
**CSV source decision**: Jira attachment SHA-256 matched local `functional/test-cases-KAN-10.csv` — **kept local** (identical; no overwrite)  
**Resolution mode**: Local `TC-*` IDs only — no ALM lookup

## ID detection summary

| Pattern | Count | Action |
|---------|-------|--------|
| Local `TC-NNN` (`TC-001` … `TC-038`) | 38 | Use CSV / MD directly — no Jira or TestRail fetch |
| Jira issue keys as Test Case # | 0 | — |
| Numeric IDs as Test Case # | 0 | — |
| TestRail `C*` IDs as Test Case # | 0 | — |

`Requirement_ID` values such as `KAN-8` are requirement traceability only and were **not** treated as executable test-case IDs.

## Resolution log

| TC ID | Source | Issue/Case ID | Status | Title |
|-------|--------|---------------|--------|-------|
| TC-001 … TC-038 | Local CSV/MD | — | Resolved (local) | See `functional/test-cases-KAN-10.md` |

No Jira issues or TestRail cases were fetched for step expansion. Existing `functional/test-cases-KAN-10.md` and `functional/test-cases-KAN-10.csv` remain the execution sources.

## Notes

- Attachment filename: `test-cases-KAN-10.csv` (size 86549 bytes; content hash matches local).
- Expanded step rows in CSV: 261 (including 38 Preconditions rows).
- Unique test cases scanned: **38**.
