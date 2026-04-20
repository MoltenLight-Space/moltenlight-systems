# Risk Register

A single system-level register is kept here. Per rule 2 of the overhead-
reduction policy, the register will only be split per subsystem once more
than ten subsystem-specific risks are active in any one subsystem. Until
then, every risk lives in [`risk-register.md`](risk-register.md).

## Scoring

Each risk carries a **Likelihood** and a **Consequence** score on a 1-to-5
scale, with the product recorded as the **Score**.

**Likelihood (L):**

| L | Label | Meaning |
|---|-------|---------|
| 1 | Rare | Unlikely to materialise in this programme. |
| 2 | Unlikely | Has materialised in similar programmes but not expected here. |
| 3 | Possible | Plausible given current evidence. |
| 4 | Likely | Expected at least once on current trajectory. |
| 5 | Almost certain | Will materialise unless mitigated. |

**Consequence (C):**

| C | Label | Meaning |
|---|-------|---------|
| 1 | Negligible | Absorbed in scheduled work, no artifact change. |
| 2 | Minor | Local rework; no schedule or scope impact above one phase-internal cycle. |
| 3 | Moderate | Rework across one subsystem or one-phase delay. |
| 4 | Major | Multi-subsystem rework, phase-level delay, or stakeholder-visible impact. |
| 5 | Severe | Programme viability threatened; mission statement invalidated. |

**Score = L × C.** Risks with Score ≥ 12 are reported at every review gate.

## Escalation

- Any risk opening at **Score ≥ 15** triggers an ADR decision within the
  same working session.
- Any risk crossing the Score ≥ 15 threshold after opening triggers an
  immediate review of the affected subsystem architecture.
- Closed risks are retained in the register with status `Closed` and the
  closure date; they are not deleted, so that reviewers can reconstruct
  the history.

## Split rule

When the number of open *subsystem-specific* risks in any one subsystem
exceeds **ten**, the register is split: a subsystem register is created
under `docs/subsystems/<subsystem>/risks/`, and only cross-cutting or
system-level risks remain here. The split is recorded as an ADR.

## UID convention

`RISK-NNN`, monotonic across the whole project, not reset per subsystem.
Closed risks keep their UID — new risks get the next free number.
