---
entity:
  identity:
    type: slug
    value: key-aps-s-21-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-07-26T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-21
---

# Review the problem strategy concept

## Frame

Give problem strategy the smallest clear definition, boundary, relationships,
ownership, and lifecycle needed by the complete APS loop. The responsible user
and decision authority is the APS framework maintainer.

This is the sixth concept review under P1 and the first taken after the
[open-problem review](2026-07-26-open-problem-review.md) cleared the
problem-lifecycle gate. It is the highest remaining concept in the dependency
chain: problem signal, solved, closed, problem grooming, and task all read
against the approach a problem is pursuing.

A useful stopping point is one reviewed disposition propagated through the
normative framework and Framework Operations, with downstream questions
captured without deciding signal, solved, closed, or grooming semantics beyond
what consistency requires.

## Orientation

The concept review test asks first what the concept means, what it is distinct
from, and whether the loop can operate coherently without it. The orientation
pass answered the second question unexpectedly: the framework defines this
concept twice.

- [`VOCABULARY.md` "Strategy"](../../../framework/VOCABULARY.md) — "the current
  evidence-informed theory and approach for changing one problem," under
  *Direction*.
- [`VOCABULARY.md` "Problem strategy"](../../../framework/VOCABULARY.md) — "the
  current approach for resolving or reducing one problem," under *Problems and
  tasks*, roughly sixty lines later.

The same pair appears four bullets apart in one README list
([`README.md` core definitions](../../../framework/README.md)), where a reader
sees both at once.

Ownership and lifecycle are already clean. The concept has no independent
identity: it lives inside the problem's system of record, changes through
problem grooming under the maintainer's authority, and its changes are
recorded in the problem's decision history. No lifecycle machinery exists to
prune.

Dependents are real and unambiguous: tasks implement or test part of it,
task grooming asks whether a candidate does so bounded rather than whole,
problem grooming checks it against the system strategy, and verification
compares results to the signal and may revise it. Nothing depends on there
being *two* definitions.

## Load-bearing question

Are `Strategy` and `Problem strategy` one concept named twice, or two?

The operator recommended one, arguing from the vocabulary's shape rather than
the definitions' substance. `Problem` and `System problem` are a general
concept and its specialization. `Strategy` and `System strategy` are the same
pair. `Problem strategy` is the unspecialized case given a second entry of its
own, and there is no analogous `Problem problem`.

The counter-case was stated and not chosen: a reader working through *Problems
and tasks* would otherwise jump back to *Direction* to learn what a problem's
strategy is. Its price is that the same reader must diff two definitions to
confirm they agree.

## Decision

**Merge.** The maintainer decided it is a single concept.

One `Strategy` entry carries it. `System strategy` remains the specialization
for the root problem. "Problem strategy" survives as ordinary wording where the
scope must be distinguished from the system's — the same treatment "open
problem" received in the preceding review.

## Changes

- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — the `Strategy` entry
  absorbs what only the removed entry stated: every problem has one, informed
  by the system strategy and the problem's decomposition context; it guides the
  work selected for that problem; it changes when that problem's signal,
  verification, or other evidence challenges it. Ownership and change authority
  are now stated where the concept is defined. The `Problem strategy` entry
  under *Problems and tasks* is removed.
- [`README.md`](../../../framework/README.md) — the `Strategy` bullet takes the
  same content; the `Problem strategy` bullet four lines below it is removed.
  The P1 worked example keeps its "Problem strategy" label, which is now the
  licensed ordinary use.
- [`CHANGELOG.md`](../../../framework/CHANGELOG.md) — material change recorded.
- [`problem-grooming.md`](../../processes/problem-grooming.md) — the strategy-
  scope bullet no longer scopes a problem's strategy to open problems only. A
  strategy belongs to a problem in either lifecycle state.
- [P1](../../problems/p1-finish-mvp-and-run-loop.md) — grooming history entry.

## Observations this surfaced

The duplication survived five prior concept reviews because the two definitions
sat in different vocabulary sections and were never read together. This is a
review-method observation rather than a defect in the concept: section-local
reading can miss a duplicate that one alphabetical or dependency-ordered pass
would catch. It belongs to the adversarial pass of P1's validation strategy.

