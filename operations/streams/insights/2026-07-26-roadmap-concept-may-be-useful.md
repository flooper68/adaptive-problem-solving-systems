---
id: apss.insight.roadmap-concept-may-be-useful
type: insight
status: captured
captured: 2026-07-26
source: APS framework maintainer
source_records: []
related_insights:
  - apss.insight.goals-decompose-into-open-problems
related_work:
  - apss.current-state-reporting
  - apss.visual-html-generator
compiled_into: []
---

# Operating a system needs a digestible current-state and next-work view

## Insight

### Claim

APS may benefit from an explicit **roadmap** concept, because an operator
frequently needs a higher-level view of the next tasks and work to be done than
the individual task records provide. As stated by the source: "it could be
useful to have a 'roadmap' concept" and "I often need to get a higher level idea
of next tasks/work to be done".

On clarification the source narrowed this to a **view**, not a new decision
record: "the info is there, I just need quick easily digestable view on the
current state". The underlying information already exists across problem, task,
and strategy records; what is missing is a fast, readable presentation of it.

The requested content is "current summary of open problems and their status +
few next tasks/groomings etc. to do" — a state body with a short forward-looking
slice, both derived from existing records.

### Scope

Orientation of an operator resuming or steering a system that already holds its
problems, strategies, and tasks as separate records. The source's clarification
places the need at the presentation layer rather than in the normative
concepts, so the claim does not currently assert that APS needs a new
vocabulary term. Whether it warrants a framework-level derived view, an
Operations-local artifact, or tooling remains open.

### Reasoning

The source reports a recurring need rather than a single incident: while
operating the system, they often want a higher-level idea of what work comes
next. Each APS record is authoritative for its own scope and is written to be
read on its own, so reconstructing the overall picture means opening many files
and holding them in mind at once. The source's inference is that the cost is in
reading, not in deciding: the information needed to answer "what is the state
and what is next" is already retained, but no single readable surface presents
it.

## Evidence

### Supporting

- The maintainer reports frequently needing a higher-level idea of the next
  tasks and work to be done (2026-07-26 session). Recurrence is the reported
  evidence; specific occasions have not yet been recorded.

### Contradictory or limiting

- Operator note, not source claim: APS previously reviewed and removed a
  separate `vision` concept because it usually restated the desired inverse of
  the problem, deciding that longer-horizon direction may be stated in strategy
  when useful (see
  [`review-vision.md`](../../tasks/archive/review-vision.md) and
  [`framework/CHANGELOG.md`](../../../framework/CHANGELOG.md)). A roadmap
  concept would touch adjacent ground and must show what strategy, the problem
  decomposition, and the task collection do not already cover.
- Operator note, not source claim: the captured candidate
  [`current-state-reporting.md`](../../tasks/current-state-reporting.md)
  already proposes a repeatable snapshot covering "context, current state,
  unresolved concerns, and next actions", and carries the open question of
  whether it is a generated view, a process, or a durable artifact. The roadmap
  idea is adjacent to it and may be the same gap seen from the forward-looking
  side.
- Operator note, not source claim: the Operations task collection currently
  holds 25 tasks at `status: ready` with no ordering recorded among the task
  files themselves. The near-term sequence is instead derivable from the
  problem strategy — [`P1`](../../problems/p1-finish-mvp-and-run-loop.md)
  directs reviewing concepts "from top to bottom by conceptual dependency", and
  the most recent session record names the next concept in that chain. This is
  consistent with the source's "the info is there", and means the forward
  slice can be derived rather than newly decided. It also means the derivation
  depends on reading session records, not only task files.
- Operator note, not source claim: the request names "groomings" alongside
  tasks. Grooming invocations are processes rather than task records, so a view
  covering them draws on a source the task collection does not hold.
- Operator note, not source claim: the system strategy directs the framework to
  keep only what is needed to run one complete loop now and to add complexity
  only when observed use, feedback, validation, or a new problem demonstrates
  it is needed (see [`STRATEGY.md`](../../STRATEGY.md)).

## Possible implications

Because the source placed the need at the presentation layer, the likeliest
responses do not add a vocabulary term:

- The insight is corroborating evidence for the captured candidate
  [`current-state-reporting.md`](../../tasks/current-state-reporting.md), and
  supplies concrete content for it: open problems with status, plus a few next
  tasks and groomings. It also partly answers that candidate's open question
  about consumers, by naming the operator resuming work as one.
- It may argue for a fifth standard derived view in
  [`VISUALIZATION.md`](../../../framework/VISUALIZATION.md), which currently
  defines four views oriented to structure rather than to current state and
  near-term work.
- It may instead be satisfied by tooling such as
  [`visual-html-generator.md`](../../tasks/visual-html-generator.md), with no
  normative change at all.
- A weaker reading is that needing such a view is itself evidence that the
  existing records are harder to read in aggregate than intended, which would
  be a problem-grooming input rather than a new artifact.

The term "roadmap" may not survive: what was described is closer to a
current-state summary with a short next-work slice than to a sequenced
forward plan. Naming is left to grooming.

## Open questions

- Is this the same gap as `current-state-reporting`, or does it stay separate?
- Is the view generated on demand, retained as a file, or produced by tooling?
  A retained file risks drifting from the records it summarizes.
- What is the correct altitude and size for "a few" next tasks, and what
  determines which ones appear?
- Should the framework define this as a standard derived view, or is it
  purely an Operations-local convenience?
- What would be observably worse if APS never adds it?

## Intake and clarification record

### 2026-07-26 — captured

Source wording: "I am thinking about adding an insight that it could be useful
to have a 'roadmap' concept."

The initial claim was preserved before clarification. No reasoning, scope, or
supporting observation was supplied with it.

Three clarifying questions followed. The source reported the prompting need — "I
often need to get a higher level idea of next tasks/work to be done" — then
narrowed the claim from a possible concept to a view — "the info is there, I
just need quick easily digestable view on the current state" — and finally
specified its content: "current summary of open problems and their status + few
next tasks/groomings etc.. to do".

That second answer is the material one: it moves the claim off the normative
concepts, so this record no longer proposes adding a term to the APS
vocabulary. The operator raised the naming tension between "roadmap" and
"current state" explicitly, and the source's content answer resolved it toward
a state summary carrying a short forward slice.

Operator interpretation is marked as such throughout and kept separate from the
source's words. The source participated through this stopping point. Remaining
questions are grooming-level — whether this merges into
`current-state-reporting`, what produces the view, and what it is called — and
are recorded rather than decided here.

## Grooming record

Not yet groomed. See
[`grooming.md`](../../processes/grooming.md).
