# APS changelog

Simple history of material framework changes. Git remains the detailed audit
trail.

## 2026-08-06 — current state defined as a first-class concept

Added `Current state` to the vocabulary. The framework had leaned on the term
in five places — task recoverability, working-session records, and the
archive were all defined against it — without saying what it is or who owns
it: exactly the ownerless-state defect the adversarial checklist hunts.

The entry has two halves. Current state itself is the present condition of a
system's work — open problems and their current meaning, work in flight, its
intended result, responsible participant, stopping condition, and next step —
owned by the problem and task systems of record, which APS already required
to keep it recoverable. A current-state view is an optional derived,
date-stamped snapshot compiled from those records for orientation,
resumption, and handoff; it is subordinate and loses to the authoritative
records on any conflict, and its date makes staleness visible. APS prescribes
no view format, location, or refresh cadence. No lifecycle machinery was
added: current state is a responsibility and an optional derived view, not a
new durable identity.

The evidence is Framework Operations' own use: the current-state-reporting
task delivered a root `STATE.md` plus per-problem `Current state` sections,
and the maintainer reported the pattern very useful and directed its
promotion into the framework. This is the first evidence-driven addition
under the add-complexity-only-when-demonstrated strategy, after seven
pruning dispositions.

## 2026-08-06 — authority removed from the framework

Removed authority as a framework notion. APS defines no owners, personas, or
roles, so it has nothing to attach a concept of authority to; who participates
in a process and who makes which decision are choices each system's processes
state for themselves. The maintainer ruled this during the authority concept
review: authority can be part of a specific implementation, but not of the
MVP framework.

The word never had a vocabulary entry, but it qualified decisions across the
package: open and closed were "authorized decisions," problem grooming and
adaptation were "authority-governed," the loop diagram adapted "with declared
authority," and view 3 showed a "Declared approver." All of those qualifiers
are gone. The decisions themselves are untouched — problem grooming still
opens and closes problems, adaptation still accepts and applies changes — the
framework just no longer implies that it defines who may make them.

The "Process participants and authority" section became "Process
participants" and now carries the single remaining statement of the boundary.
"Declared authority" was residue from the earlier declaration model: SCHEMA.md
had already excluded authority from the declaration, so nothing was declared
anywhere. The creating-a-system steps, assessment checklist, and work-session
process responsibilities dropped authority from their lists. Instance-level
authority statements, such as Framework Operations naming its maintainer as
adaptation approver, are unaffected — that is exactly where the ruling says
such rules belong.

## 2026-07-27 — the task family reduced to Task and Task grooming

Removed the `Task candidate`, `Selected task`, and `Task collection` vocabulary
entries. `Task` and `Task grooming` are the family's only remaining concepts.

The framework already said twice that APS prescribes no fixed task lifecycle
states, then defined two of them as concepts. Both entries named positions on a
workflow rather than distinct kinds of thing, and each showed it: `Task
candidate` defined a candidate as "a bounded action... such as a task,
research inquiry, experiment, discussion, review, or remediation" — the list
`Task` then carried — and named a state its only implementation does not
have. `Selected task` still required "at least one open problem" a day after
that rule was dropped, because an edit pass touching three of five siblings
missed the fourth.

The load-bearing content survived the removal: `Task` now states that work may
be captured before its problem relationship is clear and that selection is the
authorized act that commits the task to execution and resolves that
relationship; the framework definition carries execution-step inheritance. The
entry was then rewritten for concision in maintainer review — three short
paragraphs, with elaboration such as session sizing and system-of-record
responsibilities left to the framework definition alone.

The definition itself was generalized in the same review. It had enumerated
what a task produces — "an attempt, decision, finding, or change" — and what
tasks include — "implementation, research, experiment, discussion, review, and
remediation." The maintainer judged the enumerations too specific to hold in
general; a task simply produces an artifact. That word already carries the
needed meaning — `Artifact` is "an inspectable output produced by a system" —
so the definition now leans on an existing concept instead of re-describing
it.

