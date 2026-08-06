# Grooming

## Purpose

Process any captured input with the maintainer and record one explicit,
evidence-aware disposition. One process grooms every input kind: framework
feedback reports, insights, task candidates, proposed, open, and closed
problems, and verification results or other stream evidence. Grooming improves
decision quality; it does not itself authorize execution, edit the compiled
framework, or silently convert an input into commitment, knowledge, or work.

This single process implements the framework's grooming responsibilities —
source-specific, problem, and task grooming — which stay distinguishable in
the questions asked, not in separate procedures. The previous per-kind
processes were deliberately consolidated following the system strategy: start
simple and add per-kind procedure back only when observed use shows the shared
one fails. Like all processes, they are compiled knowledge — the removed ones
remain reconstructable from git history and retained session records.

## Invocation and roles

Groom when the maintainer requests it, before selecting substantial work, when
new evidence accumulates on an item, when a dependency resolves, when
verification cannot read a signal, or when an item blocks a consumer.

Grooming also runs on a declared cadence: after every third working session
since the last grooming invocation, groom the accumulated feedback, insights,
and task candidates, and reconfirm or reprioritize the next selected work.
The working-session records under `streams/working-sessions/` are the
counter; any grooming invocation — cadenced or not — resets it. The cadence
is a floor, not a gate: the triggers above still invoke grooming earlier.

- An operator gathers evidence, facilitates, proposes updates, and preserves
  provenance and disagreement.
- The source or reporter clarifies intended meaning when available, but need
  not prove the claim or design the response.
- The APS framework maintainer approves every disposition — including opening,
  reframing, and closing problems — and alone selects a task for execution.

## Procedure

Groom one item at a time; the session can stop between items without forcing
batch decisions.

1. **Orient.** Read the item, its source records, related items, the system
   strategy, current problem and task files, and relevant sessions and
   knowledge.
2. **Clarify.** Restate what the item observes, claims, or proposes, and keep
   observation, inference, assumption, and proposed solution separate. Ask one
   load-bearing question at a time. Do not rewrite the source record to fit a
   conclusion; append clarifications with provenance. Merge duplicates and
   split unrelated items, preserving links to their sources.
3. **Assess.** Seek supporting and contradicting evidence proportionate to the
   decision; record impact, confidence, remaining uncertainty, and the cost of
   being wrong. Use discussion, research, or a bounded experiment when a
   missing answer could materially reverse the disposition.
4. **Decide.** Before proposing, the operator runs the alignment and
   adversarial beat: state which problem and strategy element the proposed
   disposition serves (or that it serves none), whether it contradicts
   compiled knowledge or a prior decision, and the strongest case against it —
   hunting for overlapping or circular definitions, multiple sources of truth,
   ownerless state, unjustified lifecycle machinery, and ceremonial artifacts.
   With that on the table, the maintainer approves one disposition from the
   set below with its rationale. Do not equate desirability with priority, and
   do not claim improvement without evidence against the relevant signal.
5. **Propagate without conflating.**
   - An evidenced higher-level gap becomes a problem decision here: open a new
     problem, or use the evidence to revise an existing one. Keep strategy
     changes at the smallest level supported by their evidence — edit the
     system strategy only when the change should guide other problems.
   - An executable response is captured or linked as a task through
     [`intake.md`](../intake.md). Prefer the smallest bounded work that
     fits one working session; work addressing no open problem may still be
     selected when the maintainer accepts that explicitly.
   - A framework-worthy lesson is captured as a compilation task through
     [`intake.md`](../intake.md); a
     [`brainstorming`](brainstorming.md) session executes it. Grooming never
     edits the compiled framework.
   - Link records in both directions, and leave the item unchanged when no
     propagation is warranted.
6. **Record.** Append a dated entry to the item's authoritative file with
   participants, evidence consulted, the clarified claim or scope, the
   approved disposition and rationale, and a reconsideration trigger or links
   where relevant.

## Dispositions

Every groomed item receives exactly one:

- **act** — the evidence warrants a bounded response now: open or revise a
  problem, create or link a task, or mark a task ready or selected.
- **revise** — update the item's own statement, scope, evidence, desired
  outcome, strategy, or signal.
- **keep** — retain as-is, including monitoring for more evidence; record what
  evidence or event should trigger reconsideration.
- **close** — no further action: addressed, solved, unsupported, duplicate
  (link the canonical record), superseded, rejected, or out of scope. Record
  the reason in the file; a closed problem or task moves under its `archive/`.

Problems and tasks keep their two lifecycle states, `open` and `closed`.
A stream record's `status` moves from `captured` or `received` to `groomed`
(or `closed`); the grooming entry carries the assessment in prose. Existing
records keep their historical status vocabularies as valid history.

## Completion

An invocation is complete when each item in scope has an approved disposition
recorded in its authoritative file, propagation links exist in both
directions, and any missing answer has an evidence request or next trigger.

## Evidence and retention

- The item's file is authoritative for its current state and grooming history;
  do not reconstruct either from session records.
- The working-session record preserves material invocations with participants,
  decisions, affected files, the stopping point, and a brief closing
  "Lessons and friction" note on what the session revealed about how the
  system works ("none" is a valid entry).
- A material invocation updates the affected problems' `Current state`
  sections and refreshes [`STATE.md`](../../STATE.md) before delivery.
- Raw transcripts, feedback, and research stay in their native recoverable
  sources, linked when material.
