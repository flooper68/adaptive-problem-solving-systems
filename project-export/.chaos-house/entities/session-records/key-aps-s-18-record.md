---
entity:
  identity:
    type: slug
    value: key-aps-s-18-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-07-10T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-18
---

# Define open problems and simplify the APSS MVP

## Frame

Use the missing relationship between system goals and everyday work to test and
simplify the initial APSS loop. A useful stopping point is a coherent,
reviewable top-down model that the maintainer can understand and operate.

## Material decisions

- The independent system strategy owns the current goal and the system's
  approach for reaching it. It lives in `STRATEGY.md` beside `SYSTEM.md`
  because it is system-level direction, not a reusable process.
- Every open problem has one file containing its evidence, desired change,
  signal, strategy, and grooming history.
- Every selected task identifies the problems it addresses and implements or
  tests their strategies.
- P1—finishing the smallest understandable MVP and running its complete
  loop—is the only groomed Operations problem. The ungroomed P2 candidate was
  deleted.
- `PLAN.md` was removed because strategy, problem, and task files already own
  its useful state.
- Selected and active tasks live at `tasks/`; captured, grooming, ready, or
  deferred candidates live at `tasks/backlog/`; inactive tasks live at
  `tasks/archive/`.
- The generic work log was removed. Active task files own resumable state,
  problem files own problem decisions, material working-session records own
  interaction history, native streams own domain evidence, and Git owns
  detailed repository history.

## Affected artifacts

- [Framework definition](../../../framework/README.md)
- [Framework vocabulary](../../../framework/VOCABULARY.md)
- [Operations strategy](../../STRATEGY.md)
- [P1](../../problems/p1-finish-mvp-and-run-loop.md)
- [CNC example](../../../examples/cnc-part-production/SYSTEM.md)

## Stopping point

The strategy, problem, and task layers have been simplified and applied to
Operations and CNC. The maintainer explicitly ended the session and accepted
this stopping point, then requested that the complete session changes be
committed and pushed.

Next: continue P1's top-down review at execution, validation, learning, and
adaptation.

---

Legacy participants: APSS framework maintainer, Codex operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-07-10-open-problems-strategy-and-mvp-simplification.md","legacyId":"apss.session.open-problems-strategy-and-mvp-simplification"}

---

[repository-import:session:apss.session.open-problems-strategy-and-mvp-simplification@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-07-10-open-problems-strategy-and-mvp-simplification.md]
