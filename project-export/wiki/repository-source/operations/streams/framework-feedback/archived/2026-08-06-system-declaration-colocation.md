---
id: apss.feedback.system-declaration-colocation
type: framework-feedback
status: groomed
received: 2026-08-06
reporter: APS framework maintainer
source: Maintainer-agent discussion in the current Claude Code session
related_feedback:
  - apss.feedback.problem-hierarchy-and-goal-ambiguity
related_work:
  - apss.colocate-system-declaration
---

# Separate verification and strategy files for the system are confusing; problems colocate them

## Report

### Context

The maintainer was reading the system declaration
[`operations/SYSTEM.md`](../../../SYSTEM.md), which links its verification to
[`processes/verification.md`](../../../processes/verification.md) and its strategy
to [`STRATEGY.md`](../../../STRATEGY.md) as separate files, following the
declaration template in [`framework/SCHEMA.md`](../../../../framework/SCHEMA.md).

### Observed problem or outcome

Having verification and strategy in files separate from the system declaration
is confusing. Problems already colocate these elements — a problem file such as
[`P1`](../../../problems/p1-finish-mvp-and-run-loop.md) carries its desired
outcome, signal, and strategy inline — so the system, as the root of the same
problem hierarchy, is the asymmetric case.

### Desired outcome

The main system holds its verification and strategy colocated with the
declaration, the same way problem files hold theirs.

### Suggested response

Colocate verification and strategy in `SYSTEM.md` rather than linking them as
separate files. Acting on this would touch the framework's declaration
contract: the [`SCHEMA.md`](../../../../framework/SCHEMA.md) template defines
`verification` and `strategy` as links to other files (`strategy: STRATEGY.md`
appears literally in the template), so the shape is currently prescribed, not
an Operations choice. Whether the contract should require, permit, or stay
silent on colocation is a grooming question.

### Evidence

Direct maintainer feedback from the current session. Supporting repository
state at the time of capture: the `verification: processes/verification.md` and
`strategy: STRATEGY.md` links in [`operations/SYSTEM.md`](../../../SYSTEM.md); the
template in [`framework/SCHEMA.md`](../../../../framework/SCHEMA.md) defining both
fields as links; and the colocated Desired outcome, Signal, and Strategy
sections in [`P1`](../../../problems/p1-finish-mvp-and-run-loop.md). Report and
repository observation; the suggested response is not independently validated.

## Grooming record

### 2026-08-07 — act: task candidate captured

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Evidence consulted:** the linked declaration fields in
  `operations/SYSTEM.md`, the SCHEMA.md template, and P1's colocated
  Desired outcome, Signal, and Strategy sections as the worked precedent.
- **Assessment:** the asymmetry is real — problems colocate outcome, signal,
  and strategy while the root system links them out to separate files — and
  resolving it serves P1's understandability signal and strategy point 3.
  The change touches the compiled framework's declaration contract, so it
  needs a brainstorming session, not a grooming edit.
- **Disposition:** **act** — captured
  [`apss.colocate-system-declaration`](../../../tasks/colocate-system-declaration.md)
  as the bounded executable response for a brainstorming session. This
  decision also supplies the direction that closes
  [`apss.modular-system-concerns`](../../../tasks/archive/modular-system-concerns.md)
  as contradicted.
