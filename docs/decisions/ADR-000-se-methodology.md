# ADR-000 — Systems Engineering Methodology

- **Status:** Accepted
- **Date:** 2026-04-20
- **Deciders:** Principal (solo)
- **Supersedes:** —
- **Superseded by:** —

## Context

Molten Light is a multi-year, cross-domain project — opto-mechanical, thermal,
control, software — executed by a single aerospace engineer, with the
engineering record itself as an explicit deliverable. A methodology choice
made now shapes every artifact that follows: it dictates the document set,
the tooling, the review cadence, and the vocabulary used with regulators,
insurers, and potential collaborators.

Three layered standards are available and non-equivalent:

- **ISO/IEC/IEEE 15288** is the *process* standard — roughly thirty SE
  processes grouped in four categories. It defines *what* processes exist
  but not how to execute them at any particular scale.
- **INCOSE SE Handbook v5 (2023)** is the practitioner guidance for
  executing 15288. It also supplies the commonly-cited lifecycle stage
  names, which are frequently misattributed to 15288 directly.
- **ECSS-E-ST-10** is the space-domain tailoring of 15288, adding the
  Phase 0/A/B/C/D/E/F structure, the MDR/PRR/SRR/PDR/CDR/QR/AR/FRR
  review gates, and document-deliverable conventions.

For MBSE, two serious free options exist: Eclipse Capella with the ARCADIA
method (Thales-originated, widely used at TAS, OHB, ArianeGroup, and in
ESA-funded programmes), and SysML v2, formally adopted by OMG on
30 June 2025 and supported by the free Eclipse SysON tool. For requirements,
StrictDoc provides plain-text `.sdoc` files, recursive discovery across
folders, ReqIF export, and native Git compatibility.

## Decision

Adopt the following stack:

1. **ISO/IEC/IEEE 15288 as the process standard**, executed using **INCOSE
   SE Handbook v5** as practitioner guidance.
2. **ECSS-E-ST-10 as the lifecycle tailoring**, with an explicit
   APPLY / ADAPT / SKIP matrix recorded under `docs/ecss-tailoring/`.
3. **Eclipse Capella + ARCADIA as the primary MBSE tool**, with the
   official System-to-Subsystem Transition add-on used (never bypassed)
   for subsystem model derivation in Phase B.
4. **SysML v2 via Eclipse SysON as a parallel learning track** applied to
   one subsystem, treated as a career-portable credential exercise rather
   than a project deliverable.
5. **StrictDoc as the requirements management tool**, with MID enabled,
   recursive scanning from the repository root, and UID conventions
   (`STNR-*`, `SYSR-*`, `MIR/OTA/MNT/CTL-*`, `RISK-*`, `ADR-NNN`) fixed
   at project level.

## Consequences

**Positive.**
The stack is entirely free and open-source, which is compatible with the
solo-engineer funding model. Every artifact is plain-text and Git-native,
which supports the "engineering record as deliverable" requirement — the
documentation site builds deterministically from source in CI. The
Capella + ARCADIA choice aligns with the aerospace professional pool the
principal already inhabits, and ECSS tailoring gives regulators and
insurers a familiar framework to audit.

**Negative.**
Capella has a learning curve; early models will be discarded. Running
SysML v2 in parallel is deliberate extra cost — an hour on SysON is an
hour not on Capella. StrictDoc is maturing rapidly but smaller in
community than DOORS or Polarion; documentation is good but tooling
around it is thinner.

**Neutral.**
This ADR fixes the *methodology*, not the *design*. Every subsequent
technical ADR is free to override within the methodology — for example,
the trade between alt-az and equatorial is a separate, later ADR. This
one only commits to *how* such decisions will be recorded.

## Alternatives considered

- **Cameo Systems Modeler** (paid, SysML v1). Rejected on cost and on
  the superior fit of ARCADIA for this project's cross-domain structure.
- **SysML v2 as the primary tool.** Rejected: tooling and the SSS-style
  decomposition story are not yet mature enough to be the project's sole
  modelling backbone. Retained as the learning track for portability.
- **No MBSE — prose-only engineering.** Rejected: the project is complex
  enough that traceability without a model is a false economy.
- **ECSS skipped entirely in favour of INCOSE alone.** Rejected: ECSS
  gives the lifecycle phases and review gates that anchor the whole
  schedule; removing them would require reinventing equivalent structure.

## References

- ISO/IEC/IEEE 15288:2023
- INCOSE Systems Engineering Handbook, 5th edition (2023)
- ECSS-E-ST-10C Rev.1 — System engineering general requirements
- Eclipse Capella — <https://www.eclipse.org/capella/>
- Capella System-to-Subsystem Transition add-on — <https://github.com/eclipse/capella-sss-transition>
- SysML v2 — OMG adoption 2025-06-30
- StrictDoc — <https://strictdoc.readthedocs.io/>
