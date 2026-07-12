---
id: P1
type: open-problem
status: open
opened: 2026-07-10
---

# The APS MVP is unfinished and has not run its complete loop

## Parent problem

P1 decomposes the [Framework Operations system problem](../SYSTEM.md): APS
cannot become reliably effective and usable while its framework evolves
without disciplined operations connecting consumer experience, decisions,
validated changes, and learning.

## Evidence

The operations system remains `proposed`. Prior framework changes have artifact
validation and maintainer review but not a recorded subsequent run improved by
outcome evidence.

The normative package is already about 1,400 lines across its definition,
declaration contract, visualization, vocabulary, and changelog. It contains several
concepts and supporting contracts introduced before the first end-to-end loop
has established which are necessary for a useful initial version. The
maintainer identified finishing the MVP, simplifying and pruning it, and running
the whole loop as the largest current problem.

Initial self-use also showed that mixing full problem definitions, completed
work, and current decisions expanded the plan to 148 lines and the log to 394
lines. Moving problem detail to one file and archiving older logs improved the
structure. Further use showed that a separate plan still duplicated direction in
the strategy, gaps in problem files, and commitments in task files, so the
maintainer removed it. The maintainer's usability judgment remains the relevant
outcome evidence.

The problem-hierarchy change now supplies a candidate cycle: it began
from an observed maintainer need, produced compiled framework changes and
example applications, and is being tested through a live problem-grooming
session. It still lacks approved adaptation, a subsequent affected run, and
sufficient outcome evidence.

## Desired change

The smallest coherent APS MVP is explicitly bounded, nonessential concepts and
surfaces are removed or deferred, the retained pieces are finished and
consistent, and one real consumer need runs through the complete loop into an
approved adaptation that changes a later run.

## Signal

The MVP boundary identifies what is included and deferred; every included
responsibility is implemented consistently; and the maintainer can understand
and run the whole process from one real need through problem grooming, selected
work, verification, learning, approved adaptation, and the
later operation changed by that learning. The maintainer's direct feedback is
the initial outcome verification.

## Strategy

Following the [system strategy](../STRATEGY.md), use the initial APS
version to operate the Framework Operations System. Keep only what is needed to
run one complete loop now, simplify it until the maintainer can understand and
use the whole process, and defer the rest. Add complexity later only when more
use or feedback demonstrates a need for it.

Inventory the concepts that the normative framework actually defines or
requires, order them from top to bottom by conceptual dependency, and review
them one at a time. For each concept, establish the smallest clear definition,
boundary, relationships, ownership, and—only when it owns durable identity or
state—lifecycle needed by the complete loop. Retain, simplify, merge, demote,
defer, or remove it, then propagate the decision through every affected
normative and supporting surface.

This is an order of review, not a one-way waterfall. A lower-level review or
attempted run may reopen an upstream concept.

### Concept review test

For each concept, determine:

- its concise meaning and purpose in the complete loop;
- what it is distinct from and which concepts it depends on;
- which lower-level concepts depend on it;
- whether it owns durable identity or state and therefore needs a lifecycle;
- when applicable, what creates, changes, completes, closes, replaces, or
  reopens it, and who authorizes those transitions;
- where its authoritative state lives and what evidence validates it; and
- whether the first complete loop can operate coherently without it.

Avoid creating lifecycle machinery for concepts that are only properties,
relationships, activities, outputs, assessments, or transitions.

### Validation strategy

Validate the simplified model in three independent ways:

1. Run one real need through a complete loop into an approved adaptation and a
   subsequent operation changed by that learning.
2. Give the framework to a reviewer without the session's unstated context and
   ask them to explain its concepts, relationships, and lifecycles, apply it,
   and identify avoidable complexity.
3. Adversarially search for overlapping or circular definitions, multiple
   sources of truth, ownerless state, unjustified lifecycle machinery,
   ceremonial artifacts or processes, undefined transitions, unsupported
   future machinery, and confusion between artifact completion and outcomes.

P1 is not solved merely because its files and schema are consistent. The model
must survive use, teach-back, and adversarial review, and its learning must
change a later run.

## Grooming history

### 2026-07-10 — retained; candidate response identified

Source: maintainer-agent problem-grooming discussion in the current Codex task.

P1 remains relevant and its desired change and signal still distinguish a
completed cycle from artifact delivery. The first grooming session identified
the current goal-linked planning change as a possible first cycle but did not
infer that designation without the maintainer's decision.

### 2026-07-10 — revised and selected as the highest-priority problem

Source: maintainer-agent problem-grooming discussion in the current Codex task.

The maintainer identified the largest current gap as finishing the APS MVP and
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
complete APS loop now and defer everything else. The problem strategy is to use
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

