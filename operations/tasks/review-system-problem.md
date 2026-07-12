---
id: apss.review-system-problem
type: review
status: awaiting-review
owner: APS framework maintainer
agent: Codex operator
created: 2026-07-11
addresses: [P1]
source: Conceptual simplification strategy session
---

# Review the system problem concept

## Intended result

Give the system problem concept the smallest clear definition, boundary,
relationships, ownership, and lifecycle needed by the complete loop.

## Approach

Apply the concept review test in
`operations/problems/p1-finish-mvp-and-run-loop.md`, choose a disposition,
and propagate accepted changes through affected normative and operational surfaces.

## Current sources

- The normative
  [system-problem definition](../../framework/VOCABULARY.md#system-problem)
  defines the root problem, affected consumer or environment, and
  problem-owning boundary.
- The framework's
  [problem-hierarchy explanation](../../framework/README.md#problem-hierarchy-and-strategy)
  relates the root system problem to smaller open problems and their strategies.
- The declaration
  [contract](../../framework/SCHEMA.md#aps-system-declaration) requires
  `problem` as the condition the system exists to change.
- The [Framework Operations declaration](../SYSTEM.md) supplies the current
  concrete system-problem statement.
- [P1](../problems/p1-finish-mvp-and-run-loop.md) demonstrates a smaller open
  problem within that broader system problem.
- The maintainer's
  [current feedback](../streams/framework-feedback/2026-07-12-problem-hierarchy-and-goal-ambiguity.md)
  reports that the framework lacks a worked example and clear problem
  hierarchy and that goal appears redundant.
- The vocabulary defines the current
  [open-problem state](../../framework/VOCABULARY.md#open-problem),
  [problem signal](../../framework/VOCABULARY.md#problem-signal),
  [task relationship](../../framework/VOCABULARY.md#task),
  [`solved` assessment](../../framework/VOCABULARY.md#solved), and
  [`closed` decision](../../framework/VOCABULARY.md#closed).
- The Operations
  [verification process](../processes/verification.md) compares task attempts
  with the addressed problem's signal, while
  [problem grooming](../processes/problem-grooming.md) authorizes retention,
  revision, work selection, or closure.
- The maintainer's queued
  [creation, grooming, and storage feedback](../streams/framework-feedback/2026-07-12-problem-creation-grooming-and-storage.md)
  challenges normative problem-file storage, asks how problems are created and
  changed, and proposes separating problem grooming from task grooming.

## Lifecycle model under review

1. Evidence reveals a possible smaller problem; it remains feedback, an
   insight, or a question until grooming establishes that the gap exists.
2. Opening the problem places it in the decomposition with evidence, desired
   change, signal, strategy, and demonstrated relevance to the system problem.
3. While open, tasks implement or test bounded parts of its strategy. Task
   execution and results become evidence; task completion does not solve or
   close the problem.
4. Verification evaluates each material attempt against the problem's signal.
   The result may retain, reframe, split, merge, relate, or revise the problem
   and its strategy.
5. When the desired change and signal are satisfied, `solved` records an
   evidence-based assessment. `Closed` remains a separate authorized decision,
   which may also occur for reasons other than solution.
6. New evidence may reopen a closed problem. Improvement of one problem becomes
   evidence for the broader decomposition but does not automatically solve
   another problem.

The maintainer accepted this model on 2026-07-12: problem lifecycle states are
only `open` and `closed`; `solved` remains an assessment that may support the
separate closure decision.

## Stop condition

The concept has one reviewed disposition, affected artifacts are consistent,
and downstream questions are captured without expanding this task.

## Current state

Selected by the maintainer on 2026-07-12 after the system-concept dependency
was resolved.

Proposed disposition: **simplify and retain**. Define problem and strategy
generally, make the system problem the root of the system's problem hierarchy,
and give every smaller problem its own desired change, signal, and strategy.
Tasks perform bounded attempts on those strategies and supply evidence to
verification and learning. The maintainer removed goal completely because it
added nothing beyond a problem's desired change and strategy.

The compiled framework includes a worked Framework Operations → P1 example.
The declaration contract, visualization, Operations strategy, P1, problem and
task grooming, compilation, feedback, and prior goal-decomposition insight are
aligned. The separate goal-review task is superseded and archived.

Validation finds no current goal semantics in the normative framework,
Operations strategy, declaration, or processes; P1 retains its locally required
Operations state; current links resolve; task IDs remain unique; lifecycle
wording consistently separates task completion, verification, solved
assessment, closure, and reopening; and `git diff --check` passes.

The maintainer decided that APS should not define problem parents. The framework
describes decomposition conceptually while each system's process chooses
whether and how to represent relationships among problems. Framework Operations
may retain a local relationship where it is useful.

The maintainer also decided that streams and processes retain their own issues,
observations, results, and insights; source-specific grooming may propose a
higher-level problem; and problem grooming alone acts on that proposal. The
framework and Operations processes now separate proposal from problem creation
authority.

The maintainer decided that each problem's system of record must also retain a
concise history of material decisions and their evidence and authority, without
duplicating routine task execution or native source evidence.

The maintainer decided that problem-grooming cadence is implementation detail.
APS requires problem-set re-evaluation but permits event-driven, scheduled,
continuous, or mixed operation.

The maintainer decided that the hierarchical problem structure is central to
APS and that problem grooming and task grooming are distinct responsibilities.
Problem grooming maintains that hierarchy; task grooming shapes bounded work
for it. Systems may combine the responsibilities operationally only when their
different decisions remain explicit.

The maintainer decided that APS should specify no problem-storage details. The
normative problem-file schema, folder, archive path, identifiers, and fields are
removed; only the general problem concepts and recoverability responsibilities
remain. Framework Operations keeps its files as local implementation.

The maintainer decided that the root system problem is constitutive and does not
change within APS. What might otherwise be called clarification belongs to the
system strategy. APS does not need a problem-replacement concept or transition.

Final validation finds no normative goal, problem-parent, problem-file, folder,
archive-path, fixed-cadence, combined-grooming, or root-replacement requirement.
All current links resolve; the flat task collection has 44 current and eight
inactive tasks with unique IDs and valid active problem references; and
`git diff --check` passes.

Current stopping point: the complete uncommitted proposal is awaiting
maintainer review.
