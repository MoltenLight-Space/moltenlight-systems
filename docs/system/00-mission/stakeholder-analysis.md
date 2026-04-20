# Stakeholder Analysis

!!! note "Status"
    **Draft, v0.1.** Phase 0 artifact. To be reviewed at MDR.

This document identifies the stakeholders whose needs, interests, or authority
bear on the project, classifies them by interest and influence, and records
the intended engagement strategy for each. Derived stakeholder *requirements*
(`STNR-*`) will be written in Phase A as a separate artifact; this document
captures only the people and organisations from which those requirements will
ultimately be drawn.

## Register

| # | Stakeholder | Description | Needs / Interests |
|---|-------------|-------------|--------------------|
| 1 | **Principal (project lead)** | The solo aerospace engineer delivering the project. | Credible engineering record; career-portable credential; personal technical satisfaction; sustainable workload. |
| 2 | **Amateur astronomer community** | ATM (amateur telescope making) practitioners, observing clubs. | Reproducible mirror-making method; honest discussion of limits; access to observing time. |
| 3 | **Educators** | School, university, and informal-science-education staff. | Teaching-grade access to a real instrument; age-appropriate documentation; data that students can reduce. |
| 4 | **Citizen scientists** | Hobbyist observers contributing to variable-star, exoplanet-transit, or asteroid programmes. | Calibrated data products; scheduled target windows; persistent archive. |
| 5 | **Content audience** | Readers of moltenlight.space and viewers of @moltenlight on YouTube. | Engaging, honest narrative; technical depth; continuity. |
| 6 | **Open-source contributors** | Potential contributors to `moltenlight-control`, Capella model, StrictDoc spec. | Clear contribution guide; ADRs explaining *why*; stable repo structure. |
| 7 | **Site owner / host** | Owner of the land or property where the observatory is eventually sited. | Non-intrusive installation; liability cover; clear revenue/use model. |
| 8 | **Regulators** | Planning authorities, electrical inspectors, dark-sky authorities where applicable. | Compliant installation; permit documentation; safety case. |
| 9 | **Neighbours** | Residents or landowners near the siting location. | Low visual impact; no noise; no light spill; respectful communication. |
| 10 | **Professional astronomy community** | Researchers, observatory engineers, survey-network operators. | Credible performance claims; openness to data-sharing; no misuse of professional terminology. |
| 11 | **Collaborators** | Pro-bono engineers, interns, students contributing specific work packages. | Scoped work packages; mentorship; visible credit; licence clarity. |
| 12 | **Insurers & legal counsel** | Those who will underwrite or advise on public-access operation. | Risk register; operational SOPs; evidence of due diligence; incident history. |

## Interest × Influence classification

Using the classical four-quadrant grid (monitor / keep informed / keep
satisfied / manage closely):

| Influence \ Interest | **Low interest** | **High interest** |
|---|---|---|
| **Low influence** | *Monitor* — neighbours (9, when remote), professional astronomy (10) | *Keep informed* — amateur astronomers (2), educators (3), citizen scientists (4), content audience (5), OSS contributors (6) |
| **High influence** | *Keep satisfied* — regulators (8), insurers & legal (12), neighbours (9, when local) | *Manage closely* — principal (1), site owner (7), collaborators (11) |

Placement is tentative and will be revisited at MDR with a proper
influence-vs-interest plot once the siting decision narrows — several
entries (neighbours in particular) move between quadrants depending on the
site chosen.

## Engagement strategy

- **Manage closely** — direct, documented communication. The principal is
  the project's own first user; every decision is logged. Site owner and
  named collaborators get formal agreements before any binding commitment.
- **Keep satisfied** — regulators and insurers are engaged *early*, with
  documentation drawn from this repository. The ECSS tailoring matrix and
  the risk register are the primary artifacts to present.
- **Keep informed** — the three-layer content architecture (research logs,
  concept videos, build videos) is the engagement channel. Cadence is set
  in the content strategy, not here.
- **Monitor** — the professional astronomy community is reached passively
  through publications and public code; active outreach is deferred until
  on-sky performance is demonstrable.

## Open issues

- **TODO** — Decide whether the site owner is the principal (own land),
  a third-party host (lease), or a partner institution (shared facility).
  This reshapes stakeholders 7, 8, 9, and 12 materially.
- **TODO** — Identify specific educators and citizen-science programmes
  to approach during Phase B. Generic categories here must become named
  organisations before they can drive requirements.
- **TODO** — Determine whether any stakeholder (most plausibly, an
  educational partner) becomes a *customer* in a contractual sense, which
  would promote selected `STNR-*` items to a higher level of formality.
- **TODO** — Capture the *engineering peer reviewer(s)* who will sign off
  on the external technical review called out in the mission statement.
