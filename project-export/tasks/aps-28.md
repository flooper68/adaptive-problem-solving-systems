---
entity:
  identity:
    type: key
    value: APS-28
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:51.407Z
  createdBy:
    agent: null
    type: user
  finishedAt: 2026-08-16T19:39:47.761Z
  key: APS-28
  keyNumber: 28
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
  title: Review the open problem concept
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T19:39:47.763Z
---

# Review the open problem concept

## Intended result

Give open problem the smallest clear definition, boundary, relationships, ownership,
and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected and in progress. The
[system-problem review](../../streams/working-sessions/2026-07-12-system-problem-review.md)
established that an open problem is a smaller problem in the hierarchy and that
`open` and `closed` are its only lifecycle states, and the
[system-strategy review](../../streams/working-sessions/2026-07-12-system-strategy-review.md)
resolved the last higher-level dependency on 2026-07-26.

This task implements P1's concept-review strategy for the concept that
problem strategy, problem signal, problem grooming, solved, closed, and task
all depend on. Acceptance condition: one reviewed disposition propagated
through every affected normative and Operations surface, with downstream
questions captured rather than decided.

Disposition: **remove**. The concept review found no defect in the underlying
concept — it owns real durable state, so its lifecycle is justified — but found
that the term fused a structural predicate (not the root) with a lifecycle
predicate (currently open). The maintainer read `open` as a status on a problem;
checking that reading against every current use found no contradiction and two
surfaces already implementing it, including the redundant `type: open-problem`
beside `status: open` in P1's own file.

`Open` and `closed` are now the two lifecycle states of a problem, with `open`
defined beside `closed` as the authorized grooming decision. The durable-state
content moved into the general problem definition. Six uses that genuinely mean
"currently open" were kept as ordinary adjective-plus-noun; ten inert uses
dropped the adjective; four uses that leaned on "open" to mean "not the root"
now name the decomposition. Three definitions that wrongly scoped artifact,
outcome, and solved evidence to open problems only were corrected.

Immediate validation passes: `git diff --check` clean; no link broken by this
change; declared strategy, loop, verification, work-session, and stream process
paths resolve; `operations/SYSTEM.md` still matches `framework/SCHEMA.md`; P1
retains its required state and this task references it; the framework
definition, vocabulary, visualization, and changelog agree.

The maintainer accepted the disposition on 2026-07-26. Commit `09a86d9`
contains the accepted framework change. This task is closed and archived.

Working session:
[open-problem review](../../streams/working-sessions/2026-07-26-open-problem-review.md).

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/archive/review-open-problem.md","legacyId":"apss.review-open-problem"}

---

[repository-import:task:apss.review-open-problem@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/archive/review-open-problem.md]