A final cut reduced the entry to boundary only. The problem-less selection and
own-acceptance clauses repeated what the entry's closing paragraph and the
framework definition already say, and the whole-problem, closure, and
splitting rules moved to the framework definition beside the sizing
preference.

The maintainer then removed selection and authority from tasks entirely: they
are not generic concepts at the task level, and the framework already said so
in general — "Loop ownership does not prescribe who performs or approves each
step. Those authorities belong to the system's chosen processes." A declared
selection authority for tasks was over-specifying that delegation. `Task` now
states that APS prescribes no task states, no selection or authority
machinery, no system of record, and no tooling; how work is chosen, and who
decides, belong to each system's process. `Task grooming` is no longer framed
as authority-governed and no longer references a declared selection
authority; its boundary against problem grooming is unchanged. The framework
definition requires recoverability of current work rather than authorized
selection, and "opening a problem does not authorize a task" became "does not
by itself start work on it." The explicit problem relationship survives inside
recoverability: the system of record carries the addressed problem and
strategy when the task has one. Problem lifecycle authority — open and closed
as authorized grooming decisions — is untouched.

`Task collection` went the same way once the other two were folded in. It had
enumerated candidate, selected, active, and deferred work — contradicting its
own next sentence — and with that list gone it read as `Task` pluralized plus a
delegation statement `Task` now carries. The framework never used the term
outside its own heading, and problems, the other durable groomed thing, have no
collection concept. Its surviving ruling is now one sentence of `Task`: APS
names no task states and prescribes no system of record, organization, views,
files, folders, identifier format, or task-management product.

The principle behind the removal is stated directly: the framework keeps
responsibilities, authorities, and boundaries, and does not keep state names.
What APS requires of selection is that the act be authorized and its result
recoverable, not that a particular state name exist. `Task grooming` passes
that test and is unchanged; "task candidate" and "selected task" survive as
ordinary wording.

## 2026-07-27 — a task may or may not be in the context of a problem

Dropped the rule that a task must address at least one current problem before
selection. The maintainer's evidence is that real operation produces small
one-off work — chores, fixes, and errands — that has no long-running gap
behind it, and forcing a problem link would either invent problems or leave
the work untracked. No new task kind is named for this; the vocabulary simply
states that a task may or may not be in the context of a problem.

Most tasks still iterate on a problem's solution by implementing or testing
part of its strategy, and tasks selected for a problem must still do so rather
than attach by identifier alone. A task without one is selected under the same
declared selection authority, remains bounded and owned, and is verified
against its own acceptance conditions instead of a problem signal. Recurring
or substantial problem-less work is evidence of an unrepresented gap for
problem grooming, so the escape hatch does not silently erode the hierarchy.

`Task`, `Task candidate`, and `Task grooming` entries and the framework
definition's task-selection paragraph carry the change; the task system of
record now needs the addressed problem and strategy only when the task has
one.

## 2026-07-26 — problem signal must be readable while the problem is open

Sharpened the problem signal concept, renamed it `Signal`, and widened
`Outcome` to cover the target it was being confused with.

The old definition — "an observable condition used to judge whether a problem is
worsening, improving, or sufficiently resolved" — was satisfied by a restated
goal. It fused three jobs: the indicator observed, the threshold that counts as
enough, and the reading itself. The threshold job overlapped the problem's
desired change, which the framework required of every problem but never defined,
so writers stated the target twice and never named an observation.

Rather than add a second entry, `Outcome` absorbed it. That entry had defined
itself through an artifact — "the change an artifact should cause" — while
evidencing itself through a problem, "shows whether the relevant problem
improved." It is now anchored to the problem in both halves: the change
resolving a problem should produce for its consumer or environment, of which
every problem states its *desired outcome*. Artifacts contribute to an outcome
without constituting one. "Desired change" is retired as framework wording.

