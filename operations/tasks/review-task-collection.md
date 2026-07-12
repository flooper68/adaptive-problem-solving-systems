---
id: apss.review-task-collection
type: review
status: awaiting-review
owner: APS framework maintainer
agent: Codex operator
created: 2026-07-11
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the task collection concept

## Intended result

Give task collection the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected by the maintainer on 2026-07-12 in response to direct difficulty with
the backlog-folder structure.

Proposed disposition: **demote and simplify**. APS retains the abstract task
collection but delegates its system of record, organization, views,
identifiers, and lifecycle states to each system's process. It no longer
prescribes task files or folders; systems may use Jira, GitHub, Linear, a
database, or another recoverable source.

Framework Operations chooses to keep every current task file directly under
`operations/tasks/`, with explicit status carrying candidate, selection, and
execution state. Its `backlog/` directory and move rules are removed.
`archive/` remains its useful boundary for inactive material; archived tasks
keep their final status, reason, and delivery reference.

The maintainer further defined a task as actual work that iterates on a
problem's solution and processes information for the system. The normative
proposal now makes the task's execution and results an information source for
verification and future learning, while distinguishing that evidence-producing
role from the task's primary role as work.

Validation passes: Framework Operations has 44 current task files at the task
root, eight inactive files in `tasks/archive/`, no backlog directory, no duplicate
task IDs, no invalid current/archived status placement, and no broken task or
current normative links. Normative scans find no prescribed task folder,
product, identifier format, or fixed lifecycle states. `git diff --check`
passes. The task definition and framework explanation consistently connect
actual work, information processing, verification evidence, and future
learning.

Current stopping point: the demoted normative concept and simplified Operations
layout are uncommitted and awaiting maintainer review.
