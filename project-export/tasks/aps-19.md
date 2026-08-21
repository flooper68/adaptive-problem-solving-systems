---
entity:
  identity:
    type: key
    value: APS-19
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:43.138Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-19
  keyNumber: 19
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
  status: backlog
  summary: null
  title: Review the outcome and state concepts (closed, outcome, solved)
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-21T07:31:19.848Z
---

# Review the closed concept

## Intended result

Give closed the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Ready. The maintainer decided in the
[system-problem review](../streams/working-sessions/2026-07-12-system-problem-review.md)
that `closed` is an authorized lifecycle decision distinct from solved and that
new evidence may reopen a problem. Review remaining closure reasons and
authority details after the problem lifecycle is accepted.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/review-closed.md","legacyId":"apss.review-closed"}

---

[repository-import:task:apss.review-closed@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/review-closed.md]
