---
entity:
  identity:
    type: key
    value: APS-32
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:54.507Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-32
  keyNumber: 32
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
  title: Review the problem grooming concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T17:36:54.507Z
---

# Review the problem grooming concept

## Intended result

Give problem grooming the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Ready. The
[system-problem review](../streams/working-sessions/2026-07-12-system-problem-review.md)
established that source-specific grooming may propose higher-level problems but
problem grooming alone opens, merges, revises, defers, or rejects them. The
[follow-up feedback](../streams/framework-feedback/archived/2026-07-12-problem-creation-grooming-and-storage.md)
also established that cadence is system-specific and may be event-driven,
scheduled, continuous, or mixed. Problem grooming maintains the hierarchy while
task grooming separately shapes bounded work and readiness; systems may combine
their implementation only when distinct decisions remain inspectable.
APS now delegates all problem-storage and cadence details to each system's
process. Framework Operations retains its current file-based implementation.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/review-problem-grooming.md","legacyId":"apss.review-problem-grooming"}

---

[repository-import:task:apss.review-problem-grooming@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/review-problem-grooming.md]
