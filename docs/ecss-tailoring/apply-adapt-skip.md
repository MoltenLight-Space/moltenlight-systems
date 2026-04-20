# ECSS Tailoring — APPLY / ADAPT / SKIP

!!! note "Status"
    **Draft, v0.1.** Phase 0 artifact. Ported from the project context.
    To be reviewed at MDR.

ECSS is a body of standards originally written for space-flight programmes.
Molten Light is a ground-based instrument built by a solo engineer — a much
smaller scale than ECSS's baseline audience. The sensible position is
therefore not "adopt ECSS wholesale" and not "ignore ECSS", but **tailor**:
adopt the core SE methodology directly, borrow selectively from peripheral
standards, and skip spacecraft-specific standards entirely.

Three decision categories are used:

- **APPLY** — adopt directly. The standard's text becomes project-binding.
- **ADAPT** — borrow selectively, scaling down in scope and formality to
  match project size and solo-engineer execution.
- **SKIP** — not applicable to a ground-based instrument.

Per-standard rationale lives in [`rationale.md`](rationale.md).

## APPLY — core SE methodology, adopt directly

| Standard | Title | Application |
|---|---|---|
| ECSS-E-ST-10 | System engineering | Full SE lifecycle, process framework, documentation structure. |
| ECSS-E-ST-10-02 | Verification | V&V plan for mirror figure, mount pointing, and software. |
| ECSS-E-ST-10-06 | Technical requirements | Requirements writing format and traceability method, implemented in StrictDoc. |
| ECSS-E-ST-32 | Structural engineering | Mirror FEA methodology, self-weight criteria, fatigue where relevant. |
| ECSS-Q-ST-70 | Materials and processes | Glass composition, BN coatings, refractories, aluminium deposition. |

## ADAPT — borrow selectively, scale down for project size

| Standard | Title | Application |
|---|---|---|
| ECSS-E-ST-10-09 | Interface management | Optical, mechanical, electrical, and software ICDs; one-page form per interface rather than full ECSS formality. |
| ECSS-E-ST-10-12 | Methods and tools (MBSE) | Guidance on SysML modelling and tool selection — applied to Capella/ARCADIA primarily and SysML v2 secondarily. |
| ECSS-E-ST-40 | Software engineering | Control system, scheduler, web UI — tailored for open-source single-repo development. |
| ECSS-M-ST-10 | Project planning | WBS, schedule, risk register — scaled to a solo engineer. |
| ECSS-Q-ST-20 | Quality assurance | Test and inspection procedure templates, non-conformance process — proportionate to a single-article build. |

## SKIP — out of scope

All spacecraft-specific standards, including but not limited to:

- AOCS / GNC (ECSS-E-ST-60 series beyond what is functionally relevant to
  tracking control)
- Propulsion (ECSS-E-ST-35)
- Launch and launch-environment qualification (ECSS-E-ST-32 dynamic
  environment clauses specific to launch)
- Space-environment radiation and thermal-vacuum qualification
  (ECSS-Q-ST-60 radiation hardness; ECSS-E-ST-10-04 space environment)
- Ground-segment standards written against orbital operations
  (ECSS-E-ST-70 series where not directly applicable to robotic observatories)

A ground-based autonomous telescope shares *method* with these standards
but not their *environment* or *scale*. Keeping them in scope would dilute
the tailoring without adding engineering value.

## Change control

Movement of a standard between categories — in particular, any standard
moving *out* of SKIP — requires an ADR. The tailoring matrix is a baseline
artifact, not a working document; ad-hoc edits are not permitted.