Decision: remove the plan artifact. Selected and active responses live under
`tasks/`; candidate and deferred responses live under `tasks/backlog/` with
explicit statuses. This simplifies the P1 surface while preserving goal →
problem → task traceability.

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

### 2026-07-11 — concept-by-concept simplification strategy accepted

Source: [conceptual simplification strategy session](../streams/working-sessions/2026-07-11-conceptual-simplification-strategy.md).

The maintainer refined the top-down approach around the framework's
existing concepts: inventory them, order them by dependency, then define and
prune them one at a time. Lifecycle machinery is required only for concepts
with durable identity or state; other concepts should remain ordinary
properties, relationships, activities, outputs, assessments, or transitions.

The validation combines a complete live loop, explanation and
teach-back without unstated session context, and adversarial review for hidden
or unnecessary complexity.

The maintainer also identified that the prior umbrella task duplicated P1 and
was too large for one working session. It was deleted rather than archived.
P1 now owns the long-running result and strategy; selected tasks own one
bounded, session-sized response. The current review supplied enough evidence to
create one task for every concept identified so far. The system concept review
is selected; the remaining concept reviews are ready and will be selected in
dependency order.

### 2026-07-12 — provisional examples removed

Source: current system-concept brainstorming session.

The maintainer decided that Framework Operations is the first APS application
and removed the provisional example directory until the framework is polished.
The prior CNC material had no real outcome evidence and created synchronization
work as the declaration changed. Git retains it; future example work is
deferred until the first complete Operations loop produces validated learning.

### 2026-07-12 — flat task collection selected

Source: current task-collection brainstorming session.

The maintainer reported that the `tasks/backlog/` structure made the task
collection harder to use and directed that all task files live directly under
`tasks/`. This reopens the earlier physical-lifecycle convention recorded
above. The explicit status field already carries candidate, active, and
inactive state, so folder placement duplicates that information.

Decision: remove the backlog subdivision and keep every current task directly
under `tasks/`, using status for candidate, selection, and execution state.
Retain `tasks/archive/` as the useful inactive-material boundary. This directly
tests P1's strategy of removing ceremony that obstructs maintainer
understanding and operation.

The maintainer then clarified the framework boundary: task organization is an
implementation detail of each system's process because real systems may use
Jira, GitHub, Linear, repository files, or another system of record. The flat
root plus archive is therefore an Operations choice, not a normative APS rule.

### 2026-07-12 — goal removed and problem hierarchy clarified

Source: [current system-problem review](../streams/working-sessions/2026-07-12-system-problem-review.md)
and [maintainer feedback](../streams/framework-feedback/2026-07-12-problem-hierarchy-and-goal-ambiguity.md).

The maintainer could not form a coherent top-down model from the separate
system-problem, goal, open-problem, and strategy definitions. The framework
also lacked a worked problem-statement example. The maintainer decided to
remove goal completely because it duplicated the desired change and strategy
already carried by problems.

Decision: define problem and strategy generally; treat the system problem as
the root of an evolving hierarchy; relate each smaller problem to a parent and
give it its own desired change, signal, and strategy; use Framework Operations
and P1 as the first worked example; and supersede the separate goal review.
This simplification directly addresses P1's understandability signal.

### 2026-07-12 — problem creation and decision history clarified

Source: [current system-problem review](../streams/working-sessions/2026-07-12-system-problem-review.md)
and [follow-up feedback](../streams/framework-feedback/2026-07-12-problem-creation-grooming-and-storage.md).

The maintainer decided that streams and processes retain their own issues,
observations, results, and insights. Relevant source-specific grooming may
propose higher-level problems, while problem grooming alone decides whether to
open, merge, revise, defer, or reject them. Each problem's chosen system of
record must retain a concise history of material decisions, evidence, and
authority without duplicating task activity or native evidence.

The maintainer also removed normative problem-parent fields and cardinality;
each system's process chooses whether and how to represent decomposition
relationships.

The maintainer later established that the root system problem is constitutive
and stable. Clarification belongs to system strategy, and APS does not define a
root-problem replacement transition.

The maintainer also proposed surprise, excess resource use, and verification
regression as possible review signals. The separately
[groomed insight](../streams/insights/2026-07-12-surprise-cost-and-verification-regression-signals.md)
is compiled provisionally as recommended framework guidance with process-
specific implementation details.

The maintainer later proposed learning from decision quality, harmful choices,
course corrections, and causal hypotheses. That remains a separate
[groomed insight](../streams/insights/2026-07-12-learning-from-decision-quality-and-course-correction.md),
compiled provisionally as lightweight framework learning guidance.
