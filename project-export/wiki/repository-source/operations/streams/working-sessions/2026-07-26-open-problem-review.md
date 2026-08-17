---
id: apss.session.open-problem-review
type: working-session
status: retained
recorded: 2026-07-26
accepted: 2026-07-26
closed: 2026-07-26
delivery: 09a86d9
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks: [apss.review-open-problem]
---

# Review the open problem concept

## Frame

Give open problem the smallest clear definition, boundary, relationships,
ownership, and lifecycle needed by the complete APS loop. The responsible user
and decision authority is the APS framework maintainer.

This review addresses P1's concept-simplification strategy after the system,
boundary, system-problem, and system-strategy dependencies were reviewed. It is
the gate for problem strategy, problem signal, problem grooming, solved,
closed, and task, which all wait on the problem lifecycle being accepted.

A useful stopping point is one reviewed disposition propagated through the
normative framework and Framework Operations, with downstream questions
captured without deciding problem-strategy, signal, or grooming semantics
beyond what consistency requires.

## Current evidence

- The normative definition in
  [VOCABULARY.md](../../../framework/VOCABULARY.md), as it stood before this
  review removed it, called an open problem "an evidenced, unresolved smaller
  problem that decomposes the system problem or another open problem," then
  stated that `open` is one of the problem's two lifecycle states.
