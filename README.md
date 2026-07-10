# Adaptive Problem-Solving Systems repository

This repository contains the Adaptive Problem-Solving Systems (APSS) framework,
examples of its application, and the operations system that improves it. These
are separate at the root so the normative framework is not confused with its
tests or with the work that produces it.

## Use APSS

- [Framework definition](framework/README.md) — the normative APSS
  specification, schema, template, and visualization contract.
- [APSS vocabulary](framework/VOCABULARY.md) — exact meanings and boundaries
  for recurring framework terms.
- [Implementation examples](examples/README.md) — non-normative
  examples that demonstrate how the framework can be applied.

## Inspect or operate the producing system

- [Operations system declaration](operations/SYSTEM.md) — its problem, vision,
  current goal, strategy, boundary, roles, and adaptive loop.
- [Operations strategy](operations/STRATEGY.md) — how the current
  goal guides problem grooming, problem strategies, and selected work.
- [Active problems](operations/problems/) — one authoritative file per current
  gap between the system's goal and current evidence.
- [Tasks](operations/tasks/) — selected and active tasks at the root, candidates
  under `backlog/`, and inactive tasks under `archive/`.
- [Task intake](operations/processes/task-intake.md) and
  [grooming](operations/processes/task-grooming.md) — the path from a proposed
  action to an explicit disposition and possible selection.
- [Working sessions](operations/streams/working-sessions/) — one durable record
  per material brainstorming or problem-grooming invocation.
- [Problem grooming](operations/processes/problem-grooming.md) — revisit the
  current gaps between goals and selected work without automatically creating
  or prioritizing more work.
- [Brainstorming work session](operations/processes/brainstorming.md) — discuss
  and iteratively compile an idea, task, or research topic without conflating
  its evidence, insights, questions, decisions, and possible actions.
- [Insight intake](operations/processes/insight-intake.md) and
  [grooming](operations/processes/insight-grooming.md) — preserve an explicit
  interpretation with provenance, then assess its evidence, scope, confidence,
  and possible propagation without treating it as executable work.
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
operations/  System problems, work, and processes that improve the framework
```

The repository itself is a container, not an APSS system. `operations/` is the
declared system; `framework/` is its primary artifact; and `examples/` contains
supporting artifacts. Operational choices are not normative APSS requirements
unless the framework explicitly adopts them.
