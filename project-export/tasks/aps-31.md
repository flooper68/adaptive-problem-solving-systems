---
entity:
  identity:
    type: key
    value: APS-31
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:53.732Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:48.286Z
  key: APS-31
  keyNumber: 31
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
  title: Review the problem file concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:48.287Z
---

# Review the problem file concept

## Intended result

Give problem file the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Superseded by `apss.review-system-problem` on 2026-07-12. The maintainer decided during the
[system-problem review](../../streams/working-sessions/2026-07-12-system-problem-review.md)
that APS should not define a problem-file concept, schema, folder, archive path,
identifier, or field layout. It retains only general problem concepts and
recoverability responsibilities; Framework Operations files are local
implementation. The normative concept task therefore has no remaining subject.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/review-problem-file.md","legacyId":"apss.review-problem-file"}

---

[repository-import:task:apss.review-problem-file@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/review-problem-file.md]
