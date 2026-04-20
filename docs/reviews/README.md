# Reviews

Milestone review reports are filed here as each review actually occurs.
Per rule 1 of the overhead-reduction policy, **no individual review files
exist yet** — there is nothing to file until a review happens. This
document summarises the gates, their phase mapping, and the conventions
for filing when the time comes.

## Gates

| Gate | Name | Ends phase | Entry (condensed) | Exit (condensed) |
|------|------|------------|-------------------|-------------------|
| **MDR** | Mission Definition Review | Phase 0 | Seven Phase 0 deliverables drafted, risks opened, ADR-000 accepted. | Go / no-go to Phase A recorded as an ADR. |
| **PRR** | Preliminary Requirements Review | Phase A (mid) | Stakeholder requirements (`STNR-*`) drafted and traced to operational needs. | STNR baseline frozen; system requirements derivation authorised. |
| **SRR** | System Requirements Review | Phase A | System requirements (`SYSR-*`) complete and traced to STNR. Performance budgets drafted. | SYSR baseline frozen; system architecture work authorised. |
| **PDR** | Preliminary Design Review | Phase B | Subsystem requirements drafted; architecture consolidated; trade studies closed; interface control draft issued. | Detailed-design authorisation. |
| **CDR** | Critical Design Review | Phase C | Detailed design complete; FEA, thermal, and optical analyses closed; build drawings issued. | Authorisation to build. |
| **QR / AR** | Qualification Review / Acceptance Review | Phase D | Integration complete; V&V executed against the verification plan. | Authorisation to enter operations. |
| **FRR** | Flight / Field Readiness Review | Phase D → E | Site prepared; operational procedures dry-run; safety case signed. | Authorisation to commission on-site. |

TODO — extend this table with the exact ECSS-E-ST-10 wording and confirm
the tailoring (for example, whether QR and AR are merged given the single-
article build) at the point of drafting each review, not now.

## Filing convention (for future use)

When a review happens, a single report is added to this folder, named:

```
<GATE>-YYYY-MM-DD-report.md
```

with the structure:

- Summary (one paragraph)
- Entry criteria — met / not met, per item
- Exit criteria — met / not met, per item
- Actions (with owners and target dates)
- Decision (proceed / rework / abandon)
- Signatures (principal + any external reviewers)

Review reports are **immutable** after signing; any later change is a new
report that references the earlier one.

## Current status

No reviews filed. The next expected gate is **MDR**. Entry readiness is
tracked via the deliverables table in
[`../system/00-mission/README.md`](../system/00-mission/README.md).
