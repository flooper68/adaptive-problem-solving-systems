# APS vocabulary

This vocabulary is the normative reference for recurring APS terms. The
framework definition explains how the concepts operate together; this file
keeps their meanings and boundaries concise. When ordinary domain language
uses a term differently, a concrete system should state that local meaning
without silently changing the APS meaning.

## Direction

### Adaptive Problem Solving (APS)

The domain-independent method for designing systems that iteratively solve a
defined problem, verify the effect of their work, learn from evidence, and
adapt later attempts. APS defines general problem-solving concepts and permits
systems to form a hierarchy for problem decomposition; it is not itself one
system instance.

### Adaptive problem-solving system

One concrete instantiation of APS. It owns a problem statement and an
iterative loop that uses strategy, planned work, information inputs,
verification, information grooming, learning, compiled knowledge, and
adaptation to solve that problem. Grooming is the general responsibility to
process relevant information and make decisions from it; a system may implement
different grooming for each problem or input stream. These are system
responsibilities rather than a prescribed sequence of separate processes or
components. Each system defines the processes that implement them. Other
participants, including a parent system, may supply feedback, verification,
insights, or other inputs; the system still owns how those inputs close and
adapt its loop.

Loop ownership does not prescribe who performs or approves each step. Those
authorities belong to the system's chosen processes.

Artifacts are contextual to the problem being solved. A system may produce one
or more inspectable artifacts as part of an attempt, but a separately named
artifact is not an identity criterion for every system.

Verification is the loop's value function: it evaluates a solution attempt
against the system problem and supplies the evidence that guides later
optimization. That evidence may be qualitative or quantitative; APS does not
require a mathematical score. Where a problem declares a signal, verification
reads it; the reading is evidence about the problem, distinct from the signal
that defines what to observe.

APS does not prescribe a universal lifecycle process or consequence when the
problem is solved; the system defines its response.

The system's name is sufficient declaration identity. APS does not require a
separate system ID, status, or parent field. A problem definition, strategy, or
process records any decomposition link to another named system.

### Problem

A condition affecting a consumer or environment that calls for understanding
or change. A problem states the condition, not its desired result, strategy, or
executable work. Problems form an evolving hierarchy as evidence and learning
decompose a larger problem into smaller problems.

A problem may remain relevant across many working sessions and tasks. It owns
the long-running evidence, desired outcome, signal, strategy, and concise history
of material decisions that guide and evaluate work on it; it is not an
executable work package. That history preserves why the problem was opened,
materially reframed, changed, closed, or reopened without duplicating routine
task activity or native evidence. `Open` and `closed` are its two lifecycle
states.

### Strategy

The current evidence-informed theory and approach for changing one problem.
Every problem has one, informed by the system strategy and by the problem's
decomposition context. A strategy guides the work selected for that problem and
changes when the problem's signal, verification, or other evidence challenges
its assumptions or effectiveness. The problem owns it; the system's declared
authority changes it.

The root system problem's strategy is the system strategy. *Problem strategy*
is ordinary wording for the strategy of one problem, used where that scope must
be distinguished from the system's; it is not a separate concept.

### System problem

The stable root problem an adaptive problem-solving system exists to solve,
including the affected consumer or environment. It is constitutive of the
system and defines its problem-owning boundary. The system problem is not
revised or replaced within APS; improved understanding and clarification belong
to system strategy. When a decomposed problem receives an independent boundary
and complete loop, it becomes the system problem of a child system; otherwise
it remains a problem in the current system's decomposition. The same solved-
versus-closed distinction applies to the root problem; the system's process
defines what root closure means for the system's subsequent lifecycle.

### System strategy

The system's current theory and approach for solving its system problem: how it
interprets evidence, decomposes and compares smaller problems and possible
responses, guides their problem strategies, executes work, verifies results,
learns, adapts, and coordinates its subsystems. Its scope is system-wide; each
problem strategy covers only that problem. It is the sibling
`STRATEGY.md` document linked from `SYSTEM.md` and changes through adaptation
when evidence warrants it.

## Evidence and interpretation

### Evidence

Recoverable information relevant to a claim, problem framing, decision, or
result. Evidence may support, contradict, or leave a conclusion uncertain; its
existence does not make one interpretation or response authoritative.

### Feedback

Evidence about a consumer's, operator's, validator's, or other participant's
experience of a system or artifact. Feedback may reveal, change, or help close
a problem, but a report does not automatically become a problem or
authorize work.

### Insight

An explicit interpretation inferred from evidence. An insight may explain or
reframe a problem, but remains distinguishable from its source evidence,
an authorized decision, and executable work.

### Question

A statement of unresolved uncertainty. A question may be used to frame or
investigate a problem; recording it does not by itself make it a problem
or a task.

## Problems and tasks

### Task

A bounded unit of work that produces an artifact. What a task does and what it
produces are themselves evidence for verification and later learning.

