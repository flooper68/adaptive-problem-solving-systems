# Adaptive Problem Solving (APS)

A framework for designing systems that work on a problem, verify whether their
work changes it, learn from the evidence, and improve their next attempt.

The distinction at its centre is simple: producing a correct artifact is not the
same as improving the situation it was built for. Software may pass its tests
and still fail to help its users. APS makes the connection between a problem,
strategy, work, evidence and adaptation explicit enough to inspect and revise.

It is intended to apply across domains, including software delivery, research,
organizations and personal workflows. It describes responsibilities and concepts,
not one mandatory workflow or a software product to install. Its usefulness
across those settings remains something to establish through application.

## Start reading

The repository's latest published framework snapshot is under
[`project-export/wiki/framework/`](project-export/wiki/framework/):

1. [Overview](project-export/wiki/framework/README.md) — purpose, core concepts and the complete loop.
2. [Vocabulary](project-export/wiki/framework/VOCABULARY.md) — the precise meanings of recurring terms.
3. [Schema](project-export/wiki/framework/SCHEMA.md) — how the framework is represented.
4. [Visualization](project-export/wiki/framework/VISUALIZATION.md) — conventions for showing a system.
5. [Changelog](project-export/wiki/framework/CHANGELOG.md) — changes to the specification.

A useful reading question is: **what evidence would change the next attempt?**
If an activity produces output but never checks outcomes or adapts its approach,
that part of the loop is still open.

## Where the work happens

Since 17 August 2026, APS Framework Operations runs in the maintainer's Metis
(formerly Chaos House) instance, under `aps-framework-operations`. Its wiki is
the canonical source for the framework, work processes, tasks and session history.
This GitHub repository is a backup projection; it can lag the live wiki.

Metis is an implementation used to operate the work, not a requirement for using
APS. See [AGENTS.md](AGENTS.md) for contributor instructions and live access.

## Repository map

- `project-export/` is machine-written by the repository backup. Do not edit it
  by hand or rewrite the history it is based on.
- `framework/` and `operations/` are the pre-migration capsule, retained as history.
  They are not the current specification.
- The `chaos-house-backup` branch preserves the frozen pre-migration repository.

Framework and process changes belong in the live wiki and are recorded in the
framework changelog. Operational choices become framework requirements only
when the normative specification adopts them.