The evidence was the framework's own worked example. P1's signal, "the
maintainer can understand and run the whole process," has no reading while P1
is open; it becomes observable only once P1 is already resolved. Seven concept
reviews recorded no value for it, the last two carrying the same sentence
verbatim.

A signal now must be readable while the problem is open: a value now, another
on a later attempt, and the two comparable. Readings may be qualitative — a
teach-back, a consumer judgment — but a reading must be takeable. A signal that
reads work performed rather than the problem's condition does not distinguish
activity from improvement.

"Signal" also named two things. Verification was said to "supply the signal that
guides later optimization" while the problem's signal was the yardstick
verification compares against. Verification now supplies *evidence*; it *reads*
the signal. `Solved` reads against a signal reading rather than the signal
itself. With that collision resolved, the entry is `Signal` rather than `Problem
signal`, matching `Strategy`; "problem signal" remains ordinary wording for the
signal of one problem, as "problem strategy" and "open problem" do. Framework Operations propagated the change: verification records the
value observed or records the signal as unreadable, and problem grooming treats
a signal no attempt has been able to read as a trigger.

## 2026-07-26 — problem strategy merged into strategy

Removed `problem strategy` as a separate APS concept. The framework defined one
concept twice: `Strategy` under *Direction* and `Problem strategy` under
*Problems and tasks*, sixty lines apart, and again as two bullets four apart in
the README core definitions. The entries differed only in wording — "changing
one problem" against "resolving or reducing one problem" — and named no
distinct responsibility, owner, evidence, or lifecycle.