A task may or may not be in the context of a problem; most implement or test
part of one problem's strategy, and work may be captured as a task before that
relationship is clear. APS prescribes nothing further — no task states, no
selection or authority machinery, no system of record, no tooling. Each
system's process decides how its tasks are chosen, represented, and tracked.

### Signal

The observable a system reads to judge whether one problem is worsening,
improving, or sufficiently changed. A signal must be readable while the problem
is open: it yields a value now, another value on a later attempt, and the two
can be compared. An observation available only once the problem is already
resolved restates the desired outcome and cannot indicate movement toward it.

A signal may be a measure, repeated observation, validation result, teach-back,
consumer judgment, or other fit-for-purpose evidence. APS requires that a
reading can actually be taken, not that it be numerical. A signal that reads
work performed rather than the problem's condition does not distinguish
activity from improvement. The problem owns its signal and problem grooming
changes it; verification reads it and may find it uninformative.

*Problem signal* is ordinary wording for the signal of one problem, used where
that scope must be named; it is not a separate concept.

### Problem grooming

The authority-governed processing of proposed, open, or closed problems. Source-
specific grooming may propose a problem after interpreting observations,
issues, results, or insights, but problem grooming decides whether to open it,
merge it with or use it to revise an existing problem, defer it, or reject it.
For existing problems, grooming reviews relevance to the problem decomposition,
evidence, impact, framing, strategy, signal, and priority and may retain,
revise, address, close, or reopen them. The system's process defines cadence,
participants, storage, and decision authority; event-driven, scheduled,
continuous, and mixed operation are all valid.

### Task grooming

The processing of candidate actions into bounded work and a readiness
disposition. Task grooming checks scope, problem-strategy relationship,
evidence, expected result, dependencies, validation, responsibility, and
stopping conditions. It does not open, reframe, prioritize, or close problems;
an unrepresented evidenced gap is proposed to problem grooming. Problem and
task grooming are distinct responsibilities even when a system combines them
in one meeting, process, tool, or cadence.

### Working-session record

The durable record of one material invocation of a declared work session. It
identifies the session, participants, affected problems and tasks, material
evidence or decisions, and stopping point. It preserves history and provenance;
the problem and task systems of record remain authoritative for current state
and resumption.

### Archive

Durable inactive material retained outside the current-state views. Each
system's process chooses how inactive material is represented and retrieved.
Archiving changes visibility, not provenance or meaning.

## Results, learning, and change

### Artifact

An inspectable output produced by a system. Producing or accepting an artifact
does not by itself show that a problem improved or a consumer outcome
occurred.

### Outcome

The change in the affected consumer or environment that resolving a problem
should produce. Every problem states its *desired outcome*: the condition it
should reach, distinct from the strategy pursuing it and from the signal read to
judge movement toward it. Problem grooming changes it, and evidence that the
desired outcome itself was wrong is a reason to reframe the problem rather than
to retry the work.

Where a system produces artifacts, they contribute to an outcome but do not
constitute one. Outcome evidence, not work or artifact completion alone, shows
whether the problem improved.

### Solved

An assessment that the desired outcome for a problem occurred and a reading of
its problem signal, or equivalent outcome evidence, supports the conclusion.
“Solved” describes the evidenced condition and may be reconsidered when new
evidence arrives. It is not a lifecycle state and does not itself close the
problem.

### Open

An authorized decision that the system treats a problem as part of its active
decomposition. Problem grooming opens a problem when the proposal is evidenced,
relevant to the system problem, and distinct from current problems; a proposal
is not open until that decision is made, and opening a problem does not by
itself start work on it. `Open` is the first problem lifecycle state.

### Closed

An authorized decision that the system will no longer treat a problem as open.
A problem may close because it was solved, disproved, duplicated or replaced,
moved outside the system boundary, ceased to matter to the system problem, or
had its remaining risk explicitly accepted. Closure records the reason,
evidence, and authority and does not imply “solved.” `Closed` is the second
problem lifecycle state. New evidence may justify reopening the problem.

### Learning

A reusable change in understanding derived from evidence and results. Learning
may revise a problem or the problem decomposition, strategy, process,
validation method, or other future operation; an observation is not reusable
learning merely because it was recorded. For material decisions and course corrections,
learning may compare expected effects with later signals or outcomes and assess
whether the decision helped, harmed, or remains uncertain. When useful for
future work, it retains a brief causal hypothesis plus material alternatives or
challenging evidence; this is not required for every grooming invocation.

### Compiled knowledge

A reusable synthesis derived from evidence, interpretations, decisions, and
learning. It preserves material scope and uncertainty and remains revisable as
new evidence arrives.

### Adaptation

An authority-governed change to future operation based on evidence and
learning. Compilation proposes reusable knowledge; adaptation authorizes and
applies a change to task selection, strategy, process, validation, stream,
artifact, or system structure.
