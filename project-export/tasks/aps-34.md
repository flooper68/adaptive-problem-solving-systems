---
entity:
  identity:
    type: key
    value: APS-34
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:56.345Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:48.907Z
  key: APS-34
  keyNumber: 34
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
  title: Review the problem strategy concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:48.909Z
---

# Review the problem strategy concept

## Intended result

Give problem strategy the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected on 2026-07-26. The
[open-problem review](../../streams/working-sessions/2026-07-26-open-problem-review.md)
cleared the problem-lifecycle gate that this and five sibling reviews waited
on. This is the sixth concept review and the first of the unblocked set.

The orientation pass found that the normative framework defines the concept
twice — `Strategy` and `Problem strategy` — in two vocabulary sections and in
two bullets of one README list.

Disposition: **merge**. The concept review found no defect in the concept
itself — ownership and lifecycle were already clean, and its dependents are
real and unambiguous — but found that nothing depended on there being two
definitions. The surviving `Strategy` entry absorbs what only the removed entry
stated and now carries ownership and change authority. `System strategy`
remains the root-scoped specialization; "problem strategy" survives as ordinary
wording, checked occurrence by occurrence.

Immediate validation passes: `git diff --check` clean; no cross-file link or
anchor pointed at the removed definition; declared strategy, loop,
verification, work-session, and stream process paths resolve;
`operations/SYSTEM.md` still matches `framework/SCHEMA.md`; P1 retains its
required state and this task references it; the framework definition,
vocabulary, and changelog agree on one strategy concept.

Eighteen pre-existing broken links in retained evidence are left as written and
deferred to problem grooming rather than settled by a concept review.

The maintainer accepted the disposition on 2026-07-26 and asked to ship the
session. Commit `4c70ff9` contains the accepted framework change. This task is
closed and archived.

Working session:
[problem-strategy review](../../streams/working-sessions/2026-07-26-problem-strategy-review.md).

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/review-problem-strategy.md","legacyId":"apss.review-problem-strategy"}

---

[repository-import:task:apss.review-problem-strategy@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/review-problem-strategy.md]
