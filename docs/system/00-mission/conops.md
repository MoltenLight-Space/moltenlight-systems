# Concept of Operations

!!! note "Status"
    **Draft, v0.1.** Phase 0 artifact. To be reviewed at MDR.

This ConOps describes how the Molten Light telescope is operated in its
intended end-state — a remotely bookable autonomous observatory. It is
written from the perspective of the instrument as a whole, not any single
subsystem. Subsystem ConOps (if needed) are Phase B artifacts.

## Operational modes

Five top-level modes. Only one is active at a time.

| Mode | Entry condition | Primary activity | Exit condition |
|------|-----------------|------------------|-----------------|
| **Stowed** | Default state whenever not observing. | Instrument parked at safe attitude; dome/enclosure closed; drives powered down except for heartbeat. | Scheduler requests observation and all safety preconditions pass. |
| **Initialising** | Transition out of Stowed at start of an observing window. | Open enclosure; power-on drive electronics; run pointing model refresh; execute focus & collimation check. | All health checks pass → Observing; any failure → Safing. |
| **Observing** | Issued by the scheduler with a validated target plan. | Slew; track; acquire image; guide; download; iterate through target queue. | Queue complete, weather interrupt, safety interrupt, or user-requested hold. |
| **Safing** | Triggered by: weather alert, power anomaly, pointing fault, dome fault, watchdog timeout, or explicit operator command. | Stop tracking; slew to park; close enclosure; disable high-voltage rails; issue notifications; preserve logs. | Manual clear-to-resume, or safe-hold timer expiry and automatic retry per policy. |
| **Maintenance** | Entered only by explicit operator authorisation. | Human-in-loop. Mechanical work, optical cleaning, software updates, recoating campaigns. | Operator declares maintenance complete and re-arms the scheduler. |

State transitions are defined in the control subsystem design (Phase B). The
mode names above are binding: subsystem designs may not invent their own.

## Operational scenarios

### Scenario 1 — Public user books an observing session

A registered user selects a target or target list via the booking interface,
chooses an available window, and confirms. The scheduler validates the
window against site policy (elevation, moon avoidance, session length limits)
and weather forecast. At the start of the window, the observatory transitions
Stowed → Initialising → Observing. Data products and a session report are
made available to the user on completion. The user never directly commands
the mount.

### Scenario 2 — Weather interruption mid-session

During Observing, the weather subsystem asserts a "close" condition
(precipitation, excess wind, low dew-point margin, excess cloud, humidity
spike). The scheduler halts the current exposure, posts a notice to the
active user, and commands Observing → Safing. If conditions recover within a
configurable window and the user's booked time remains, operation resumes.
Otherwise the session is concluded and compensation policy (TODO, business
case) is applied.

### Scenario 3 — Autonomous survey (future capability, not baseline)

When no user is booked, the scheduler optionally runs background survey work
— e.g. photometric monitoring of a target list, or contribution to a
citizen-science campaign. Survey activity has lower priority than user
bookings and yields immediately if a booking begins. This is flagged as a
**future capability** and is out of scope for MDR acceptance.

### Scenario 4 — Scheduled maintenance

A maintenance window is blocked in the booking system. On arrival, the
operator explicitly requests Maintenance mode, which requires acknowledgement
of the interlock conditions (dome latched, drives disabled). Work
(cleaning, software update, realignment, recoating) is performed. Logs of
all maintenance actions are appended to the operations record.

### Scenario 5 — Fault and recovery

A fault (encoder disagreement, tracking error exceeds threshold, focuser
stall, controller watchdog) triggers Observing → Safing. The observatory
attempts one automated recovery per fault class per session. If recovery
fails, a notification is dispatched to the operator and the observatory
remains in Safing until cleared. "Fully autonomous" is bounded by the list
of faults the observatory is authorised to self-clear; that list is a
Phase B deliverable.

## Siting

The instrument is a **ground-based, fixed-installation** optical telescope.
Siting decisions that frame every subsystem:

- **Dark-sky class**: candidate sites at Bortle 3 or better. Final class
  drives sky-brightness terms in the optical budget.
- **Altitude**: high enough for reduced air column and seeing; low enough for
  year-round road access.
- **Power**: grid-connected preferred; UPS mandatory; off-grid solar only
  if uptime targets can still be met.
- **Network**: broadband with a committed uptime SLA; the booking model
  requires it.
- **Access**: scheduled site visits for maintenance; not 24/7 crewed.

The actual site is an **open issue** and is deliberately not fixed at MDR.
Siting will be resolved during Phase A after trade studies against the
business case.

## Users and operators

- **User** — member of the public or an institution who books an observing
  session. Interacts only with the booking UI and the data-delivery interface.
  Holds no operational authority over the instrument.
- **Operator** — the principal (and later, potentially a small delegated
  group) who authorises Maintenance mode, clears faults, and has commit
  access to operational policy.
- **Maintainer** — operator acting under an explicit maintenance window.
  Physically present or remotely interlocked into the hardware.

## Operational constraints

- **Environmental**: the observatory operates in open-to-sky conditions only
  within a defined environmental envelope (temperature, humidity, wind,
  precipitation). Thresholds are set in the safety subsystem (Phase B).
- **Astronomical**: minimum target elevation, moon separation, and twilight
  constraints are enforced by the scheduler.
- **Regulatory**: any local permits (dark-sky, planning, electrical
  certification) are treated as hard operational preconditions.
- **Thermal settling**: the optical tube requires thermal equalisation before
  observations meet the error budget; an equalisation pre-period is included
  in the Initialising mode.
- **Recoating cadence**: aluminium coatings degrade; a recoating campaign is
  a scheduled Maintenance event, cadence TBD from coating analysis.

## Off-nominal operations

- **Loss of network** — observatory completes the current exposure, commands
  Safing, logs locally, resumes upload when connectivity returns.
- **Loss of grid power** — UPS holds long enough to execute Safing cleanly.
  If UPS depletes, controllers fail safe (parked, latched, unpowered).
- **Dome fault in open state** — highest-priority fault; if dome will not
  close, operator is alerted immediately and locally-hosted tarp/cover policy
  (TBD, not baselined) applies.
- **Collision / pointing runaway** — hardware limits are independent of
  software; breaching a limit cuts drive power.
- **Contaminated or damaged mirror** — observatory is taken out of service;
  recoating or repair campaign initiated.

## Open issues

- **TODO** — Define the maximum session length and inter-user slew/cooldown
  buffer. This is a scheduler input; it cannot be left open past Phase A.
- **TODO** — Specify the data-delivery model: raw frames, calibrated
  science frames, or both? Who owns the data? What is the retention policy?
- **TODO** — Decide the authorisation model for maintenance: single-factor
  (account), two-factor (account + physical key), or presence-only
  (interlocks only). This is both a security and a liability decision.
- **TODO** — Confirm the "autonomous recovery" fault list in Phase B.
  Mis-scoped autonomy is the single biggest source of operational risk.
- **TODO** — Resolve siting. Every open question above depends on it.
