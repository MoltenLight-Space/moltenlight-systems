# ECSS Tailoring — Rationale

!!! note "Status"
    **Skeleton, v0.1.** One-to-two-sentence rationale per standard,
    ported from the project context. Deeper discussion — where the
    standard's requirements are tailored down and why — is **TODO**
    and will be filled in alongside the review of each standard.

## ECSS-E-ST-10 — System engineering

Core SE lifecycle and process framework. This is the anchor standard for
the whole project; everything else is structured around it.

**TODO** — describe which clauses are adopted verbatim and which are
interpreted in a solo-engineer context (e.g. review-panel composition).

## ECSS-E-ST-10-02 — Verification

Defines the V&V method, evidence types, and closure criteria. The project's
figure, pointing, and software acceptance all need a traceable verification
method; this standard supplies one without invention.

**TODO** — map each top-level success criterion from the mission statement
to an ECSS-E-ST-10-02 verification method (test / analysis / inspection /
demonstration / review-of-design).

## ECSS-E-ST-10-06 — Technical requirements

Defines requirement writing rules, attributes, and traceability. StrictDoc's
native model maps cleanly onto these rules — adopting the standard costs
little and buys a defensible requirements artifact.

**TODO** — confirm the StrictDoc grammar covers every mandatory attribute
in -10-06; list any supplementary attributes introduced locally.

## ECSS-E-ST-32 — Structural engineering

FEA methodology and margin-of-safety philosophy for structural analyses.
The mirror blank, OTA, mount, and enclosure are all structural; adopting a
common methodology across them is cheaper than inventing one.

**TODO** — identify which -32 clauses on launch dynamic environments are
explicitly excluded as SKIP-within-APPLY.

## ECSS-Q-ST-70 — Materials and processes

Covers material selection, traceability, and process qualification for
critical components. Glass composition, BN coatings, mullite refractories,
and aluminium coatings all fall here.

**TODO** — list the specific processes being qualified under this standard
and the evidence type planned for each.

## ECSS-E-ST-10-09 — Interface management

Interface Control Documents as the contract between subsystems. Full ECSS
formality would be disproportionate at this scale; the standard is used as
a template and ICDs are kept as concise one-page documents.

**TODO** — catalogue the inter-subsystem interfaces and state which will
have full ICDs and which will be described inline in subsystem docs.

## ECSS-E-ST-10-12 — Methods and tools (MBSE)

Guidance on SysML modelling and MBSE tool use. Applied to Capella/ARCADIA
as the primary tool and SysML v2 as the secondary (learning-track) tool.

**TODO** — state the project's adopted modelling rules (naming,
decomposition depth, viewpoint use) derived from -10-12 guidance.

## ECSS-E-ST-40 — Software engineering

Software process standard. Scaled down for open-source, single-repo
development: the control stack lives in `moltenlight-control` under
Apache 2.0, with CI-driven quality gates replacing formal inspection.

**TODO** — enumerate which -40 software-product-assurance clauses are
adopted, which are tailored, and which are skipped.

## ECSS-M-ST-10 — Project planning

WBS, schedule, and risk-management structure. Applied at an appropriate
scale: a single WBS at system level, risk register as one document, no
earned-value management.

**TODO** — record the WBS structure chosen and its mapping to repository
folders.

## ECSS-Q-ST-20 — Quality assurance

Non-conformance process, test/inspection templates, configuration control.
Proportionate QA for a single-article build: configuration control is
delivered by Git; NCRs are tracked as issues with a fixed label.

**TODO** — define the NCR workflow (open → investigate → disposition →
close) in enough detail to be auditable.
