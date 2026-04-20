# Critical Technologies

!!! note "Status"
    **Skeleton, v0.1.** Phase 0 artifact. To be populated before MDR.

This document identifies the technologies whose maturity materially drives
programme risk, assigns each a current **Technology Readiness Level (TRL)**,
and — for any technology below the TRL required at its relevant design phase
— records the maturation activity planned to close the gap.

TRL assignments use the ISO 16290 / ECSS-E-HB-11 nine-level scale. The
*relevant phase* is the phase at which the technology's current TRL must be
no lower than the value in the "Required TRL by" column to avoid becoming
critical-path.

## Template

Each entry below follows this structure:

- **What it is** — one-sentence functional description.
- **Why it is critical** — the specific programme risk the technology gates.
- **Current TRL** — defensible assessment, with the evidence source.
- **Required TRL by** — design phase and gate (e.g. "TRL 5 by PDR").
- **Maturation plan** — what activity will raise the TRL, and where in the
  repository that work is recorded.

## 1 — Spin-cast borosilicate honeycomb primary

- **What it is** — vertical-axis spin-cast molten borosilicate forming a
  paraboloid on its free surface, over an open-back honeycomb mould.
- **Why it is critical** — **TODO.** The single largest technical risk in
  the project; the method is the project's defining premise.
- **Current TRL** — **TODO.** Likely TRL 2–3 in Molten Light's own
  implementation despite higher TRL for related large-mirror spin-casting
  elsewhere; scale, tooling, and process are not directly transferable.
- **Required TRL by** — **TODO.**
- **Maturation plan** — **TODO.** Expect early-phase sub-scale castings.

## 2 — Bottom-only fire polishing

- **What it is** — reliance on the rotating free surface itself to
  fire-polish to sub-nm roughness, without a top radiant heater.
- **Why it is critical** — **TODO.** The engineering brief calls this
  "TBD" for effectiveness. If it fails, the process economics collapse.
- **Current TRL** — **TODO.**
- **Required TRL by** — **TODO.**
- **Maturation plan** — **TODO.**

## 3 — B₂O₃ volatilisation control in furnace atmosphere

- **What it is** — management of boric oxide evaporation from the borosilicate
  melt at process temperature, which otherwise changes composition and
  coats cooler surfaces.
- **Why it is critical** — **TODO.** Composition drift alters CTE, viscosity,
  and optical properties; deposited B₂O₃ attacks thermocouples and viewports.
- **Current TRL** — **TODO.**
- **Required TRL by** — **TODO.**
- **Maturation plan** — **TODO.** Atmosphere composition trade study listed
  as a programme open question.

## 4 — IPT (inductive power transfer) vs slip rings for rotor power

- **What it is** — contactless inductive power delivery to the rotating
  furnace, as an alternative to slip rings.
- **Why it is critical** — **TODO.** Drives vibration transmission,
  contamination risk, cost, and controllability.
- **Current TRL** — **TODO.** IPT as a generic technology is TRL 9; for this
  specific high-temperature, high-cleanliness application it is lower.
- **Required TRL by** — **TODO.**
- **Maturation plan** — **TODO.** Trade study is listed as pending in the
  engineering brief.

## 5 — Bath interferometry at 1 m aperture

- **What it is** — home-built common-path Bath interferometer scaled up
  from the typical amateur ATM size range to a 1 m mirror.
- **Why it is critical** — **TODO.** Metrology defines what "done" means.
  If the metrology is not trustworthy, the figure claim is not defensible.
- **Current TRL** — **TODO.** Well-established at small aperture; scaling to
  1 m raises beam-geometry and vibration-isolation issues.
- **Required TRL by** — **TODO.**
- **Maturation plan** — **TODO.** See the metrology strategy in
  `moltenlight-notebook/03 - Mirror System/03d - Metrology/`.

## 6 — Protected aluminium coating (Al + MgF₂) by resistive boat

- **What it is** — in-house deposition of a protected-aluminium coating on
  the finished mirror, with resistive-boat evaporation source and MgF₂
  overcoat.
- **Why it is critical** — **TODO.** The last operation before on-sky use;
  a failure here wastes every prior phase. Recoating cadence also drives
  operational maintenance policy.
- **Current TRL** — **TODO.**
- **Required TRL by** — **TODO.**
- **Maturation plan** — **TODO.**

---

**TODO (overall):** populate each row above during the MDR preparation
session. Any technology identified as critical here that is *below* its
required TRL must have a corresponding risk in the risk register.
