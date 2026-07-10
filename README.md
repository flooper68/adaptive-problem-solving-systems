# Adaptive Problem-Solving Systems repository

This repository contains the Adaptive Problem-Solving Systems (APSS) framework,
examples of its application, and the operations system that improves it. These
are separate at the root so the normative framework is not confused with its
tests or with the work that produces it.

## Use APSS

- [Framework definition](framework/README.md) — the normative APSS
  specification, schema, template, and visualization contract.
- [Implementation examples](examples/README.md) — non-normative
  examples that demonstrate how the framework can be applied.

## Inspect or operate the producing system

- [Operations system declaration](operations/SYSTEM.md) — its problem, vision,
  current goal, strategy, boundary, roles, and adaptive loop.
- [Current plan](operations/work/PLAN.md) and
  [work log](operations/work/LOG.md) — committed work and durable execution
  history.
- [Backlog](operations/work/backlog/README.md) — captured, ready, or deferred
  executable candidates that have not been selected into the current plan.
- [Backlog intake](operations/processes/backlog-intake.md) and
  [grooming](operations/processes/backlog-grooming.md) — the path from a
  proposed action to an explicit disposition and possible planning commitment.
- [Working sessions](operations/processes/working-session.md) — conduct and
  retain bounded discussions or brainstorming without conflating their
  insights, questions, decisions, and candidate actions.
- [Framework feedback intake](operations/processes/framework-feedback-intake.md)
  and [grooming](operations/processes/framework-feedback-grooming.md) — report
  an experience with APSS, preserve it as evidence, and decide whether it
  warrants a separate work candidate.
- [Framework operating loop](operations/processes/framework-loop.md) —
  execution, validation, learning, adaptation, and release orchestration.
- [Knowledge compilation](operations/processes/knowledge-compilation.md) and
  [framework adaptation](operations/processes/framework-adaptation.md) — turn
  evidence into an approved, published framework artifact.

## Repository map

```text
framework/   Normative APSS definition produced by the operations system
examples/    Non-normative applications that explain and test the framework
operations/  System that improves the framework using evidence and learning
```

The repository itself is a container, not an APSS system. `operations/` is the
declared system; `framework/` is its primary artifact; and `examples/` contains
supporting artifacts. Operational choices are not normative APSS requirements
unless the framework explicitly adopts them.
