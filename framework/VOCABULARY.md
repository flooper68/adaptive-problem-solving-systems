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
against the system problem and supplies the signal that guides later
optimization. The signal may be qualitative or quantitative; APS does not
require a mathematical score.

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

### Strategy

The current evidence-informed theory and approach for changing one problem. A
strategy guides work and changes when verification or other evidence challenges
its assumptions or effectiveness. The system strategy belongs to the root
system problem; every smaller open problem has its own problem strategy.

### System problem

The stable root problem an adaptive problem-solving system exists to solve,
including the affected consumer or environment. It is constitutive of the
system and defines its problem-owning boundary. The system problem is not
revised or replaced within APS; improved understanding and clarification belong
to system strategy. When a decomposed problem receives an independent boundary
and complete loop, it becomes the system problem of a child system; otherwise
it remains an open problem within the current system. The same solved-versus-
closed distinction applies to the root problem; the system's process defines
what root closure means for the system's subsequent lifecycle.

### System strategy

The system's current theory, interpretation, and approach for solving its
system problem: how it interprets evidence, decomposes and chooses among smaller
problems and possible responses, guides their strategies, plans, executes,
validates, learns, and coordinates its subsystems. It is the sibling
`STRATEGY.md` document linked from `SYSTEM.md` and may change when evidence
warrants it.

## Evidence and interpretation

### Evidence

Recoverable information relevant to a claim, problem framing, decision, or
result. Evidence may support, contradict, or leave a conclusion uncertain; its
existence does not make one interpretation or response authoritative.

### Feedback

Evidence about a consumer's, operator's, validator's, or other participant's
experience of a system or artifact. Feedback may reveal, change, or help close
an open problem, but a report does not automatically become a problem or
authorize work.

### Insight

An explicit interpretation inferred from evidence. An insight may explain or
reframe an open problem, but remains distinguishable from its source evidence,
an authorized decision, and executable work.

### Question

A statement of unresolved uncertainty. A question may be used to frame or
investigate an open problem; recording it does not by itself make it a problem
or selected task.

## Problems and tasks

### Open problem

An evidenced, unresolved smaller problem that decomposes the system problem or
another open problem. It states a gap to understand or change, not a proposed
solution. Open problems belong to the system's active problem hierarchy and
remain there until closed or otherwise inactive. They do not become child
systems unless they receive an independent boundary, ownership, and complete
problem-solving loop.

An open problem may remain relevant across many working sessions and tasks. It
owns the long-running evidence, desired change, signal, strategy, and concise
history of material decisions; it is not an executable work package. `Open` is
one of the problem's two lifecycle states; the other is `closed`. The history
preserves why it was opened, materially reframed, changed, closed, or reopened
without duplicating routine task activity or native evidence.

### Problem strategy

The current approach for resolving or reducing one problem. An open problem's
strategy is informed by the system strategy and relevant decomposition context,
guides the work selected for that problem, and is revised when its signal or
other evidence challenges the approach.

### Task

A bounded unit of actual work that iterates on a problem's solution by
implementing or testing part of its strategy. A task processes information into
an attempt, decision, result, or other inspectable change. Its execution and
results are also an information source for verification and future learning.
Tasks include implementation, research, experiment, discussion, review, or
remediation. The task system of record preserves the current state and the
information needed to understand, perform, stop, and resume it.

A task implements or tests part of an open problem's strategy; it does not
duplicate the whole problem or use problem closure as its own scope. Prefer a
task small enough to produce one inspectable result in one working session. If
it contains several independently reviewable results or stopping points, split
it before selection.

### Task collection

The tasks currently known to and managed by a system, including candidates,
selected work, active work, and deferred work. The system's process chooses its
system of record, organization, views, and lifecycle states; APS does not
prescribe files, folders, or a task-management product.

### Problem signal

An observable qualitative or quantitative condition used to judge whether an
open problem is worsening, improving, or sufficiently resolved. A signal may
be a measure, repeated observation, validation result, or other fit-for-purpose
evidence; APS does not require artificial numerical scoring.

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

### Task candidate

A bounded action that may be considered for execution, such as a task,
research inquiry, experiment, discussion, review, or remediation. A candidate
may be captured before its problem relationship is clear, but that gap must be
resolved before selection.

### Task grooming

The authority-governed processing of candidate actions into bounded work and a
readiness disposition for open problems. Task grooming checks scope, problem-
strategy relationship, evidence, expected result, dependencies, validation,
responsibility, and stopping conditions. It does not open, reframe, prioritize,
or close problems; an unrepresented gap returns to problem grooming before work
is selected. Problem and task grooming are distinct responsibilities even when
a system combines them in one meeting, process, tool, or cadence.

### Selected task

A task selected under declared authority. It identifies at least one open
problem and implements or tests that problem's strategy. Small execution steps
may inherit that relationship from their containing task rather than repeating
it.

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
does not by itself show that an open problem improved or a consumer outcome
occurred.

### Outcome

The change an artifact should cause for its consumer or environment. Outcome
evidence, not work or artifact completion alone, shows whether the relevant
open problem improved.

### Solved

An assessment that the desired change for an open problem occurred and its
problem signal or equivalent outcome evidence supports the conclusion.
“Solved” describes the evidenced condition and may be reconsidered when new
evidence arrives. It is not a lifecycle state and does not itself close the
problem.

### Closed

An authorized decision that the system will no longer treat a problem as open.
A problem may close because it was solved, disproved, duplicated or replaced,
moved outside the system boundary, ceased to matter to the system problem, or
had its remaining risk explicitly accepted. Closure records the reason,
evidence, and authority and does not imply “solved.” `Closed` is the second
problem lifecycle state. New evidence may justify reopening the problem.

### Learning

A reusable change in understanding derived from evidence and results. Learning
may revise an open problem or the problem decomposition, strategy, process,
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
