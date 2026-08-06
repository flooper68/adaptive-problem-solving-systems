---
id: P1
type: problem
status: open
opened: 2026-07-10
---

# The APS MVP is unfinished and has not run its complete loop

## Current state

As of 2026-08-06 ([subsystem and relationships review
session](../streams/working-sessions/2026-08-06-subsystem-and-relationships-review.md)):

- **Recently:** the last Direction-level concept review delivered — subsystem
  merged into child system, run as the first automated brainstorming
  invocation (this session); current state promoted to a first-class
  framework concept, the first evidence-driven addition under strategy
  point 4 after seven prunings (`dfc62a4`).
- **In flight:** the grooming-cadence declaration session awaits delivery;
  two ungroomed stream-declaration feedback records (2026-08-06) await
  grooming.
- **Next:** the first full grooming invocation under the consolidated
  process — now due under the declared cadence of one grooming per three
  working sessions. P1's own signal rewrite remains open from the
  problem-signal review.

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

## Desired outcome

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

Write every retained surface in plain language. Prefer everyday words over
specialist vocabulary, define any term the framework must keep, and treat
wording that a reader stumbles over as avoidable complexity to remove like any
other. Apply this constraint while propagating each concept decision through
its affected surfaces.

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
   and identify avoidable complexity, including any wording they had to reread
   or could not restate in their own words.
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
and [maintainer feedback](../streams/framework-feedback/archived/2026-07-12-problem-hierarchy-and-goal-ambiguity.md).

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
[groomed insight](../streams/insights/archived/2026-07-12-surprise-cost-and-verification-regression-signals.md)
is compiled provisionally as recommended framework guidance with process-
specific implementation details.

The maintainer later proposed learning from decision quality, harmful choices,
course corrections, and causal hypotheses. That remains a separate
[groomed insight](../streams/insights/archived/2026-07-12-learning-from-decision-quality-and-course-correction.md),
compiled provisionally as lightweight framework learning guidance.

### 2026-07-26 — system strategy retained

Source: [system-strategy review](../streams/working-sessions/2026-07-12-system-strategy-review.md).

The fourth concept review found no structural defect in system strategy: one
authoritative location, no lifecycle machinery, explicit change authority. The
load-bearing question was whether the concept conflates the approach to the
root problem with the system's operating model for running the loop, since the
general strategy definition already covers the former. The operator recommended
demoting it; the maintainer decided both belong to one concept in use and that
splitting or demoting would add complexity rather than remove it.

Decision: retain system strategy, tighten wording only. Unlike the goal removal
and boundary demotion, this review confirms a concept rather than pruning one,
which is evidence that the remaining model is approaching its useful minimum
rather than that the pruning strategy has stalled. The conflation question is
recorded for the teach-back and adversarial passes of the validation strategy,
which are better placed to judge whether readers can separate system strategy
from problem strategy.

### 2026-07-26 — open problem removed; `open` kept as a problem status

Source: [open-problem review](../streams/working-sessions/2026-07-26-open-problem-review.md).

The fifth concept review found no defect in the underlying concept — it has
genuine durable state, so its lifecycle is justified — but found that the term
fused a structural predicate (not the root) with a lifecycle predicate
(currently open). The maintainer read `open` as a status on a problem and asked
whether that contradicted any current use. It did not: Framework Operations
already stored `status: open` beside a redundant `type: open-problem`, and the
problem-grooming process already treated open, closed, and proposed as states
of one kind of thing.

Decision: **remove** the separate concept. `Open` and `closed` are the two
lifecycle states of a problem; `open` gains a definition alongside `closed` as
the authorized grooming decision that admits an evidenced proposal. This is the
third pruning disposition after goal removal and boundary demotion, and the
first reached from the maintainer's own reading rather than an operator
recommendation.

The change was surgical rather than mechanical: about six uses that genuinely
mean "currently open" were kept as ordinary adjective-plus-noun, ten inert uses
dropped the adjective, and four uses that leaned on "open" to mean "not the
root" now say decomposition explicitly. Three definitions that wrongly scoped
artifact, outcome, and solved evidence to open problems only were corrected as
a side effect — evidence that the fused term had been hiding errors rather than
merely costing a word.

### 2026-07-26 — problem strategy merged into strategy

Source: [problem-strategy review](../streams/working-sessions/2026-07-26-problem-strategy-review.md).

The sixth concept review, and the first taken after the problem-lifecycle gate
cleared. Orientation answered the review test's distinctness question
immediately: the framework defined the concept twice, as `Strategy` under
*Direction* and `Problem strategy` under *Problems and tasks*, with no
difference beyond wording. Ownership and lifecycle were already clean — the
concept lives in the problem's system of record, has no independent identity,
and needed no machinery pruned.

Decision: **merge**. One `Strategy` entry now carries the concept and absorbs
what only the removed entry stated; `System strategy` remains its specialization
for the root problem; "problem strategy" survives as ordinary wording. This is
the fourth pruning disposition, after goal removal, boundary demotion, and open
problem, and the second consecutive one reached by reading the vocabulary's own
shape rather than the concept's substance — `Problem`/`System problem` and
`Strategy`/`System strategy` are the same general-plus-specialization pair, and
`Problem strategy` had no `Problem problem` analogue.

