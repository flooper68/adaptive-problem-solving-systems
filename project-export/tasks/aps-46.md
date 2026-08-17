---
entity:
  identity:
    type: key
    value: APS-46
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:37:07.885Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:53.085Z
  key: APS-46
  keyNumber: 46
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
  title: Review the task concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:53.087Z
---

# Review the task concept

## Intended result

Give task the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Closed on 2026-07-27 by the
[task-family review](../../streams/working-sessions/2026-07-27-task-family-review.md),
which took this task together with `apss.review-task-candidate` and
`apss.review-selected-task` because both dependents were defined in terms of
this concept.

Disposition: **retain, widened.** `Task` is the family's only concept. It
absorbs the selection rules the two removed entries carried — work may be
captured before its problem relationship is clear, selection is the authorized
act that resolves it, and small execution steps inherit the relationship from
their containing task — and states explicitly that APS names no task states.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/review-task.md","legacyId":"apss.review-task"}

---

[repository-import:task:apss.review-task@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/review-task.md]
