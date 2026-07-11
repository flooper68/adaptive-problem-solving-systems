# APSS changelog

Simple history of material framework changes. Git remains the detailed audit
trail.

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
Added the normative APSS vocabulary and demonstrated the convention in
Framework Operations and the CNC example.
Corrected the stream-ID schema rule, which had unintentionally required every
stream to use the ID `brainstorming`.

Made strategy explicit at two levels. A system declaration now links to an
independent sibling `STRATEGY.md` that guides problem grooming and problem
selection; every problem file states its own strategy, which guides selected
work and is revised from evidence. For the current MVP problem, adopted a
use-first simplification strategy and human-feedback outcome verification.

## 2026-07-10 — system-owned work sessions

Initially defined `brainstorming` as the single required APSS work session.
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
all declared paths remain explicit. The APSS framework package is now the
primary artifact of a root stewardship-system declaration; implementation
examples are supporting, non-normative artifacts.

## 2026-07-09 — initial definition

Defined APSS as a domain-independent framework for nested systems that own a
problem, artifact, consumer outcome, full adaptive loop, evidence streams,
compiled knowledge, and adaptation authority. Added the declarative system
schema/template, visualization projections, physical-production example, and
deferred foundations-research work.