The duplication survived five prior reviews because the two definitions sat in
different vocabulary sections. That is a review-method observation, not a
defect in this concept: section-local reading can miss a duplicate that a
single alphabetical or dependency-ordered pass would catch. Recorded for the
adversarial pass of the validation strategy.

This review also sharpened, without resolving, the conflation question the
system-strategy review deferred. With the duplicate removed, `System strategy`
is visibly the root problem's strategy plus the system-wide operating model.
The teach-back and adversarial passes remain the right place to judge it.

### 2026-07-26 — problem signal must be readable; P1's own signal fails it

Source: [problem-signal review](../streams/working-sessions/2026-07-26-problem-signal-review.md).

The seventh concept review found the definition satisfied by a restated goal.
It fused the indicator observed, the threshold counting as sufficient, and the
reading itself, and its threshold job overlapped the desired change — a required
element of every problem that the vocabulary never defined.

The maintainer decided a signal must be readable at any time, "otherwise it does
not reflect reality." A signal now yields a value now, another on a later
attempt, and the two must be comparable; readings may be qualitative. The
missing target concept was resolved by widening `Outcome` to cover it rather
than adding a second entry, so a problem now states its *desired outcome*, and
the framework stopped using "signal" for both the yardstick and verification's
output. With the word freed, the entry became `Signal` rather than `Problem
signal`, matching `Strategy`.

The evidence was P1 itself. Its signal above is observable only once P1 is
already resolved, and seven reviews recorded no value for it — the last two
carrying the same placeholder sentence verbatim. **P1's signal does not satisfy
the definition this review adopted.** Rewriting it is a problem-grooming
decision and is left open here rather than taken by a concept review.

### 2026-07-27 — task family cut to two concepts; Operations statuses cut to two

Source: [task-family review](../streams/working-sessions/2026-07-27-task-family-review.md).

The eighth concept review took `Task`, `Task candidate`, and `Selected task`
together, because both dependents were defined in terms of the parent and their
disposition turned on one question. The maintainer split that question in two:
are the statuses local process or framework, and why would the framework need
these two entries at all.

The framework had already answered the first, deliberately and asymmetrically —
problem states are normative because they carry decision authority, task states
are delegated because task workflow follows the tool — and then defined two task
states as concepts anyway. Two checks showed they were leaking local names:
no task file ever carried `status: candidate` (Operations used `captured`), and
five archived tasks carried a `superseded` status the process never documented.

Decision: **remove both, retain and widen `Task`.** The principle is that the
framework keeps responsibilities, authorities, and boundaries and does not keep
state names; `Task grooming` passes that test, the two removed entries did not.
This is the fifth pruning disposition, after goal removal, boundary demotion,
open problem, and problem strategy.

During review the maintainer asked why `Task collection` was still there, and it
was removed too — the sixth pruning. Folding the other two entries into `Task`
had left it as `Task` pluralized plus a delegation statement `Task` now carried,
and the framework used the term nowhere outside its own heading. Problems have
no collection concept, the third time a missing analogue on the other half of a
pair has exposed a redundant entry. This reopens the 2026-07-12 task-collection
review, which the strategy's non-waterfall clause permits: that demotion was
correct for what the entry held then, and this session is what made the
remainder redundant.

`Selected task` had been stale for one day — it still required an open problem
after the compilation-invocation session removed that rule from three of the
five siblings and missed the fourth. That is evidence for the disposition
rather than a defect fixed alongside it: the fragmentation is what let a careful
session leave a contradiction behind.

Framework Operations separately collapsed twelve task statuses to `open` and
`closed`, mirroring the problem lifecycle. Six of the eleven documented statuses
had never been used once. Closure reasons, readiness, deferral, and selection
became recorded dispositions rather than states — the same demotion `solved`
received. Whether losing the `captured`/`ready` distinction costs anything is
the open question the maintainer chose to judge in review.

In iterative review the maintainer then cut deeper than the operator had:
the `Task` entry was reduced from 28 lines to 8, the definition was
generalized to "produces an artifact," and selection and authority were
removed from tasks entirely as non-generic concepts the general loop-ownership
delegation already covers. Who chooses work, and whether anyone authorizes it,
is now each system's process choice; Operations' maintainer-selects rule became
visibly an instance rule. The maintainer also set the compilation principle
that definitions live in the vocabulary and the framework definition
references them, recorded in `knowledge-compilation.md` with a captured
backfill task for the README's remaining duplication.

### 2026-08-06 — plain-language constraint added to the strategy

Source: [plain-language grooming session](../streams/working-sessions/2026-08-06-plain-language-constraint-grooming.md).

The maintainer asked whether the current strategy makes the system simple in
language as well as in structure, so that its documents are easy to understand.
Grooming established that the audience is unchanged — the maintainer and
capable reviewers, not a new consumer group — and that plain wording is a
writing-quality bar on the surfaces they read. Per the strategy-scope rule, the
change guides only P1, so it lives in P1's strategy rather than the system
strategy.

