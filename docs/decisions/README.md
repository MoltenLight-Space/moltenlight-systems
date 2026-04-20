# Architecture Decision Records (ADRs)

An **Architecture Decision Record** captures a single significant decision,
the context that led to it, and its consequences. ADRs are immutable once
accepted: if a decision is later reversed, a new ADR is written that
*supersedes* the earlier one, and the earlier one is marked accordingly.

## Numbering

ADRs are numbered sequentially with a three-digit zero-padded index:

```
ADR-NNN-short-kebab-case-title.md
```

The numbering is monotonic across the whole project and does not reset
per subsystem. At present a single ADR log is kept at the system level.
Per rule 2 of the overhead-reduction policy, it will only be split per
subsystem if volume demands it.

## When to write an ADR

Write an ADR when a decision:

- narrows the design space in a way that is costly to reverse,
- selects between methodologies, frameworks, or tools that affect the rest
  of the project,
- resolves a trade study, or
- formally commits to an architectural property (e.g. alt-az vs equatorial,
  Newtonian vs Ritchey–Chrétien).

Do **not** write an ADR for routine working choices (e.g. a variable name,
a build-script refactor, a version bump).

## Status values

- **Proposed** — authored but not yet accepted.
- **Accepted** — in force.
- **Superseded by ADR-NNN** — no longer in force; pointer to the replacement.
- **Deprecated** — no longer in force, with no replacement (rare).

## Template

Each ADR follows a fixed structure: Context, Decision, Status, Consequences,
and optionally Alternatives Considered and References. See `ADR-000-se-methodology.md`
for the concrete form.
