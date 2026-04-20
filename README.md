# moltenlight-systems

**Systems engineering record for the Molten Light robotic telescope.**

Molten Light is a solo-engineer project to build a fully autonomous robotic
Newtonian telescope around a **1 m borosilicate honeycomb primary mirror** cast
in a vertical-axis spin furnace. The long-term vision — **AirBnObservatory** —
is a remotely bookable public observatory.

This repository is the flagship of the project: the **formal systems engineering
record**. Everything here is an engineering artifact under configuration control.
Exploratory thinking happens elsewhere (see *Related repositories*).

## Status

**Phase 0 — Mission Analysis.**
Working towards the **Mission Definition Review (MDR)**. The seven Phase 0
deliverables live under [`docs/system/00-mission/`](docs/system/00-mission/).
Phase A (Stakeholder & System Requirements) does not begin until MDR is passed.

## Methodology

- **Process standard:** ISO/IEC/IEEE 15288
- **Practitioner guidance:** INCOSE SE Handbook v5 (2023)
- **Space-domain tailoring:** ECSS-E-ST-10 — see [`docs/ecss-tailoring/`](docs/ecss-tailoring/)
- **MBSE (primary):** Eclipse Capella + ARCADIA method
- **MBSE (learning track):** SysML v2 via Eclipse SysON on one subsystem
- **Requirements management:** StrictDoc (`.sdoc`, Git-native, ReqIF export)
- **Documentation site:** MkDocs Material → `systems.moltenlight.space`

The methodology choice is recorded in
[`docs/decisions/ADR-000-se-methodology.md`](docs/decisions/ADR-000-se-methodology.md).

## Related repositories

All repositories live under the [`moltenlight-space`](https://github.com/moltenlight-space) GitHub organisation.

| Repository | Purpose |
|---|---|
| `moltenlight-systems` (this repo) | SE artifacts — requirements, Capella model, analyses, V&V, ECSS tailoring |
| `moltenlight-notebook` | Obsidian vault — exploratory / working notes |
| `moltenlight-hardware` | CAD, FEA meshes, PCBs (Git LFS) |
| `moltenlight-control` | Observatory software — INDI drivers, scheduler, booking UI |

## Licensing

Mixed, applied per artifact type:

- **Prose, diagrams, models** — Creative Commons Attribution-ShareAlike 4.0 (`LICENSE`)
- **Code snippets and build scripts in this repo** — Apache 2.0 (`LICENSE-CODE`)
- **Hardware** (in `moltenlight-hardware`) — CERN Open Hardware Licence Weakly Reciprocal v2 (CERN-OHL-W)
- **Observatory software** (in `moltenlight-control`) — Apache 2.0

## Contact

- Blog: [moltenlight.space](https://moltenlight.space)
- YouTube: [@moltenlight](https://youtube.com/@moltenlight)
