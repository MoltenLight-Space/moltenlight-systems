# Feasibility Assessment

!!! note "Status"
    **Skeleton, v0.1.** Phase 0 artifact. To be populated before MDR.

This assessment answers a single question: **is it defensible to enter
Phase A given what is currently known?** It is deliberately brief; depth
lives in the trade studies that will follow in Phase A.

## Technical feasibility

Addresses whether the concept — a 1 m spin-cast borosilicate honeycomb
primary in an autonomous alt-az Newtonian — is physically and engineeringly
achievable by the project team, given cited precedent and the critical
technologies catalogue.

- **TODO** — reference existing large-aperture spin-cast mirrors (Roger
  Angel / Steward Observatory Mirror Lab as the canonical precedent) and
  identify what *does* and *does not* transfer to a 1 m, solo-engineer
  scale.
- **TODO** — state the principal known unknowns: fire-polish quality with
  bottom-only heating; ω stability during vitrification at nm sensitivity;
  demolding stress from fictive-temperature gradients.
- **TODO** — confirm that each subsystem (mirror, OTA, mount, control) has
  at least one credible implementation path at this scale, citing
  commercially available elements where appropriate.

## Programmatic feasibility

Addresses whether the principal can execute the project within acceptable
bounds of time, cost, and attention, and whether critical dependencies
(facilities, suppliers, tooling) are available.

- **TODO** — order-of-magnitude schedule, refined in the business case.
  The solo-engineer cadence is a hard programmatic constraint; the
  schedule must be compatible with it or the project must scale its
  scope.
- **TODO** — order-of-magnitude cost envelope by top-level subsystem.
  Mirror (blank + furnace + metrology + coating) dominates. Mount and
  control are cost-known from commercial reference prices. Enclosure
  is site-dependent.
- **TODO** — identify suppliers and services whose unavailability would
  block the project: SiC heating elements, mullite refractories, optical
  metrology services, MRF/IBF figuring services, aluminium coating
  services (if not in-house).
- **TODO** — capture the single-person-single-point-of-failure risk and
  the mitigations being considered (written record, collaborator pool,
  explicit handover docs).

## Legal feasibility

Addresses whether the project can legally be constructed, operated, and
opened to public use at the intended scale, in the candidate sites under
consideration.

- **TODO** — planning and building-permit status for candidate sites
  (structure, enclosure, electrical).
- **TODO** — public-access legal framework: liability, insurance,
  consent, data protection for user bookings.
- **TODO** — export-control and licensing check: borosilicate glass,
  SiC elements, harmonic drives, optical coatings — none expected to be
  controlled, but this must be confirmed.
- **TODO** — open-licensing clarity: the CC BY-SA 4.0 / Apache 2.0 /
  CERN-OHL-W split must be reviewed for consistency before the project
  begins accepting third-party contributions in Phase A.

## Conclusion

- **TODO** — explicit go / no-go recommendation to enter Phase A, with
  the conditions (if any) under which go becomes no-go. This is the
  statement on which ADR-to-be-written ("Proceed to Phase A") will hang.
