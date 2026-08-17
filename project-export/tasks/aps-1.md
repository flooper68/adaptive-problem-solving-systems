---
entity:
  identity:
    type: key
    value: APS-1
  kind: task
kind: task
value:
  assignedToUser: false
  assignee: null
  backlogRank: null
  createdAt: 2026-08-16T17:36:30.288Z
  createdBy:
    agent: null
    type: user
  finishedAt: null
  key: APS-1
  keyNumber: 1
  labels:
    - repository-import
    - aps-legacy
  originSchedule: null
  originSession: null
  originTask: null
  parent: null
  priority: 3
  problem: null
  queuePosition: null
  startedAt: null
  status: backlog
  summary: null
  title: Colocate strategy and verification in the system declaration
  type: session-type:slug:brainstorming
  updatedAt: 2026-08-16T17:36:30.288Z
---

# Colocate strategy and verification in the system declaration

## Proposed action

In a brainstorming session, revise the declaration contract so the system
declaration holds its verification and strategy colocated with the
declaration, the way problem files already hold their desired outcome,
signal, and strategy inline — then apply the revised shape to
`operations/SYSTEM.md`, folding in `STRATEGY.md` and
`processes/verification.md` as the contract decides.

## Intended result

The root system reads like its problems do: one file carries what the system
is, how it verifies attempts, and its current strategy. The
`framework/SCHEMA.md` template no longer prescribes separate linked files for
these fields (whether it requires, permits, or stays silent on colocation is
the session's decision to propose).

## Motivation

Maintainer feedback on 2026-08-06: separate verification and strategy files
are confusing; problems colocate these elements, making the system the
asymmetric case. Serves P1's understandability signal and system strategy
point 3 (prefer the smaller model the maintainer can understand).

## Evidence

- [Groomed feedback record](../streams/framework-feedback/archived/2026-08-06-system-declaration-colocation.md)
  with the repository observations at capture.
- [P1](../problems/p1-finish-mvp-and-run-loop.md) as the worked colocation
  precedent.
- The same grooming closed `apss.modular-system-concerns` (extract concerns
  into folders) as contradicted by this direction.

## Open questions

- Should the contract require colocation, permit it, or stay silent and let
  each system choose?
- Does `STRATEGY.md`'s adaptation clause (maintainer approves strategy
  changes) move into `SYSTEM.md` unchanged?
- What happens to inbound links to `STRATEGY.md` and
  `processes/verification.md` across retained records — update live surfaces
  only, per the established precedent?

## Grooming log

### 2026-08-07 — captured from groomed feedback

Captured during the
[first cadenced grooming invocation](../streams/working-sessions/2026-08-06-first-cadenced-grooming.md)
as the approved **act** disposition of the source feedback. Scope and
acceptance are concrete enough for a brainstorming session; selection order
proposed after the information-stream review and the start-simple
compilation.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/tasks/colocate-system-declaration.md","legacyId":"apss.colocate-system-declaration"}

---

[repository-import:task:apss.colocate-system-declaration@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/tasks/colocate-system-declaration.md]
