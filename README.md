# Adaptive Problem Solving (APS)

This repository develops Adaptive Problem Solving, a general method for systems
that iteratively solve a defined problem, evaluate progress, learn from
evidence, and adapt later attempts.

Its purpose is to make APS understandable, usable across different domains, and
improvable through evidence from applying the method itself.

## Where the work happens

Since 2026-08-17 the APS Framework Operations system runs in the maintainer's
Chaos House instance (project `aps-framework-operations`), which owns the
canonical framework documents, problems, tasks, sessions, and streams. This
repository is the backup that instance pushes to `main`. See `AGENTS.md` for
how to work with the instance.

## Repository structure

- [`project-export/`](project-export/wiki/framework/README.md) is the live
  projection of the Chaos House project: the current framework text under
  `wiki/framework/`, processes under `wiki/processes/`, plus tasks, sessions,
  stream records, and the timeline. It is machine-written; do not edit it by
  hand.
- [`framework/`](framework/README.md) and [`operations/`](operations/SYSTEM.md)
  are the pre-migration repository capsule, retained as history. The branch
  `chaos-house-backup` preserves the last pre-migration state of `main`.

Operational choices become APS requirements only when the normative framework
adopts them. Additional applications and examples can be added after the
framework is sufficiently stable for them to provide useful validation.
