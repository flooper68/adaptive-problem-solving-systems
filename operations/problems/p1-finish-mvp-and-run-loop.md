---
id: P1
type: open-problem
status: open
opened: 2026-07-10
---

# The APSS MVP is unfinished and has not run its complete loop

## Goal

Complete and validate the first evidence-driven framework improvement cycle.

## Evidence

The operations system remains `proposed`. Prior framework changes have artifact
validation and maintainer review but not a recorded subsequent run improved by
outcome evidence.

The normative package is already about 1,400 lines across its definition,
schema, template, visualization, vocabulary, and changelog. It contains several
concepts and supporting contracts introduced before the first end-to-end loop
has established which are necessary for a useful initial version. The
maintainer identified finishing the MVP, simplifying and pruning it, and running
the whole loop as the largest current problem.

Initial self-use also showed that mixing full problem definitions, completed
work, and current decisions expanded the plan to 148 lines and the log to 394
lines. Moving problem detail to one file and archiving older logs improved the
structure. Further use showed that a separate plan still duplicated the goal in
the strategy, gaps in problem files, and commitments in task files, so the
maintainer removed it. The maintainer's usability judgment remains the relevant
outcome evidence.

The goal-linked open-problem change now supplies a candidate cycle: it began
from an observed maintainer need, produced compiled framework changes and
example applications, and is being tested through a live problem-grooming
session. It still lacks approved adaptation, a subsequent affected run, and
sufficient outcome evidence.

## Desired change

The smallest coherent APSS MVP is explicitly bounded, nonessential concepts and
surfaces are removed or deferred, the retained pieces are finished and
consistent, and one real consumer need runs through the complete loop into an
approved adaptation that changes a later run.

## Signal

The MVP boundary identifies what is included and deferred; every included
responsibility is implemented consistently; and the maintainer can understand
and run the whole process from one real need through problem grooming, selected
work, artifact and outcome validation, learning, approved adaptation, and the
later operation changed by that learning. The maintainer's direct feedback is
the initial outcome verification.

## Strategy

Following the [system strategy](../STRATEGY.md), use the initial APSS
version to operate the Framework Operations System. Keep only what is needed to
run one complete loop now, simplify it until the maintainer can understand and
use the whole process, and defer the rest. Add complexity later only when more
use or feedback demonstrates a need for it.

Refine the MVP from top to bottom:

1. clarify the system goal and system strategy;
2. clarify active problems, their strategies, signals, and grooming;
3. simplify selected-work and task processes so they implement those problem
   strategies;
4. finish execution, artifact and outcome validation, learning, and adaptation;
   and
5. retain supporting structure only when the complete loop needs it.

This is the order of review, not a one-way waterfall. Evidence from a lower
layer may reopen and revise an upstream problem or strategy.

## Grooming history

### 2026-07-10 — retained; candidate response identified

Source: maintainer-agent problem-grooming discussion in the current Codex task.

P1 remains relevant and its desired change and signal still distinguish a
completed cycle from artifact delivery. The first grooming session identified
the current goal-linked planning change as a possible first cycle but did not
infer that designation without the maintainer's decision.

### 2026-07-10 — revised and selected as the highest-priority problem

Source: maintainer-agent problem-grooming discussion in the current Codex task.

The maintainer identified the largest current gap as finishing the APSS MVP and
running the complete loop, with simplification and pruning as part of finishing
the initial version. P1 was revised from the narrower absence of a demonstrated
cycle to include the unfinished and potentially overgrown MVP that must be
bounded before that cycle can be meaningful.

Decision: **address now** as the highest-priority open problem. The load-bearing
uncertainty is the MVP inclusion rule; no concepts are removed merely because
the package is long.

### 2026-07-10 — MVP rule, strategy, and verification clarified

Source: maintainer-agent problem-grooming discussion in the current Codex task.

The maintainer approved the pruning rule: keep only what is needed to run one
complete APSS loop now and defer everything else. The problem strategy is to use
the initial version on Framework Operations, simplify it for understandability,
and add complexity later only from observed need and feedback.

Verification is human outcome feedback: P1 is not solved merely because files
or schema validate; the maintainer must be able to understand and run the whole
process. The independent system strategy carries this guidance into later
problem-grooming sessions.

### 2026-07-10 — top-down refinement order added

Source: maintainer-agent problem-grooming discussion in the current Codex task.

The maintainer added a top-down order to the P1 strategy: polish the system
strategy first, then problems and their strategies, then task processes and the
remaining loop. The order preserves feedback: downstream use may still revise
an upstream framing or strategy.

### 2026-07-10 — ungroomed P2 candidate deleted

Source: maintainer-agent problem-grooming discussion in the current Codex task.

The maintainer determined that Operations P2 was never a real groomed problem.
It duplicated the understandability and simplification scope now owned by P1.
P2 was deleted rather than archived; its useful observation about plan and log
bloat remains evidence above, and all current Operations work now addresses P1.

### 2026-07-10 — redundant plan removed

Source: maintainer-agent problem-grooming discussion in the current Codex task.

The maintainer observed that the current goal and direction already belong to
the system strategy, open gaps belong to one problem file each, and executable
commitments belong to one task file each. A separate `PLAN.md` duplicated that
state and created synchronization work.

Decision: remove the plan artifact. The [MVP task](../tasks/finish-mvp.md) is
`in-progress` and addresses P1; candidate and deferred responses live beside
it under `tasks/` with explicit statuses. This simplifies the P1 surface while
preserving goal → problem → task traceability.

### 2026-07-10 — generic work log removed and task lifecycle made physical

Source: [current working session](../streams/working-sessions/2026-07-10-open-problems-strategy-and-mvp-simplification.md).

The maintainer observed that material interactions already have working-session
records, while task and problem files own current state and decisions. The
generic work log duplicated these sources and was removed.

Decision: selected and active tasks live at `tasks/`; captured, grooming,
ready, or deferred tasks live at `tasks/backlog/`; closed, cancelled, rejected,
merged, or superseded tasks live at `tasks/archive/`. Active tasks state their
current state and next step so operators do not need a log to resume.

The system strategy moved from `processes/strategy.md` to sibling
`STRATEGY.md`: it defines system-level direction and informs processes rather
than being one of them.
