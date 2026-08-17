---
entity:
  identity:
    type: key
    value: APS-33
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:55.622Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:48.572Z
  key: APS-33
  keyNumber: 33
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
  title: Review the problem signal concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:48.573Z
---

# Review the problem signal concept

## Intended result

Give problem signal the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

In progress as the seventh concept review under P1, following the
[problem-strategy review](../../streams/working-sessions/2026-07-26-problem-strategy-review.md),
which named problem signal as the highest remaining concept in the dependency
chain. The gate it was waiting on has cleared: the
[system-problem review](../../streams/working-sessions/2026-07-12-system-problem-review.md)
established that verification evaluates task attempts against the problem
signal and that satisfying the signal may support a solved assessment without
automatically closing the problem, and the problem lifecycle is now accepted.

This task implements P1's strategy by applying the concept review test to one
concept and propagating a single reviewed disposition. It is accepted when the
concept has one maintainer-authorized disposition, the affected normative and
Operations surfaces agree, and downstream questions are captured rather than
decided here.

Closed. The disposition was **retain, sharpened, renamed**: a signal must be
readable while the problem is open, and the entry is now `Signal`. `Outcome`
absorbed the target the signal was being confused with. The maintainer accepted
the scope on 2026-07-27 and it was delivered in commit `0a0cc10`.

Two questions were recorded rather than decided: whether P1's own signal is
rewritten, which belongs to problem grooming, and whether `Outcome` should move
next to `Signal` in the vocabulary.

This file keeps its `apss.review-problem-signal` id and name, as
`review-problem-strategy` did through the equivalent rename.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/review-problem-signal.md","legacyId":"apss.review-problem-signal"}

---

[repository-import:task:apss.review-problem-signal@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/review-problem-signal.md]