The vocabulary's own shape showed the redundancy. `Problem` and `System
problem` are a general concept and its specialization; `Strategy` and `System
strategy` are the same pair. `Problem strategy` was the unspecialized case
given a second entry of its own, with no analogous `Problem problem`.

The retained `Strategy` entry absorbs what only the removed one stated: every
problem has a strategy, it is informed by the system strategy and the problem's
decomposition context, it guides the work selected for that problem, and it
changes when that problem's signal, verification, or other evidence challenges
it. Ownership and change authority are now stated where the concept is defined.
"Problem strategy" remains ordinary wording for the strategy of one problem
where that scope must be distinguished from the system's, as "open problem" did
in the preceding change. Framework Operations corrected one grooming bullet
that scoped a problem's strategy to open problems only.

## 2026-07-26 — open problem removed as a separate concept

Removed `open problem` as a distinct APS concept. It fused two independent
predicates: a structural claim that the problem is not the root, and a lifecycle
claim that the problem is currently open. The lifecycle half never
distinguished anything, because the root system problem carries the same
solved-versus-closed distinction; the structural half was already stated by the
general problem definition and by the system problem from the other side. The
framework also had no name for a decomposed problem that had been closed, even
though closure, reopening, and decision history all need to refer to one.

`Open` and `closed` are now simply the two lifecycle states of a problem, and
`open` is defined alongside `closed` as an authorized problem-grooming decision
that admits an evidenced proposal to the active decomposition. The long-running
evidence, desired change, signal, strategy, and material decision history moved
into the general problem definition, which is where they always applied.

Corrected three definitions that wrongly scoped to open problems only: an
artifact or outcome may show that any problem improved, and `solved` is an
assessment made about a problem including at the moment of closure. Kept "open
problem" as ordinary adjective-plus-noun in the grooming, orientation, and task
surfaces that genuinely mean a problem currently in the open state, and used
explicit decomposition wording where the framework previously leaned on "open"
to mean "not the root". Framework Operations dropped the redundant
`type: open-problem` field from its problem file, which already carried
`status: open`.

## 2026-07-26 — system strategy retained and its definition aligned

Reviewed system strategy against the concept review test and retained it as a
distinct concept with system-wide scope, its existing representation, and no
lifecycle machinery. The review raised whether the concept is two things: the
approach to the root problem, which the general strategy definition already
covers, and the system's operating model for interpreting evidence, decomposing
problems, guiding lower strategies, verifying, learning, and adapting. The
maintainer decided that system strategy legitimately carries both and kept the
standalone definition rather than demoting it to the root problem's strategy.

Aligned the vocabulary and framework definitions, which previously named
different responsibilities in different order; used verification for the loop
stage rather than validation, which APS reserves for artifact and outcome
validation; stated the scope distinction from problem strategy explicitly; and
linked strategy change to adaptation. The declaration contract, the `strategy`
link from `SYSTEM.md`, and the Framework Operations strategy are unchanged.

## 2026-07-12 — system boundary demoted to contextual description

Confirmed that system boundary is not a separate APS concept with its own
identity, state, lifecycle, or required declaration. A system's root problem
and complete-loop ownership establish its identity; boundary language may
remain ordinary contextual description. Removed declaration guidance that
specifically invited a boundary explanation and removed the duplicated
Framework Operations boundary section. Retained the existing child-system
wording, where an independent boundary is descriptive shorthand rather than an
additional normative object.

## 2026-07-12 — goal removed and problem hierarchy clarified

Removed `goal` as a separate APS concept because it duplicated the desired
change already carried by problems and obscured the relationship among problem
and strategy. Defined problem generally and made the system problem the root of
an evolving hierarchy. Evidence and learning decompose it into smaller open
problems, each with its own desired change, signal, and strategy; tasks perform
bounded attempts on those strategies and return evidence to the loop. Added
Framework Operations and P1 as a worked example and delegated child systems
only when a decomposed problem receives its own boundary and complete loop.
Left the representation of relationships among smaller problems to each
system's process: APS requires neither parent fields nor a strict tree.

Defined the minimal problem lifecycle as `open` and `closed`. Tasks supply
attempt and result evidence but never change problem state merely by finishing.
Verification compares that evidence with the problem signal. `Solved` remains
an evidence-based assessment supporting a separate authorized closure decision;
new evidence may reopen a closed problem.

Separated problem discovery from creation authority. Streams and processes
retain their own observations, issues, results, and insights; source-specific
grooming may propose higher-level problems; problem grooming alone decides
whether to open, merge, revise, defer, or reject those proposals.

Required each problem's chosen system of record to retain a concise history of
material decisions and their evidence and authority: opening, meaningful
reframing, strategy or signal changes, closure, and reopening. Routine task
activity and detailed source evidence remain in their own records.

Required problem-set re-evaluation without prescribing a heartbeat or cadence.
Each system may implement problem grooming through events, a schedule such as
cron, continuous processing, or a mixed approach.

Made the evolving problem hierarchy APS's adaptive planning structure and
separated its maintenance from executable-work grooming. Problem grooming acts
on proposed and existing problems; task grooming shapes bounded responses and
their readiness for selection. Systems may combine them operationally but must
preserve their distinct decisions and authority.

Removed the normative problem-file schema, `problems/` layout, archive path,
and prescribed identifiers and fields. APS retains only the logical problem
concepts and recoverability responsibilities; each system chooses its tools,
views, record shape, and storage.

Made the root system problem constitutive and stable. Clarification and evolving
interpretation belong to system strategy, while learning revises smaller
problems and their decomposition. APS defines no root-problem replacement
transition.

Added recommended process-design questions for surprising outcomes, unexpected
time or resource use, and regression in the verification value function.
Processes specialize when and how to ask them; positive answers preserve raw
evidence for interpretation and later recompilation but do not automatically
create problems.

Added lightweight learning guidance for material decisions and course
corrections: compare expected effects with later signals or outcomes, assess
help or harm, and retain a brief causal hypothesis only when it may inform
future work. Alternatives and challenging evidence are included only when
material rather than required as grooming ceremony.

## 2026-07-12 — task organization delegated to each system

Removed normative task-file, folder-layout, and fixed lifecycle-state rules.
APS defines the task and traceability responsibilities while each system's
process chooses its task system of record and organization, such as repository
files, Jira, GitHub, Linear, or a database. Framework Operations separately
flattened its current task files into `operations/tasks/` and retained
`operations/tasks/archive/` for inactive material.

Clarified that a task is actual bounded work that iterates on a problem's
solution, processes information into an inspectable attempt or result, and
supplies execution and result evidence to verification and future learning.

## 2026-07-11 — framework renamed to APS

Renamed the method from Adaptive Problem-Solving Systems (APSS) to Adaptive
Problem Solving (APS) so it is simpler to read and say and no longer conflates
the general method with the systems that instantiate it. Updated the current
framework, operations, contributor guidance, schema URN, and
declaration terminology. Stable historical record and task IDs retain their
existing `apss.*` namespace.

## 2026-07-11 — system declaration identity simplified

Removed `aps_version`, system `id`, `status`, and `parent` from the normative
declaration contract and live declarations. A system's name is sufficient
identity. Problem decomposition no longer creates a declaration-level parent
tree: the originating problem definition, strategy, or process links to the
named system handling the decomposed problem. Updated schema guidance,
visualization, and system creation accordingly.

## 2026-07-11 — generic limits concept removed

Removed the generic limits field and terminology from current framework,
operations, process, task, and application surfaces. Concrete limits now appear by
their operational role, such as problem context, input, decision boundary,
operating condition, verification condition, risk, or authority rule.

## 2026-07-11 — system-wide roles removed

Removed the required `roles` block and its universal owner, operator, consumer,
validator, and adaptation-approver lists. Each process now defines its own
participants, responsibilities, and applicable decision authority.

## 2026-07-12 — system declaration reduced to loop orientation

Reduced the normative system declaration to `name`, `problem`, `verification`,
`strategy`, `process`, `work_sessions`, and `streams`. Planning,
execution, learning, participation, authority, uncertainty handling,
contextual artifacts, operating conditions, problem decomposition, and other
relationships now belong to the linked sources that implement them.

Retained `work_sessions` as the system-specific catalog of bounded session
types, but removed the universal requirement for `brainstorming` and
`problem-grooming`; an empty catalog is valid. Replaced the fixed artifact and
outcome validation block with one verification value-function declaration.
Removed the universal aspirational-future field because it usually restated the
desired inverse of the problem; longer-horizon direction may live in strategy
when useful.

Made `verification` a direct process link. Framework Operations now uses the
single `processes/verification.md` process for immediate correctness checks,
problem-signal evaluation, and delayed improvement evidence; the separate
artifact- and outcome-validation processes were superseded.

Renamed the Framework Operations loop implementation to the canonical
`processes/process.md` path and updated its declaration and stream consumers.

Removed the machine-readable JSON Schema and merged the separate system
template into `SCHEMA.md`. That document is now the single human-readable
declaration contract and authoring template while APS is being polished.

## 2026-07-12 — provisional examples deferred

Removed the provisional example directory while the framework is being
polished. Framework Operations is now the first and only current APS
application. Cross-domain examples remain deferred until the first complete
Operations loop has produced validated learning and the framework is stable
enough for examples to test it without becoming synchronization work.

## 2026-07-11 — APS method and system-instance distinction

Clarified that APS is the general problem-solving method and that an adaptive
problem-solving system is one concrete instantiation: a problem statement plus
an iterative loop that plans and performs work, verifies its effect, learns
from information and outcomes, and adapts later attempts. Replaced the system
concept's eleven-item identity checklist with this core and made hierarchy a
means of decomposing a larger problem into child-system problems. Clarified
that a child owns its loop even when its parent supplies feedback,
verification, or insights. Left the lifecycle consequence of solving a problem
to the system's own definition rather than prescribing a universal lifecycle
process or automatic retirement. Identified information grooming as a general
responsibility for evidence processing and decision making, with each problem
or input stream free to implement the grooming it needs. Made artifacts
contextual to the problem rather than an identity criterion for every system;
the universal responsibility is to attempt a solution and verify its effect on
the problem. Defined verification as the loop's qualitative or quantitative
value function: evaluation of an attempt against the problem that guides later
optimization. Clarified that loop ownership does not prescribe who performs or
approves each step; those authorities belong to each system's processes.

## 2026-07-11 — problem and task scope clarification

Clarified that an open problem is the long-running unit of improvement and may
span many sessions and tasks. A task implements or tests one bounded part of a
problem strategy and should preferably produce one inspectable result in one
working session. Umbrella work that duplicates the problem or contains several
independent stopping points should be split before selection.

## 2026-07-10 — goal-linked open problems and normative vocabulary

Added a lightweight problem layer between the current goal and executable
tasks. Each open problem has one file containing its goal, evidence, desired
change, signal, strategy, and grooming history; each task has one file naming
the problem strategy it implements or tests. Removed the redundant `PLAN.md`:
the system strategy owns the goal, and the `problems/` and `tasks/` directories
are the current state. Closed problems and inactive tasks move to explicit
archives. A later simplification removed the generic
work log: active task files own resumable state, material work-session records
own session history, native streams own domain evidence, and Git owns detailed
repository history. Task candidates live under `tasks/backlog/`, selected and
active tasks at the task root, and inactive tasks under `tasks/archive/`.
Defined simple creation, grooming,
improvement, solution, closure, and reopening guidance without adding a
system-declaration schema object. Defined problem grooming as the second
required work session: problem files retain its authoritative result, while the
working-session record retains material discussion and provenance.
Added the normative APS vocabulary and demonstrated the convention in
Framework Operations and the CNC example.
Corrected the stream-ID schema rule, which had unintentionally required every
stream to use the ID `brainstorming`.

Made strategy explicit at two levels. A system declaration now links to an
independent sibling `STRATEGY.md` that guides problem grooming and problem
selection; every problem file states its own strategy, which guides selected
work and is revised from evidence. For the current MVP problem, adopted a
use-first simplification strategy and human-feedback outcome verification.

## 2026-07-10 — system-owned work sessions

Initially defined `brainstorming` as the single required APS work session.
It discusses an idea, task, or research topic with the responsible user and
iteratively compiles reviewable changes into framework knowledge or a concrete
system instantiation. Its declaration contains only an ID, description, and the
same-named process link. Clarified that streams carry observations and retained
records; they are not the work that processes them.

## 2026-07-10 — evidence records and executable work

Clarified that discussion summaries, insights, questions, and decisions are
durable evidence, inference, uncertainty, or decisional records rather than
work merely because they are retained. Durable task records contain bounded
actions that can be performed and evaluated; executable responses link back to
the records that motivated them.

## 2026-07-10 — validation process placement

Clarified the conventional capsule layout by placing artifact- and
outcome-validation implementations under `processes/`. The `validation` fields
remain required declarations of what is checked; validation evidence remains in
work records or streams rather than a required directory.

## 2026-07-10 — producer and product boundary clarification

Clarified that a repository may act as a container with an operational system
capsule beside the artifacts it produces. The reference repository now declares
`operations/` as the system that improves the normative `framework/`, with
`examples/` as supporting, non-normative artifacts.

## 2026-07-09 — self-hosting boundary clarification

Clarified that a repository may itself be a root system boundary and may keep
consumer-facing artifacts separate from the operations that produce them when
all declared paths remain explicit. The APS framework package is now the
primary artifact of a root stewardship-system declaration; implementation
examples are supporting, non-normative artifacts.

## 2026-07-09 — initial definition

Defined APS as a domain-independent framework for nested systems that own a
problem, artifact, consumer outcome, full adaptive loop, evidence streams,
compiled knowledge, and adaptation authority. Added the declarative system
schema/template, visualization projections, physical-production example, and
deferred foundations-research work.
