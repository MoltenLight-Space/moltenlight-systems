# Phase 0 — Mission Analysis

This folder holds the artifacts that **exit Phase 0 at the Mission Definition
Review (MDR)**. Phase 0 is where the project is *framed* — what problem it
solves, for whom, under what constraints, and whether it is feasible to
proceed. No requirements are derived here; those are Phase A work.

## Deliverables

| # | Deliverable | File | Status |
|---|-------------|------|--------|
| 1 | Mission Statement | [mission-statement.md](mission-statement.md) | Draft |
| 2 | Stakeholder Analysis | [stakeholder-analysis.md](stakeholder-analysis.md) | Draft |
| 3 | Concept of Operations | [conops.md](conops.md) | Draft |
| 4 | Operational Needs (SDoc) | [operational-needs.sdoc](operational-needs.sdoc) | Skeleton |
| 5 | Critical Technologies | [critical-technologies.md](critical-technologies.md) | Skeleton |
| 6 | Feasibility Assessment | [feasibility-assessment.md](feasibility-assessment.md) | Skeleton |
| 7 | Business Case | [business-case.md](business-case.md) | Skeleton |

Supporting artifacts, elsewhere in the repo but required at MDR:

- Risk register populated with initial entries — [`../../risks/risk-register.md`](../../risks/risk-register.md)
- Methodology decision recorded — [`../../decisions/ADR-000-se-methodology.md`](../../decisions/ADR-000-se-methodology.md)
- ADR recording the decision to proceed to Phase A — **TODO**, written at MDR

## MDR exit criteria

The Mission Definition Review is passed when:

1. All seven deliverables above are in a reviewed state (not "Draft").
2. The initial risk register has at least ten entries, each with a scored
   likelihood × consequence and an identified owner.
3. A go/no-go decision to enter Phase A has been recorded as an ADR, with
   rationale that references the feasibility assessment and business case.
4. Critical technologies are each assigned a current TRL and a planned
   TRL-maturation activity before the relevant design phase.

## What Phase 0 is NOT

- **Not requirements.** The word "shall" has no place in these documents.
  Phase 0 captures *needs* in natural language; Phase A turns them into
  `STNR-*` and `SYSR-*` statements in StrictDoc.
- **Not architecture.** Any architectural choice mentioned here (Newtonian,
  alt-az, spin casting) is a **scoping assumption**, not a derived answer.
  These get tested in Phase A/B trade studies before they become binding.
- **Not a schedule.** Effort estimates, if any, are order-of-magnitude and
  live only in the business case.