Decision: **revise**. The strategy now requires every retained surface to be
written in plain language, treating wording a reader stumbles over as avoidable
complexity to remove like any other. The teach-back validation pass now asks
the reviewer to flag wording they had to reread or could not restate. Remaining
concept reviews carry the constraint forward; a captured backfill task
(`apss.plain-language-backfill`) covers surfaces already written, scoped by the
maintainer to everything — framework package, Operations processes, problem
files, and stream documentation — with splitting into sessions left to task
grooming.

### 2026-08-06 — purpose review task closed as superseded

Source: [purpose review session](../streams/working-sessions/2026-08-06-purpose-review.md).

The ninth review session found its question already answered: the vocabulary
never defined a `Purpose` entry, and the system-concept review's 2026-07-12
field audit had ruled that the declaration's `purpose` field restates the
problem and removed it — superseding `review-vision` in the same sweep but
missing this sibling task. Verification found no conceptual residue: what
survives is the stream `purpose` property (owned by the information-stream
review), descriptive headings, and ordinary prose.

Decision: close `apss.review-purpose` as superseded by
`apss.review-system-concept`, mirroring vision's treatment. No normative
surface changed; the pruning count stays at six. The missed-sibling pattern —
a broad decision making open tasks moot without a checklist that asks which
ones — is recorded for the adversarial validation pass. Two Direction-level
reviews remain before the order descends: authority, then subsystem and
relationships.

### 2026-08-06 — authority removed from the framework

Source: [authority review session](../streams/working-sessions/2026-08-06-authority-review.md).

The tenth concept review found authority used normatively across five
vocabulary entries without ever being defined, one delegation principle
stating the actual model, and "declared authority" wording left over from a
declaration model that no longer declares anything. The operator recommended
the shallow cut: keep the delegation principle, fix the residue. The
maintainer cut deeper, and grounded it in the model itself: APS defines no
owners or personas, so there can be no concept of authority — it can be part
of a specific implementation, but not of the MVP.

Decision: **remove** authority from the framework entirely — the seventh
pruning disposition. The decisions it qualified are untouched; the framework
simply no longer implies it defines who may make them. "Process participants"
now carries the single boundary statement, and instance-level authority rules
like Operations' maintainer-as-adaptation-approver stay where they are, as
the ruling intends. The framework's concept-to-concept "owns" language and
the source-of-truth sense of "authoritative" are unaffected; both are flagged
for the teach-back pass. One Direction-level review remains: subsystem and
relationships.

### 2026-08-06 — learning-loop work kept under P1

Source: [learning-loop application
session](../streams/working-sessions/2026-08-06-learning-loop-application.md).

Asked whether the system-learns-from-its-own-operation work should open a
second problem, the maintainer kept it under P1: it implements strategy
point 5 (verify the maintainer can understand and operate the whole process)
and the signal's understand-and-run clause. The alignment and adversarial
beat was applied to the package itself before this decision; it sorted the
items into evidence-backed (intake consolidation, snapshots, adversarial
beat, session lessons) and anticipation-heavy (declaring a heartbeat session
that has never run), and the maintainer selected the evidence-backed subset.

Decision: **retain and address under P1**. Heartbeat runs as ordinary
grooming invocations first and may be declared after observed use.
Reconsideration trigger: if the learning-loop work outgrows P1's signal or
survives P1's closure, propose it as its own problem.

### 2026-08-06 — subsystem merged into child system; relationship model confirmed

Source: [subsystem and relationships review
session](../streams/working-sessions/2026-08-06-subsystem-and-relationships-review.md),
the first automated brainstorming invocation.

The eleventh and last Direction-level concept review found no machinery to
prune — earlier reviews had already removed parent fields, the relation
registry, and universal cardinality — but found one concept under two names:
the framework definition bold-defined "subsystem" while the vocabulary,
the Problem decomposition section, and most of the visualization guide said
"child system." The same missing-analogue heuristic that exposed prior
duplicates applied: problem decomposition needs no "subproblem" entry, so
system decomposition needs no separate subsystem concept.

Proposed disposition, taken autonomously per the session type and pending
maintainer review: **merge** the term into "child system" everywhere and state
in the definition that being a child names only the decomposition origin. The
independent agent review overturned the session's initial no-vocabulary-entry
choice: the concept's rules were scattered — the becoming-a-child condition
in `System problem`, the link rule in `Adaptive problem-solving system`, the
process/capability boundary only in the framework definition — and the
compilation principle places a concept's meaning and boundary in the
vocabulary, so a concise `Child system` entry consolidates them and the
definition paragraph was trimmed to its operational explanation. The
parent-side link model (child declares no parent) was confirmed as the whole
relationship model. Orphaned "governance relationships"
wording in the visualization discipline — left without a referent by the
authority removal, though predating it — was cleaned up in passing. This
closes the Direction-level portion of the review order; the review order
descends next.