The merge also sharpened, without resolving, the question the
[system-strategy review](2026-07-12-system-strategy-review.md) deferred. With
the general definition no longer duplicated below it, `System strategy` reads
visibly as the root problem's strategy plus the system-wide operating model.
That may read as cleaner or as harder to ignore; teach-back is better placed to
judge than another operator pass.

## Captured evidence

After the disposition was compiled, the maintainer asked whether a grooming
process exists for insights and feedback. Orientation found that Operations
declares both grooming processes but only `problem-grooming` as a work-session
type, and that three of its five streams declare no grooming responsibility at
all. The maintainer's response — that grooming belongs to every input stream,
that its results should be able to reach problem grooming, the problems,
compiled knowledge, or task creation, and that a "doctor" should catch process
issues of this kind — is captured as
[framework feedback](../framework-feedback/archived/2026-07-26-stream-grooming-and-declaration-doctor.md)
at `status: received`. It is evidence, not part of this review's scope, and is
not groomed here.

The maintainer then asked whether brainstorming has a concept of adversarial
review or socratic method. Orientation found that APS develops elicitation —
the `grill` capability, the stream `grill` field, and the adaptive
clarification grill in `insight-intake.md` — but names "adversarial" exactly
once, in P1's own validation strategy, where no process references it. The
operator's reading, that APS concentrates its adversarial weight in
verification and has almost none in deliberation, is captured as an
[insight](../insights/archived/2026-07-26-adversarial-review-absent-from-deliberation.md)
at `status: captured`, with this session's own duplicate-definition finding as
its primary supporting evidence. The maintainer directed capture and close, so
the clarification grill was not run and its open questions are recorded
unanswered. It is not groomed here.

## Validation

Immediate validation passes: `git diff --check` is clean; no cross-file link or
anchor pointed at the removed definition, so this change broke nothing; the
declared strategy, loop, verification, work-session, and stream process paths
resolve; `operations/SYSTEM.md` still carries every element
`framework/SCHEMA.md` requires; P1 retains its required state and the task
references it; and the framework definition, vocabulary, and changelog agree on
one strategy concept.

A repository-wide relative-link sweep found eighteen broken links, all of them
pre-existing and all in historical records: the removed examples directory,
tasks that moved to `tasks/archive/`, and absolute paths into an unrelated
local repository cited by the first kickoff session. None are in a file this
session changed. See *Deferred* below.

Every surviving "problem strategy" occurrence was checked individually and each
is ordinary adjective-plus-noun: two in the framework definition, one in the
system-strategy vocabulary entry, two in Operations processes, one in the
Operations strategy, and three in historical changelog entries that describe
the framework as it stood and are left as written.

Problem-signal evidence is unchanged. P1's signal is whether the maintainer can
understand and run the whole process, which only later use can show. This
review is repository-correct, not yet demonstrated as an improvement.

## Deferred

The eighteen pre-existing broken links in retained evidence are left as
written, consistent with the dead-anchor decision in the
[open-problem review](2026-07-26-open-problem-review.md): the records cite
material as it stood, and Git retains it. The count is now large enough to be
worth a decision rather than a repeated note — whether retained evidence should
be repointed, annotated, or left inert is a question for problem grooming, not
for a concept review to settle.

## Acceptance and delivery

The maintainer accepted the reviewed scope on 2026-07-26 and asked to ship it
without grooming the evidence captured during the session. Commit `4c70ff9`
contains the accepted framework change and was pushed to `origin/main`; the
task is closed and archived.

The two captured records ship at their intake dispositions — the framework
feedback at `received`, the insight at `captured`. Neither was groomed, and the
open questions each records remain unanswered. The stream index in
`streams/framework-feedback/README.md` still lists one of five reports; it was
left as it stands, since an unmaintained declared index is itself an instance of
what the captured feedback reports.

---

Legacy participants: APS framework maintainer, Claude Code operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-07-26-problem-strategy-review.md","legacyId":"apss.session.problem-strategy-review"}

---

[repository-import:session:apss.session.problem-strategy-review@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-07-26-problem-strategy-review.md]
