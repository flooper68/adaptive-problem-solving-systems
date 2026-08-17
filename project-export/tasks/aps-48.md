---
entity:
  identity:
    type: key
    value: APS-48
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:37:08.598Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:54.930Z
  key: APS-48
  keyNumber: 48
  labels:
    - repository-import
    - aps-legacy
  originSchedule: null
  originSession: null
  originTask: null
  parent: null
  priority: 3
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: done
  summary: Imported terminal state from repository source.
  title: Review the task collection concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:54.931Z
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

The maintainer accepted the reviewed scope and asked to finish the session on
2026-07-12. Commit `7c273aa` was pushed to `origin/main`; this task is closed
and archived.

## Superseded on 2026-07-27

The
[task-family review](../../streams/working-sessions/2026-07-27-task-family-review.md)
removed the `Task collection` entry entirely. Folding `Task candidate` and
`Selected task` into `Task` left the demoted entry holding only a plural of
`Task` plus a delegation statement `Task` had absorbed, and the framework used
the term nowhere outside its own heading. The Operations layout decided here —
flat `tasks/` with `archive/` as the inactive boundary — is unchanged and now
rests on `Task` rather than on a separate concept. The demotion was correct for
what the entry held in July; the later widening is what made the remainder
redundant.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/review-task-collection.md","legacyId":"apss.review-task-collection"}

---

[repository-import:task:apss.review-task-collection@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/review-task-collection.md]
