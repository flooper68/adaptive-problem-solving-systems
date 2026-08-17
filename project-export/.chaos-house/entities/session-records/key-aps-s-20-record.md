---
entity:
  identity:
    type: slug
    value: key-aps-s-20-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-07-26T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-20
---

# Review the problem signal concept

## Frame

Give problem signal the smallest clear definition, boundary, relationships,
ownership, and lifecycle needed by the complete APS loop. The responsible user
and decision authority is the APS framework maintainer.

This is the seventh concept review under P1 and follows the
[problem-strategy review](2026-07-26-problem-strategy-review.md), which named
problem signal as the highest remaining concept in the dependency chain.

A useful stopping point is one reviewed disposition propagated through the
normative framework and Framework Operations, with downstream questions
captured without deciding solved, closed, or grooming semantics beyond what
consistency requires.

## Orientation

Ownership and lifecycle were already clean, as with problem strategy. The
signal is a property of a problem, lives in the problem's system of record,
changes through problem grooming, and has no independent identity. No lifecycle
machinery existed to prune.

Dependents are real: verification compares results against it, `solved` reads
against it, problem grooming reviews it, and learning compares expected effects
with later signal evidence.

Orientation surfaced an asymmetry instead. The framework requires every opened
problem to state "evidence, a desired change, a signal, a strategy, and
demonstrated relevance" ([`README.md`](../../../framework/README.md)), and the
`Problem` entry lists both desired change and signal among what a problem owns —
but only `Problem signal` had a vocabulary entry. **Desired change was a
required element of every problem that the normative vocabulary never defined.**

That gap was not merely documentary. P1's own two sections restate each other:
its desired change describes a bounded MVP run through a complete loop, and its
signal describes the same thing with the verbs changed.

## Load-bearing question

Is `problem signal` distinct from a problem's `desired change`, and if so, why
does only one of them have a definition?

The operator's reading was that the two are genuinely distinct but the framework
defined the wrong one of the pair, leaving a definition broad enough to swallow
the target condition. The maintainer supplied the sharper frame: a signal is
something trackable, closer to a KPI than to a goal statement.

The operator agreed with the reading property and resisted the vocabulary.
"Metric" imports quantification the framework deliberately allows systems to
skip, and KPIs in ordinary management usage are process- or organization-level
indicators, while an APS signal belongs to exactly one problem. What transfers
is that a signal must be something you can take a reading of.

## Evidence

The framework's own worked example had an unreadable signal, and nothing caught
it. P1's signal — "the maintainer can understand and run the whole process from
one real need through problem grooming, selected work, verification, learning,
approved adaptation, and the later operation changed by that learning" — is
observable only once P1 is already resolved. It has no reading while the problem
is open.

Across seven concept reviews no session recorded a value for it. The
[open-problem](2026-07-26-open-problem-review.md) and
[problem-strategy](2026-07-26-problem-strategy-review.md) reviews carry the same
sentence verbatim: "Problem-signal evidence is unchanged. P1's signal is whether
the maintainer can understand and run the whole process, which only later use
can show." That is boilerplate standing in for a reading, and the prior
definition permitted it.

## Decision

**Retain, sharpened.** The maintainer decided a signal must be readable at any
time, "otherwise it does not reflect reality."

The prior definition fused three jobs into one sentence: the indicator observed,
the threshold that counts as sufficient, and the reading itself. The threshold
job is what overlapped `desired change`, which is why writers asked for a signal
stated the target twice. Separating them keeps both concepts and gives the
signal the "worsening" direction a target condition cannot express.

## Naming

The maintainer opened a second question: whether the current names are right.
Two were settled here; the rest were surveyed and left open.

**The target concept is `Outcome`, not a new `Desired change` entry.** The
operator first compiled a separate `Desired change` entry and immediately
flagged it as the vocabulary's next likely collision: `Outcome` already read
"the change an artifact should cause for its consumer or environment," and
three concepts would then lean on the word "change" — the new entry, `Outcome`,
and `Adaptation`. The maintainer preferred `Outcome`.

Widening it also repaired an inconsistency already in that entry. `Outcome`
defined itself through an artifact but evidenced itself through a problem —
"shows whether the relevant problem improved." It is now anchored to the problem
in both halves, and artifacts contribute to an outcome without constituting one.
*Desired outcome* is ordinary wording for the target state, the same treatment
"problem strategy" and "open problem" received.

**The concept keeps the word `signal` and loses the qualifier.** The operator
recommended `Indicator`, arguing that in ordinary and engineering usage a
*signal* is the readings themselves while this concept specifies what to observe
— the wrong half of the pair this review had just separated — and that Google's
SRE practice already separates the service level *indicator* from the
*objective*, which is the same split as indicator-versus-desired-outcome. The
maintainer kept `signal`, then dropped the qualifier: the entry is `Signal`,
matching `Strategy`, with "problem signal" surviving as ordinary wording. The
proposal to name indicator and reading as two concepts was declined as adding a
concept during a pruning phase.

The qualifier could only be dropped because this review had already freed the
word. While verification was described as "supplying the signal," an unqualified
`Signal` entry would have been ambiguous rather than clean.

