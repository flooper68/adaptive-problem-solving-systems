# Adaptive Problem-Solving Systems repository

This repository contains both the Adaptive Problem-Solving Systems (APSS)
framework and the APSS implementation used to evolve it. The two are kept
separate so the produced artifacts are not confused with the work and processes
that produce them.

## Use the artifacts

- [Framework definition](artifacts/framework/README.md) — the normative APSS
  specification, schema, template, and visualization contract.
- [Implementation examples](artifacts/examples/README.md) — non-normative
  examples that demonstrate how the framework can be applied.

## Inspect or operate the producing system

- [SYSTEM.md](SYSTEM.md) — declaration of the APSS Framework Stewardship System.
- [Current plan](operations/work/PLAN.md) and
  [work log](operations/work/LOG.md) — committed work and durable execution
  history.
- [Backlog](operations/work/backlog/README.md) — captured, ready, or deferred
  ideas that have not been selected into the current plan.
- [Backlog intake](operations/processes/backlog-intake.md) and
  [grooming](operations/processes/backlog-grooming.md) — the path from an idea
  to an explicit disposition and possible planning commitment.
- [Framework operating loop](operations/processes/framework-loop.md) —
  execution, validation, learning, adaptation, and release orchestration.
- [Compiled knowledge](operations/knowledge/README.md) — reusable stewardship
  lessons derived from evidence.

## Repository map

```text
artifacts/   Outputs produced for APSS consumers
operations/  Processes, work, evidence, validation, and learning
SYSTEM.md    Contract connecting the operating system to its artifacts
```

The framework is the primary artifact. Examples are supporting artifacts. A
file under `operations/` describes how the repository is run; it is not a
normative APSS requirement unless the framework artifact explicitly adopts it.
