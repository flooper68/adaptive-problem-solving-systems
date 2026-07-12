---
id: apss.session.system-problem-review
type: working-session
status: retained
recorded: 2026-07-12
accepted: 2026-07-12
closed: 2026-07-12
delivery: 7c273aa
participants: [APS framework maintainer, Codex operator]
source: Maintainer-agent discussion in the current Codex task
related_problems: [P1]
related_tasks: [apss.review-system-problem]
---

# Review the system problem concept

## Frame

Give the system problem the smallest understandable meaning, relationship to
strategy and decomposed problems, and representation needed by the complete
loop. A useful stopping point is one reviewed disposition propagated through
the normative framework and Framework Operations, with downstream questions
captured without silently deciding them.

## Sources and evidence

- The current normative
  [system-problem definition](../../../framework/VOCABULARY.md#system-problem)
  defines it as the root problem the system exists to solve.
- The current
  [framework explanation](../../../framework/README.md#problem-hierarchy-and-strategy)
  originally placed goals and open problems between the system problem and
  tasks; this session is revising that model.
- The [system declaration contract](../../../framework/SCHEMA.md) requires the
  problem statement but gives no worked example.
- [Framework Operations](../../SYSTEM.md) states a concrete root problem, while
  [P1](../../problems/p1-finish-mvp-and-run-loop.md) is its current decomposed
  problem.
- The prior
  [goal-decomposition insight](../insights/2026-07-10-goals-decompose-into-open-problems.md)
  introduced the goal → open problem → task model but retained uncertainty and
  no observed comparative outcome evidence.
- The maintainer's current
  [feedback](../framework-feedback/2026-07-12-problem-hierarchy-and-goal-ambiguity.md)
  reports that the hierarchy is unclear, lacks an example, and makes goal seem
  redundant.

## Current interpretation

The maintainer decided to remove goal completely. The compiled model defines a
problem as a condition to understand or change and a strategy as the current
evidence-informed theory and approach for changing one problem. One system
problem is the root; evidence and learning decompose it into smaller problems,
each with its own desired change, signal, and strategy. Tasks perform bounded
attempts on those strategies and return evidence to verification and future
learning. A decomposed problem becomes a child system's root only when it
receives an independent boundary and complete loop.

Framework Operations and P1 now provide a worked root-to-smaller-problem
example. The separate goal review is superseded.

## Problem lifecycle, verification, and tasks

Current sources:

- The vocabulary defines the
  [open problem](../../../framework/VOCABULARY.md#open-problem),
  [problem signal](../../../framework/VOCABULARY.md#problem-signal),
  [task](../../../framework/VOCABULARY.md#task),
  [`solved`](../../../framework/VOCABULARY.md#solved), and
  [`closed`](../../../framework/VOCABULARY.md#closed) boundaries.
- The Operations
  [verification process](../../processes/verification.md) evaluates attempts
  against the problem signal.
- [Problem grooming](../../processes/problem-grooming.md) authorizes retaining,
  revising, addressing, or closing an open problem.

Current proposal: evidence first reveals a possible gap; grooming opens it in
the decomposition with evidence, desired change, signal, strategy, and
demonstrated relevance to the system problem.
Tasks implement or test bounded parts of that strategy and return execution and
result evidence. Verification compares each material attempt with the problem
signal, after which grooming may retain, revise, reframe, split, merge, relate,
or close the problem. Completing a task never proves that the problem
improved. `Solved` is currently an evidence-based assessment; `closed` is a
separate authorized decision. New evidence may reopen a closed problem, and a
one problem's improvement informs the broader decomposition but does not
automatically solve another problem.

The maintainer accepted the minimal lifecycle: `open` and `closed` are the only
problem lifecycle states; `solved` is an evidence-based assessment that may
support the separate authorized closure decision. The framework explanation,
vocabulary, changelog, and Operations reopening process now compile that
decision.

Validation finds no current goal semantics in the normative framework,
Operations strategy, declaration, or processes; P1 retains its locally required
Operations state; current links resolve; task IDs remain unique; lifecycle
wording consistently separates task completion, verification, solved
assessment, closure, and reopening; and `git diff --check` passes.

The maintainer decided that APS should not define problem parents. The framework
now describes decomposition without prescribing parent fields, cardinality, or
a strict tree; each system's process chooses useful relationship structures.
Framework Operations may retain a local relationship as implementation detail.

The maintainer also supplied
[follow-up feedback](../framework-feedback/2026-07-12-problem-creation-grooming-and-storage.md)
about problem creation, change history, problem grooming as a possible
heartbeat, separation from task grooming, and storage-neutral problem
representation. These topics are linked to existing downstream review tasks
and will be groomed one question at a time rather than silently decided here.

The maintainer decided that every stream and process retains its own issues,
observations, results, and insights. Relevant source-specific grooming may
propose a new higher-level problem, but problem grooming alone decides whether
to open, merge, revise, defer, or reject the proposal. This separates broad
discovery and interpretation from authority over the active problem set.

The maintainer decided that a concise log of problem decisions is crucial. The
framework now requires the chosen problem system of record to preserve why a
problem was opened, materially reframed, changed strategy or signal, closed, or
reopened, with supporting evidence and authority. Routine task activity and
detailed source evidence remain in their own records.

The maintainer decided that problem-grooming cadence is implementation detail:
event-driven operation may suit some systems, while scheduled execution such as
cron may suit others. The framework now requires problem-set re-evaluation
without prescribing a heartbeat mechanism; event-driven, scheduled,
continuous, and mixed implementations are valid.

The maintainer also proposed that learning assess which decisions helped or
worsened the problem, what course corrections taught, and a hypothesis about
why. The separately
[groomed insight](../insights/2026-07-12-learning-from-decision-quality-and-course-correction.md)
is compiled `provisional` as lightweight learning guidance: compare expected
and observed effects, retain context and confounders, and add a simple causal
hypothesis only when useful for future work.

For the separate surprise/resource/regression insight, the maintainer clarified
that available raw data should always be preserved or recoverably referenced so
later insights can recompile it. The maintainer then approved the three-question
screen as general normative recommended guidance with details delegated to each
process. The insight is groomed `provisional` because comparative usefulness
remains unverified.

The maintainer decided that the hierarchical problem structure is central to
APS and that problem grooming and task grooming must remain distinct
responsibilities. Problem grooming maintains proposed, open, and closed
problems and their strategies; task grooming shapes bounded executable
responses and readiness. A system may combine them operationally only when the
two decisions remain inspectable.

The maintainer decided that APS should contain no problem-storage details, only
the general concepts. The normative problem-file schema, folder layout, archive
path, identifiers, and fields are removed. APS requires recoverable problem
state and material decision history while each system chooses its system of
record. Framework Operations retains its file layout as local implementation.

The maintainer decided that the root system problem is constitutive and does not
change within APS. Clarification is a change in the system strategy's current
interpretation, not a change to the root problem. APS therefore defines no
problem-replacement concept or transition.

Final validation finds no normative goal, problem-parent, problem-file, folder,
archive-path, fixed-cadence, combined-grooming, or root-replacement requirement.
All current links resolve; the flat task collection has 44 current and eight
inactive tasks with unique IDs and valid active problem references; and
`git diff --check` passes.

Current stopping point: the complete uncommitted proposal is awaiting
maintainer review. The surprise/resource/regression insight is included as
provisional recommended guidance; the decision-quality insight is included as
provisional lightweight learning guidance. Both remain subject to validation
through later use.

## Acceptance and delivery

The maintainer accepted the complete reviewed scope and asked to finish the
session on 2026-07-12. Final validation passed for normative semantics,
Operations consistency, current links, task IDs and problem references, and
diff whitespace. Commit `7c273aa` was pushed to `origin/main`; this session is
retained and closed.
