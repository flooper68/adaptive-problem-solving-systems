---
entity:
  identity:
    type: key
    value: APS-61
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-21T07:30:46.308Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-61
  keyNumber: 61
  labels: []
  originSchedule: null
  originSession: session:key:APS-S-41
  originTask: null
  parent: null
  priority: 2
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: todo
  summary: null
  title: Revisit and nail down P1's definitions
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-21T07:30:46.308Z
---

## Why

Grooming APS-S-41 (2026-08-21) found P1's pages thin or stale: the condition page was a bare title, the evidence was pre-migration, and the maintainer answered "no" to being able to explain and run the process unaided. The pages were patched in that session, but the maintainer wants them properly reviewed and nailed down together, in a session of their own.

## Work

Go through P1's four pages with the maintainer, one at a time, in plain language:

1. **Condition** (`problems/p1/problem.html`) — is this really the problem, stated so a newcomer understands it?
2. **Desired outcome and signal** (`problems/p1/verification.html`) — is "solved" clear and checkable? Are the three signal components the right ones, and can each be read without guesswork?
3. **Strategy** (`problems/p1/strategy.html`) — does the concept-by-concept review plus the three-way validation still describe how we intend to get there? Anything to drop?
4. **Current state** — refresh after the above.

Keep meaning changes explicit; record each decision in the session. This is separate from the system-level definitions task so the two don't blur.

## Done when

The maintainer can restate P1's condition, desired outcome, signal, and strategy in their own words, and the four pages say exactly that.

## Context

Created by grooming APS-S-41 (adaptation decision L3). Sibling task: "Revisit and nail down the system-level definitions".
