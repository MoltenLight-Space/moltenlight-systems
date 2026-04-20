# Mission Statement

!!! note "Status"
    **Draft, v0.1.** Phase 0 artifact. To be reviewed at MDR.

## Mission

Molten Light exists to demonstrate that a **1 m-class research-grade primary
mirror can be produced outside the conventional aerospace supply chain** —
by a small team, from borosilicate, through vertical-axis spin casting rather
than CNC figuring of a ground blank — and to integrate that mirror into a
**fully autonomous alt-az Newtonian robotic telescope** whose design,
construction, and operation are a publicly accessible engineering record.
The long-term vision of the project is **AirBnObservatory**: a remotely
bookable public observatory that turns this instrument into a shared resource
for amateur astronomers, educators, and citizen scientists.

## Objectives

1. **Produce a 1 m (nominal) borosilicate honeycomb primary** via vertical-axis
   spin casting, achieving λ/8 to λ/20 figure after sub-aperture finishing and
   sub-nm RMS surface roughness.
2. **Integrate the mirror** into a Newtonian optical tube assembly on an alt-az
   mount, with tracking performance sufficient for its seeing-limited regime
   at the chosen site.
3. **Operate the instrument autonomously**, including scheduling, weather-safe
   open/close, fault handling, and remote user access.
4. **Publish the full engineering record** — requirements, architecture,
   analyses, trade studies, verification results — under an open licence, in a
   form that a competent engineer outside the project could re-execute.
5. **Serve public users** by the end of the programme through a booking
   interface, with an operational policy appropriate to the site and the
   legal/insurance framework in force.

## Success criteria

The project is considered successful when **all** of the following are true:

- A mirror meeting objective 1 has been produced and its figure and roughness
  have been verified by an accepted metrology procedure.
- The assembled telescope has recorded an on-sky diffraction-limited
  double-star separation at the predicted resolution, under site-typical
  seeing, in at least one reviewed observing run.
- The autonomous control stack has completed at least **N** (TBD, Phase A)
  consecutive unattended observing sessions without human intervention beyond
  scheduled maintenance.
- The public engineering record is complete, internally consistent, and has
  survived at least one external technical review (peer, workshop, or
  equivalent).

## Out of scope

- **Space-qualification** of the mirror or any subsystem — this is a
  ground-based instrument; launch, thermal-vacuum, and radiation environments
  are explicitly not considered.
- **Diffraction-limited imaging beyond seeing.** Adaptive optics is not in
  the baseline; the system targets seeing-limited performance.
- **Research-grade spectroscopy or polarimetry** as baseline instruments.
  An instrument port is provided; specific science instruments beyond a
  primary imaging camera are deferred.
- **Commercial production** of mirrors. The process is documented so others
  can replicate it, but Molten Light is not itself a manufacturing business.

## Lifetime

- **Phase 0 → Phase E (commissioning)**: multi-year, solo-engineer cadence.
  Order-of-magnitude estimate, refined in the business case; not committed.
- **Operational life (Phase E)**: the instrument is expected to remain in
  service for at least a decade of autonomous observing, with scheduled
  maintenance and periodic recoating.
- **Disposal (Phase F)**: decommissioning considerations are deferred to the
  business case; siting dictates the removal obligations.

## Open issues

- **TODO** — Precise aperture. "1 m" is a target; the acceptable range is
  1.0–1.5 m per the engineering brief. Fix in Phase A after FEA constrains
  the thermal and structural budgets.
- **TODO** — Siting. The ConOps lists candidate dark-sky locations; the
  mission statement must eventually commit to one, as it drives the
  operational constraints (climate, access, legal framework).
- **TODO** — Public-access model. "Remotely bookable" implies a user policy,
  a liability framework, and a billing model (paid, donation, free). The
  business case and the stakeholder analysis must converge on one.
- **TODO** — "Fully autonomous" needs a sharper boundary. Recovery from a
  jammed focuser is different from recovery from a dome mechanical fault;
  the ConOps off-nominal scenarios need to enumerate what counts as
  autonomous recovery vs. dispatch of a human.