- The [framework explanation](../../../framework/README.md#problem-hierarchy-and-strategy)
  gives the same concept a second name, "smaller problem," and uses both terms
  for what appears to be one referent.
- The [general problem definition](../../../framework/VOCABULARY.md#problem)
  already states that problems form an evolving hierarchy through
  decomposition.
- The [system-problem review](2026-07-12-system-problem-review.md) established
  that `open` and `closed` are the only problem lifecycle states, that `solved`
  is a separate evidence-based assessment, and that the same distinction
  applies to the root system problem.
- The [declaration contract](../../../framework/SCHEMA.md) carries no
  open-problem representation; problem storage is delegated to each system's
  process.
- Outside stream and archive records, "open problem" appears about 48 times and
  "smaller problem" about 15 times across the framework and Operations.

## Concept review test

Applying P1's test found no structural defect in the underlying concept:

- **Purpose in the loop.** It names one evidenced, unresolved gap in the
  system's evolving decomposition and owns the evidence, desired change,
  signal, strategy, and material decision history that guide and evaluate
  bounded tasks.
- **Depends on** problem, system problem, evidence, and strategy.
- **Depended on by** problem strategy, problem signal, problem grooming, task,
  selected task, task grooming, solved, closed, verification, learning, and
  adaptation. It is the most load-bearing concept reviewed so far.
- **Durable identity and state.** Yes. It persists across many sessions and
  tasks, so its `open`/`closed` lifecycle is justified rather than ceremonial.
- **Transitions and authority.** Problem grooming opens a proposal, revises,
  reframes, splits, merges, closes, and reopens it; each system's process names
  the authority.
- **Authoritative state.** The system's chosen system of record.
- **Operating without it.** The first complete loop cannot; the decomposition
  is central to APS.

## Load-bearing question raised

Whether "open problem" is one concept or a term that fuses two independent
predicates.

The definition combines a structural claim (the problem is not the root; it
decomposes something above it) with a lifecycle claim (the problem is currently
open rather than closed). Three observable consequences follow:

1. The lifecycle half is not distinguishing. The root system problem also
   carries the solved-versus-closed distinction, so `open` applies to it too.
2. There is no name for a decomposed problem that has been closed, even though
   closure, reopening, and decision history all need to refer to one. By its
   own definition it stops being an "open problem" at the moment closure makes
   its history most relevant.
3. The framework already drifts between "open problem" and "smaller problem"
   for the same referent, in both the vocabulary and the framework definition.

The general problem definition plus the two lifecycle states may already cover
everything the separate entry asserts, in which case the entry adds a term
rather than a concept.

## Candidate dispositions

- **Retain, tighten wording.** Cheapest and least disruptive; leaves the fused
  predicates and the missing name for a closed decomposed problem in place.
- **Simplify.** Keep the entry but define it purely structurally and delete the
  problem-strategy, signal, history, and child-system content that the
  neighbouring entries already own.
- **Remove.** Keep problem, system problem, and the `open`/`closed` lifecycle
  states, and use "problem" wherever the text now says "open problem." Nothing
  is lost: "a problem grooming has opened" still expresses authorized entry
  into the active decomposition.

The operator's recommendation was **remove**, with the naming question settled
in favour of the general term. The system strategy's smaller-reversible-step
guidance argued for **simplify** instead.

## Maintainer reading and its verification

The maintainer read `open` as a status on a problem, given that a system holds
many problems, and asked whether that reading contradicts any current use.

It does not, and two surfaces already implement it:

- Framework Operations stored `type: open-problem` **and** `status: open` in the
  same problem file. The type field repeated what the status field already said.
- [Problem grooming](../../processes/problem-grooming.md) reviews "proposed,
  open, and closed" problems, offers `open`, `reopen`, and `close` as verbs
  acting on one kind of thing, and sets `status: open` and `status: closed`
  directly. It never treated open and closed problems as two types.
- The vocabulary entry contradicted its own heading: "`Open` is one of the
  problem's two lifecycle states; the other is `closed`."

One real friction point was identified rather than dismissed. The term was
quietly doing a second job — excluding the root — in four sentences. Because
the root system problem carries the same solved-versus-closed distinction, the
status reading makes the root an open problem too, so those four sentences now
name the decomposition explicitly instead of leaning on "open". The word
"evidenced" in the removed definition relocated to the new `Open` entry, where
it belongs to the opening decision that problem grooming already performs.

## Maintainer decision

**Remove.** `Open` and `closed` are the two lifecycle states of a problem, and
nothing else.

## Compiled changes

Normative framework:

- [VOCABULARY.md](../../../framework/VOCABULARY.md) — removed the `Open
  problem` entry; moved its durable-state content into `Problem`; added an
  `Open` entry beside `Closed` defining the authorized opening decision.
- [README.md](../../../framework/README.md) — replaced the `Open problem`
  bullet with an `Open and closed` lifecycle bullet that preserves "opening a
  problem does not authorize a task."
- [VISUALIZATION.md](../../../framework/VISUALIZATION.md) — renamed a diagram
  node id that still said `openProblem` while its label said "Smaller problem".
- [CHANGELOG.md](../../../framework/CHANGELOG.md) — new entry.

Framework Operations:

- [P1](../../problems/p1-finish-mvp-and-run-loop.md) — dropped the redundant
  `type: open-problem` field; added the grooming-history entry.
- [knowledge-compilation.md](../../processes/knowledge-compilation.md) —
  "open-problem hierarchy" became "problem hierarchy".

The grooming, orientation, and task-selection surfaces were deliberately left
alone: their uses genuinely mean a problem currently in the open state and now
read as ordinary adjective-plus-noun.

## Errors this surfaced

Three normative definitions wrongly scoped their evidence to open problems only
and were corrected:

- `Artifact` and `Outcome` said an artifact shows whether an *open* problem
  improved; an artifact can improve a problem closed last week.
- `Solved` said the desired change for an *open* problem occurred; solved is
  routinely assessed at the moment of closure.

The fused term was concealing errors, not merely costing a word.

## Validation

Immediate validation passes: `git diff --check` is clean; no link was broken by
this change; the declared strategy, loop, verification, work-session, and
stream process paths resolve; `operations/SYSTEM.md` still matches
`framework/SCHEMA.md`; P1 retains its required state and the task references it;
and the framework definition, vocabulary, visualization, and changelog agree.

Problem-signal evidence is unchanged. P1's signal is whether the maintainer can
understand and run the whole process, which only later use can show. This
review is repository-correct, not yet demonstrated as an improvement.

## Deferred

Three historical records — an archived task, a feedback record, and the
system-problem session record — cite a `VOCABULARY.md#open-problem` anchor that
no longer resolves. They are left as written because they cite the definition as
it stood, and Git retains the removed text. Repoint them if dead anchors in
retained evidence later prove to obstruct navigation.

## Acceptance and delivery

The maintainer accepted the reviewed scope and asked to finish the session on
2026-07-26. Commit `09a86d9` contains the accepted framework change and was
pushed to `origin/main`; the task is closed and archived.
