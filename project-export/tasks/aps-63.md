---
entity:
  identity:
    type: key
    value: APS-63
  kind: task
kind: task
value:
  assignedToUser: true
  assignee: null
  backlogRank: null
  createdAt: 2026-08-21T07:30:58.601Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-63
  keyNumber: 63
  labels: []
  originSchedule: null
  originSession: session:key:APS-S-41
  originTask: null
  parent: null
  priority: 3
  problem: problem:slug:p1
  queuePosition: null
  startedAt: null
  status: todo
  summary: null
  title: Grooming plans fixes as tasks instead of applying them
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-21T07:35:21.584Z
---

## Why

In grooming APS-S-41 (2026-08-21) the agent fixed P1's pages directly after a general "makes sense" from the maintainer. The maintainer's rule: **during grooming we find problems and plan work to fix them; we do not fix them in the session.** Grooming may still append signal readings to the problem state log and change task state (create, merge, cancel, promote) — that is its job. It should not edit declarations, processes, or framework pages.

## Work

Amend `processes/sessions/grooming.md` (step 7.7 and the Completion section) so that:

- the only canonical writes grooming makes are readings/log appends, task-state changes, problem comments, and project health;
- any content fix to a declaration, process, or framework page becomes a task (or a note on an existing one) instead of an in-session edit;
- the exact wording of any proposed change is still shown to the maintainer for the record.

Keep it to a few plain sentences. Check the text against the plain-language rule (APS-10).

## Done when

The grooming page says this plainly, and the next grooming run produces tasks, not edits.

## Context

Created by grooming APS-S-41 (adaptation decision L5).
