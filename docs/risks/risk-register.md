# Risk Register

!!! note "Status"
    **Draft, v0.1.** Phase 0 artifact. Opening entries drawn from the
    "KEY PHYSICS CHALLENGES" and TBDs in the engineering brief and from
    the stakeholder-analysis open issues. To be reviewed at MDR.

Scoring scheme and escalation policy are in [`README.md`](README.md).
Legend: `L` = likelihood (1–5), `C` = consequence (1–5), `Score = L × C`.

| RISK-ID | Title | Category | L | C | Score | Mitigation | Owner | Status | Opened |
|---------|-------|----------|:-:|:-:|:-----:|------------|-------|--------|--------|
| RISK-001 | Fire polishing ineffective with bottom-only heating | Technical — mirror process | 4 | 4 | 16 | Characterise free-surface roughness in sub-scale castings with varied hold times and bottom-zone power profiles before committing to the 1 m furnace design. Fallback: add radiant top-side heating, accepting furnace-architecture rework. | Principal | Open | 2026-04-20 |
| RISK-002 | B₂O₃ volatilisation shifts composition and contaminates instrumentation | Technical — mirror process | 4 | 3 | 12 | Close the furnace-atmosphere TBD in Phase A: select between inert overpressure, dry-air, or partially closed environments. Qualify sacrificial thermocouple shielding. Monitor composition via periodic melt sampling in sub-scale runs. | Principal | Open | 2026-04-20 |
| RISK-003 | Radial T<sub>g</sub> crossing drives figure error beyond λ/5 from oven | Technical — mirror process | 4 | 4 | 16 | Thermal FEA-driven zone count and cascade control design. Pre-commission the thermal-camera-plus-zone-thermometry loop on an inert dummy load before first casting. | Principal | Open | 2026-04-20 |
| RISK-004 | Rotational instability during vitrification corrupts paraboloid figure at nm scale | Technical — mirror process | 3 | 5 | 15 | Specify bearing and drive as a matched set with measured ω jitter below the FEA-derived threshold. Instrument rotor with redundant ω sensing during casting. Commit only after demonstrating stability on a cold-rotor test rig. | Principal | Open | 2026-04-20 |
| RISK-005 | IPT option transmits unacceptable vibration to rotor | Technical — furnace | 3 | 3 | 9 | Resolve the IPT-vs-slip-ring trade study in Phase A with measured vibration spectra from candidate hardware. Carry both options through to PDR if the trade is close. | Principal | Open | 2026-04-20 |
| RISK-006 | Residual stress from fictive-temperature distribution distorts figure on demolding | Technical — mirror process | 4 | 4 | 16 | Design the cooling profile explicitly for fictive-temperature homogeneity, not just thermal-gradient reduction. Model residual stress in thermal FEA. Include a sacrificial demolding trial in the casting campaign. | Principal | Open | 2026-04-20 |
| RISK-007 | Gravitational sag on rotation stop exceeds honeycomb stiffness budget | Technical — mirror structural | 3 | 4 | 12 | Size honeycomb cell and facesheet via structural FEA against sag above the strain point. Confirm the support-transfer sequence (tungsten rods → operational support) is complete before the strain point is crossed. | Principal | Open | 2026-04-20 |
| RISK-008 | Tungsten support rods act as thermal shorts and perturb the radial gradient | Technical — furnace interface | 3 | 3 | 9 | Include the tungsten rods in the thermal FEA as geometry, not as idealised point supports. Iterate rod count and diameter against the same thermal-budget constraint that drives zone design. | Principal | Open | 2026-04-20 |
| RISK-009 | Solo-engineer single point of failure halts the programme | Programmatic | 3 | 5 | 15 | Maintain the engineering record at publication-grade completeness at all times. Identify and brief at least one external technical reader per subsystem. Explicit handover documentation kept current, not written retrospectively. | Principal | Open | 2026-04-20 |
| RISK-010 | Scope creep from AirBnObservatory vision dilutes the mirror-delivery path | Programmatic — scope | 4 | 3 | 12 | Freeze the mission statement and objectives at MDR. Gate AirBnObservatory-specific work behind Phase C entry. Record any vision-driven scope change as an ADR, not a silent requirement edit. | Principal | Open | 2026-04-20 |

## Notes

- All ten opening risks have the principal as owner, reflecting the
  solo-engineer programme structure. Owner assignments will be revisited
  when collaborators are onboarded.
- No risk is currently `Closed`. The earliest realistic closure is
  RISK-005 (IPT vibration), conditional on the Phase A trade study.
- RISK-001, RISK-003, and RISK-006 are the dominant mirror-process risks
  and will each be associated with a critical technology entry in
  [`../system/00-mission/critical-technologies.md`](../system/00-mission/critical-technologies.md)
  once that document is populated.