## Changes

- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — the entry is now
  `Signal` and requires readability while the problem is open: a value now,
  another on a later attempt, and the two comparable. An observation available only after
  resolution restates the desired outcome. Readings may be qualitative;
  APS requires that a reading can be taken, not that it be numerical. A signal
  reading work performed rather than the problem's condition does not
  distinguish activity from improvement.
- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — `Outcome` is anchored to
  the problem rather than the artifact and carries the target the signal was
  being confused with. "Desired change" is retired as framework wording
  throughout the normative package and the Operations processes; historical
  changelog and grooming entries keep it as written.
- [`VOCABULARY.md`](../../../framework/VOCABULARY.md) — the value-function
  paragraph no longer calls verification's output "the signal." Verification
  supplies *evidence* and *reads* the problem's signal; the reading is distinct
  from the signal that defines what to observe. `Solved` reads against a signal
  reading rather than the signal itself.
- [`README.md`](../../../framework/README.md) — core definitions gain `Outcome`
  and `Signal` bullets, placed adjacent so their boundary is visible in one
  pass; the value-function sentence says "evidence"; grooming question 4
  asks what signal can be read now and again later; the lifecycle paragraph
  states the readability requirement and names the failure mode.
- [`VISUALIZATION.md`](../../../framework/VISUALIZATION.md) — "verification
  signals" became "verification evidence" for the same reason.
- [`CHANGELOG.md`](../../../framework/CHANGELOG.md) — material change recorded.
- [`verification.md`](../../processes/verification.md) — attempts now record the
  value observed and compare it with the previous reading, or record the signal
  as unreadable rather than restating it.
- [`problem-grooming.md`](../../processes/problem-grooming.md) — a signal no
  attempt has been able to read is an invocation trigger, and grooming asks
  whether the signal can be read now and whether recent attempts read it.

## Observations this surfaced

This is the third consecutive review to find a fused term rather than an
unnecessary concept. `Open problem` fused a structural predicate with a
lifecycle predicate; `problem strategy` was one concept defined twice; `problem
signal` fused indicator, threshold, and reading. The pruning phase of P1 appears
to be giving way to a disambiguation phase, which is a different kind of work
and may warrant a different review method.

The undefined desired change also suggests the concept inventory driving P1's
task list was drawn from vocabulary entries rather than from what the framework
actually requires. Terms the framework demands but never defines would not
appear as review tasks. Whether other such terms exist is a question for the
adversarial pass of P1's validation strategy.

The naming survey raised four candidates the maintainer did not take up:
`grooming`, which Scrum itself largely replaced with "refinement" and which
carries an unwanted secondary sense in English; the five-term `Task` family;
`Solved`/`Open`/`Closed` as three sibling adjectives where only two are
lifecycle states; and `Artifact`, which is heavily overloaded in software. None
were decided and none are recorded as problems. They are captured here so a
later naming pass does not have to rediscover them.

## Open question

Whether P1's own signal is rewritten under this definition is a problem-grooming
decision, not a consequence of this review. It is recorded here and left to the
maintainer.

## Validation

Immediate checks pass: `git diff --check` is clean; the declared strategy, loop,
verification, work-session, and stream process paths resolve;
`operations/SYSTEM.md` still carries every element `framework/SCHEMA.md`
requires; and the framework definition, vocabulary, visualization, and changelog
agree on one signal concept and one reading sense.

The rename breaks the `VOCABULARY.md#problem-signal` anchor cited by two
retained records — the archived
[system-problem review task](../../tasks/archive/review-system-problem.md) and
the [system-problem review](2026-07-12-system-problem-review.md) session. Both
are left as written under the dead-anchor policy of the
[open-problem review](2026-07-26-open-problem-review.md): the records cite
material as it stood and Git retains it. This is the second review to add to
that count, which strengthens the deferred question below.

Every surviving "problem signal" occurrence was checked and each is ordinary
adjective-plus-noun, now explicitly licensed by the entry: three in the
framework definition, one in the `Solved` entry, two in the Operations
verification process, and the review task's own id and title, which keeps its
name as `review-problem-strategy` did through the equivalent rename. One
"supplies the signal" occurrence remains in the
[system-concept review](2026-07-11-system-concept-review.md) record, describing
the framework as it stood, and is left as written.

Problem-signal evidence: no reading was taken, because P1's current signal
remains unreadable — which is this review's own finding rather than an
acceptable result. This change is repository-correct and not yet demonstrated as
an improvement.

## Acceptance and delivery

The maintainer accepted the reviewed scope on 2026-07-27. Commit `0a0cc10`
contains the accepted framework and Operations changes and was pushed to
`origin/main`; the task is closed and archived.

The two questions this session recorded rather than decided remain open: whether
P1's own signal is rewritten, which belongs to problem grooming, and whether
`Outcome` should sit next to `Signal` in the vocabulary. The naming candidates
surveyed above were not opened as problems.

---

Legacy participants: APS framework maintainer, Claude Code operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-07-26-problem-signal-review.md","legacyId":"apss.session.problem-signal-review"}

---

[repository-import:session:apss.session.problem-signal-review@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-07-26-problem-signal-review.md]
