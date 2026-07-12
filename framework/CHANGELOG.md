# APS changelog

Simple history of material framework changes. Git remains the detailed audit
trail.

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
