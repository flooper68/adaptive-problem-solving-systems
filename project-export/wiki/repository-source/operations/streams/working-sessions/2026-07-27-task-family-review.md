---
id: apss.session.task-family-review
type: working-session
status: retained
recorded: 2026-07-27
accepted: 2026-07-27
closed: 2026-07-27
delivery: e6a9939
participants: [APS framework maintainer, Claude Code operator]
source: Maintainer-agent discussion in the current Claude Code session
related_problems: [P1]
related_tasks:
  [apss.review-task, apss.review-task-candidate, apss.review-selected-task]
---

# Review the task family: task, task candidate, selected task, task collection

## Frame

Give the task family the smallest clear definition, boundary, relationships,
ownership, and lifecycle needed by the complete APS loop. The responsible user
and decision authority is the APS framework maintainer.

This is the eighth concept review under P1 and follows the
[problem-signal review](2026-07-26-problem-signal-review.md), whose naming
survey had already flagged "the five-term `Task` family" as a candidate the
maintainer did not take up at the time.

The maintainer directed that all three review tasks be taken in one session.
That is not only convenience: `Task candidate` and `Selected task` were both
defined in terms of `Task`, so the parent's disposition determined both
dependents. Reviewing them separately is what allowed the defect found below.

## Orientation

Four observations, in the order they mattered.

**Framework Operations already treated both as statuses.**
[`task-grooming.md`](../../processes/task-grooming.md) enumerated eleven task
states — `captured`, `grooming`, `ready`, `selected`, `deferred`, `rejected`,
`merged`, `in-progress`, `awaiting-review`, `closed`, `cancelled` — and stated
plainly that "Selection sets a ready task to `selected`." No separate artifact
kind existed for either concept. This is the same shape the
[open-problem review](2026-07-26-open-problem-review.md) found, where
Operations already stored `status: open` beside a redundant
`type: open-problem`.

**`Task candidate` was circular.** It defined a candidate as "a bounded action
that may be considered for execution, such as a task, research inquiry,
experiment, discussion, review, or remediation" — the same list `Task` already
enumerated. The phrasing made a task one *kind of* candidate, while every other
use in the framework treated a candidate as a not-yet-selected task.

**`Selected task` had been stale for one day.** It still read "It identifies at
least one open problem and implements or tests that problem's strategy" after
the [compilation-invocation session](2026-07-27-compilation-invocation.md)
removed exactly that requirement. That session updated `Task`, `Task
candidate`, and `Task grooming` and missed this entry. The five-way split is
the cause: an edit pass that touched three of five siblings left the fourth
contradicting them.

**The framework contradicted itself on task states.** It said APS prescribes no
"fixed lifecycle states" for tasks in two places
([`README.md`](../../../framework/README.md),
[`VOCABULARY.md`](../../../framework/VOCABULARY.md) under `Task collection`),
and `SCHEMA.md` carried no task status requirement — yet the vocabulary defined
two states as concepts, and `Task collection` named two more (`active`,
`deferred`) that got no definition at all.

## Load-bearing question

Are `task candidate` and `selected task` separate concepts, or two statuses of
a single `Task`?

The maintainer's first question narrowed it usefully: **are the statuses local
process or framework?** The evidence is that the framework had already answered
this deliberately, and asymmetrically. Problem states are normative — `open` and
`closed` carry decision authority and are what verification, `solved`, and
closure hang on. Task states are explicitly delegated, because task workflow
follows whatever tool a system uses.

Two checks confirmed the two entries were leaking local names rather than
legislating:

- No task file carried `status: candidate`. Operations used `captured` for that
  phase. **The framework named a state its only implementation does not have.**
- Five archived tasks carried `status: superseded`, which task grooming's
  enumeration did not list. Harmless drift in a local vocabulary, and exactly
  what must not happen to a normative concept.

The maintainer then decided both parts directly: locally, "we should not need
so many statuses, process should be as simple as possible"; and framework-wise,
that a task candidate and a selected task "is individual process."

## Decision

**Remove `Task candidate` and `Selected task`; retain and widen `Task`.** This
is the fifth pruning disposition under P1, after goal removal, boundary
demotion, open problem, and problem strategy — and the third reached by reading
the vocabulary's own shape rather than the concept's substance.

The principle the operator drew from the maintainer's framing, and compiled
into the changelog: **the framework keeps responsibilities, authorities, and
boundaries; it does not keep state names.** `Task grooming` survives that test —
it names a responsibility and its boundary against problem grooming.
`Task candidate` and `Selected task` did not.

