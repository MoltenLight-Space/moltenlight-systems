# Molten Light Systems

This is the **formal systems engineering record** for the Molten Light robotic
telescope — a 1 m borosilicate honeycomb primary, spin-cast, driven by an
alt-az mount, fully autonomous, remotely bookable.

## Where the project is

**Phase 0 — Mission Analysis.** Working towards the Mission Definition Review
(MDR). Until MDR is passed, no Phase A requirements exist.

The seven Phase 0 deliverables, their current status, and the MDR exit
criteria are listed on the [Mission overview page](system/00-mission/README.md).

## How this site is organised

- **Mission (Phase 0)** — the artifacts being produced now.
- **Decisions** — Architecture Decision Records. `ADR-000` captures the
  systems engineering methodology choice.
- **Risks** — a single system-level register until volume demands a split.
- **Reviews** — milestone review reports (MDR, PRR, SRR, PDR, CDR, QR, AR).
  Empty for now; populated when a review actually happens.
- **ECSS Tailoring** — the APPLY / ADAPT / SKIP matrix and its rationale.

The requirements themselves are authored in [StrictDoc](https://strictdoc.readthedocs.io/)
and rendered under `/requirements/` when Phase A begins.

## Related work

This repository is the flagship of the [`moltenlight-space`](https://github.com/moltenlight-space)
organisation. Exploratory thinking lives in `moltenlight-notebook`; hardware
lives in `moltenlight-hardware`; observatory software lives in `moltenlight-control`.