What survived is small, because the framework definition already carried the
rules in prose: work may be captured before its problem relationship is clear;
selection is the authorized act that commits a task and resolves that
relationship; small execution steps inherit it from their containing task. All
three moved into `Task`. The stale open-problem requirement was deleted rather
than moved.

**`Task collection` removed as well, during review.** The maintainer asked why
the entry was still there. It was a review finding the session had created: with
`Task candidate` and `Selected task` folded in, and its own four-state
enumeration deleted as self-contradictory, the entry read as `Task` pluralized
plus a delegation statement `Task` now carried. The framework used the term
nowhere outside its own heading — not in the definition, visualization, or
schema — and problems, the other durable groomed thing, have no collection
concept. That last tell is the third of its kind, after `Problem strategy` with
no `Problem problem` analogue and `Open problem` fusing two predicates.

This reopens the [2026-07-12 review](2026-07-12-task-collection-review.md),
which P1's strategy explicitly permits. That demotion was correct for what the
entry held then; today's widening of `Task` is what made the remainder
redundant. The ruling it produced — APS prescribes no folders, tool, identifier
format, or states — survives as one sentence of `Task`, because a ruling about
representation is not a concept. Sixth pruning disposition.

**Framework Operations collapses twelve task statuses to two.** The eleven
documented states plus the undocumented `superseded` became `open` and
`closed`, mirroring the problem lifecycle. Six of the eleven documented
statuses had never been used once: `grooming`, `selected`, `rejected`,
`in-progress`, `awaiting-review`, `cancelled`.

The precedent did the work. `merged`, `superseded`, `rejected`, and `cancelled`
are closure *reasons*, and the framework already says closure records its
reason, evidence, and authority rather than earning its own state. `deferred`
is open-without-current-work, which problem grooming handles as a decision.
`in-progress` and `awaiting-review` describe the working tree and the session
record, which are directly visible; a status field asserting them is a second
source of truth for what Git already shows.

The one collapse that cost something is `captured` into `ready`, since that was
task grooming's actual output. The operator asked whether the distinction is
load-bearing when picking work; the maintainer's answer was to apply the
simpler version and review it. Readiness is now a *disposition* recorded in the
grooming log and current state, not a status — the same treatment `solved`
receives as an assessment about a problem rather than one of its lifecycle
states. Whether that loses something real is the first thing to check in
review.

## Changes

Framework:

- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — `Task candidate` and
  `Selected task` removed, and `Task` rewritten rather than merely extended.
  The maintainer reviewed the first merged version as too verbose: folding
  three entries in had accumulated 28 lines against `Problem`'s 14, duplicating
  explanation the framework definition already carries. The entry now holds
  three short paragraphs — what a task is, its problem relationship, and
  selection plus the statement that APS prescribes no task states, system of
  record, or tooling. Detail that only elaborates — the one-session sizing
  preference, the system-of-record responsibilities, execution-step
  inheritance — lives in the framework definition alone, with inheritance
  added there so the sentence survived the cut.

  A third maintainer correction then generalized the definition itself. The
  entry had kept two enumerations — what a task produces ("an attempt,
  decision, finding, or change") and what tasks include ("implementation,
  research, experiment, discussion, review, and remediation") — and the
  maintainer judged them too specific to hold in general: a task should just
  produce some form of artifact. The fix leaned on an existing concept rather
  than new wording, since `Artifact` already means exactly "an inspectable
  output produced by a system." `Task` now opens "a bounded unit of work that
  produces an artifact," splitting applies to several independently reviewable
  artifacts, and the kind enumeration is gone from the framework; Operations
  keeps its local `type` values in `task-intake.md`, which is where such lists
  belong.

  A fourth correction cut the middle paragraph to one sentence. The maintainer
  asked whether its remaining text was needed; it was not. The problem-less
  selection clause repeated the selection paragraph two lines down ("accepting
  that there is none"), the judged-against clause repeated the framework
  definition ("verifiable against its own acceptance conditions"), and the
  whole-problem, closure, and splitting rules are operational guidance that
  moved to the framework definition beside the sizing preference.

  A fifth correction removed selection as a framed act. The maintainer asked
  whether it makes sense to mention selection in the framework; the operator's
  reading was that the two rules leaning on it are needed — committing work to
  execution is authority-governed, and that commitment makes the problem
  relationship explicit — but selection itself is a transition, the category
  this session declined to give machinery. The entry was rewritten to state
  the rules without the concept.

  The sixth correction went further and reversed part of that reading: the
  maintainer dropped selection *and authority* from tasks entirely, as not
  generic at the task level. The framework already carried the justification —
  "Loop ownership does not prescribe who performs or approves each step.
  Those authorities belong to the system's chosen processes" — so a declared
  selection authority for tasks was over-specification of an existing
  delegation. The operator's earlier objection ("task grooming does not
  authorize execution, so something must") dissolves the same way: who, if
  anyone, authorizes work is the process's business. `Task` now ends with the
  full delegation — no task states, no selection or authority machinery, no
  system of record, no tooling. `Task grooming` lost its "authority-governed"
  framing and its declared-selection-authority reference while keeping its
  boundary against problem grooming. The framework definition now requires
  recoverability instead of authorized selection; the explicit problem
  relationship survives there, since the system of record carries the
  addressed problem and strategy when the task has one. "Opening a problem
  does not authorize a task" became "does not by itself start work on it" in
  both the definition and the `Open` entry — problem lifecycle authority
  itself is untouched. Operations keeps its local rule that the maintainer
  alone selects a task for execution; that is now visibly an instance choice
  rather than a framework requirement, which is the cleanest demonstration of
  the delegation this session converged on.
- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — `Task collection`
  removed. Its ruling becomes one sentence of `Task`: APS names no task states
  and prescribes no system of record, organization, views, files, folders,
  identifier format, or task-management product.
- [`README.md`](../../../framework/README.md) — the task section was rewritten
  from 47 lines to 27 under two maintainer corrections in review: the `Task`
  entry read too verbose, and the compiled output in general restates
  vocabulary definitions instead of referencing them. The section now opens by
  linking the vocabulary entry for the exact boundary and keeps only the
  operational guidance — sizing, capture and selection, the problem-less
  escape hatch, representation delegation, and what must stay recoverable.
  What APS requires of selection — authorized, with a recoverable result — is
  stated once, in the recoverability paragraph.
- [`CHANGELOG.md`](../../../framework/CHANGELOG.md) — material change recorded.
- [`knowledge-compilation.md`](../../processes/knowledge-compilation.md) — the
  maintainer's second correction is recorded as a compilation rule, not just
  applied once: each definition has one home; the vocabulary carries meaning
  and boundary, the framework definition explains operation and references it.
- [`deduplicate-readme-against-vocabulary.md`](../../tasks/deduplicate-readme-against-vocabulary.md)
  — the rest of the README has the same duplication, largest in its Core
  definitions section. That pass exceeds this session and is captured as a
  task through task intake, with this session's task section as the worked
  example.

Framework Operations:

- [`task-grooming.md`](../../processes/task-grooming.md) — "Dispositions and
  states" becomes "States and dispositions": two states, with readiness,
  deferral, selection, and progress demoted to recorded dispositions and
  events. Closure reasons must survive in the file rather than only in a status
  name. Invocation no longer sets `status: grooming`; propagation no longer
  sets `status: selected`.
- [`task-intake.md`](../../processes/task-intake.md) — capture creates
  `status: open`; the grooming log carries that it is captured but not groomed.
- [`ai-agent-tasks.md`](../../processes/ai-agent-tasks.md) — claim and review
  no longer set statuses; the claim record and the uncommitted working tree
  carry that information. Delivery still closes and archives. The claim step
  also admits a task that addresses no problem, which it did not before.
- 37 current task files → `status: open`; 15 archived → `status: closed`.
  `merged_into` and `superseded_by` preserve the reasons.
- [`review-goal.md`](../../tasks/archive/review-goal.md) and
  [`review-problem-file.md`](../../tasks/archive/review-problem-file.md) gained
  the `closed` date and `superseded_by` field they were missing, so their reason
  no longer depends on the status name alone.
- The two deferred tasks state their reconsideration trigger and that they
  remain open, in prose.
- The three review tasks are closed and archived with their dispositions.

Out of scope and deliberately untouched: insight and feedback records keep
their own status vocabularies in
[`insight-grooming.md`](../../processes/insight-grooming.md) and
[`framework-feedback-intake.md`](../../processes/framework-feedback-intake.md).
Those are different artifact types, and task grooming now says so explicitly.

## Observations this surfaced

**The stale `Selected task` entry is direct evidence for the disposition, not
just a bug fixed alongside it.** A five-entry family fragmented one idea across
five definitions, and a careful session one day earlier still missed one. Three
entries is the load the family can carry.

**A concept review found a defect that a concept review had created.** The
fourth sibling went stale during the compilation-invocation session, which was
itself operating under P1. The gap between "the framework is consistent" and
"the framework stays consistent under edit" is the kind of thing only the
adversarial pass is positioned to measure.

**No `review-task-grooming` task exists**, although `Task grooming` is a
vocabulary entry and `review-problem-grooming` is a current task. This is a
second instance of the inventory gap the
[problem-signal review](2026-07-26-problem-signal-review.md) recorded — that
P1's task list may not cover everything the framework defines or requires. Not
opened as a problem here.

## Open questions

Whether collapsing `captured` and `ready` loses a distinction the maintainer
uses when selecting work. The maintainer chose to apply the two-state version
and judge it in review; if it loses something, a third `ready` state still cuts
twelve to three.

Whether P1's own signal is rewritten remains open from the
[problem-signal review](2026-07-26-problem-signal-review.md). Unchanged here.

## Validation

Immediate checks pass. `git diff --check` is clean. Every task file now carries
`open` (34) or `closed` (18); no other status value survives in `tasks/`. The
`Problems and tasks` vocabulary section is down to `Task`, `Signal`, `Problem
grooming`, `Task grooming`, `Working-session record`, and `Archive`; no removed
heading remains anywhere. Every path declared in `operations/SYSTEM.md`
resolves. Every relative link in `framework/`, `operations/processes/`,
`operations/problems/`, `operations/tasks/`, and this record resolves.

Every surviving "task candidate", "selected task", and "task collection"
occurrence was checked after the final correction and each is ordinary
wording: the two framework diagrams and the framework definition's grooming
heading and core-definitions sentence, `task-intake.md`,
`framework-feedback-grooming.md`, `release.md`, `process.md`,
`task-grooming.md`'s `open` state description, the roadmap insight, and the
`task-candidate-grilling` task's own name — which keeps it as
`review-problem-strategy` did through the equivalent rename. The `Question`
entry, listed here in an earlier draft, no longer qualifies: the sixth
correction changed it to "a problem or a task." Inside `framework/`, "task
collection" now appears only in the changelog, describing the removal.

A closing audit of the propagation surfaces found two contradictions of the
task-without-problem rule that both yesterday's session and this one had
missed: `release.md` asked to confirm selected tasks "name the problems they
address" with no escape for a task addressing none, and `verification.md`
required selected tasks to "reference existing problem IDs." Both now carry
the "when it addresses a problem" qualification. Two sessions missing the
same surfaces is further evidence for the fragmentation finding above.

The archived
[task-collection review](../../tasks/archive/review-task-collection.md) carries
a superseding note, since this session reversed its disposition from demote to
remove. Its Operations layout decision — flat `tasks/` with `archive/` as the
inactive boundary — is unchanged and now rests on `Task`.

`status: captured` survives in `insight-intake.md` and `insight-grooming.md`.
That is the insight vocabulary, not the task vocabulary, and is deliberately
untouched.

Link repair beyond this session's own files: two archived task records,
[`review-system-strategy.md`](../../tasks/archive/review-system-strategy.md)
and [`review-problem-signal.md`](../../tasks/archive/review-problem-signal.md),
carried `../streams/` links that have been broken since they were archived at a
depth their paths did not account for. The three tasks archived here would have
reproduced the same defect; all five are corrected. This is a link fix, not a
content change — the records still say what they said. Pre-existing dead links
in retained stream records are left as written under the dead-anchor policy of
the [open-problem review](2026-07-26-open-problem-review.md).

Problem-signal evidence: no reading was taken. P1's signal remains unreadable,
which the [problem-signal review](2026-07-26-problem-signal-review.md) recorded
as its own finding and left to problem grooming. This change is
repository-correct and not yet demonstrated as an improvement; the maintainer's
review is the first evidence available.

## Acceptance and delivery

The maintainer reviewed the changes iteratively through six corrections —
each one cutting further than the operator's compilation — and accepted the
scope on 2026-07-27 ("let's finish this session"). The reviewed scope was
committed and pushed to `origin/main` per brainstorming delivery; the
delivery commit is referenced in this record's frontmatter follow-up.

The open questions recorded above remain with their owners: the
`captured`/`ready` collapse is judged by use, and P1's signal rewrite belongs
to problem grooming.
