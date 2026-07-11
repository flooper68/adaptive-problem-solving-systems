# APSS vocabulary

This vocabulary is the normative reference for recurring APSS terms. The
framework definition explains how the concepts operate together; this file
keeps their meanings and boundaries concise. When ordinary domain language
uses a term differently, a concrete system should state that local meaning
without silently changing the APSS meaning.

## Direction

### System problem

The durable condition an adaptive problem-solving system exists to change,
including the affected consumer or environment. It defines the system's
problem-owning boundary and is broader and more stable than a current goal or
open problem.

### Vision

The durable description of what better looks like if the system problem is
solved. A vision supplies direction but is not a bounded commitment or an
acceptance condition.

### Goal

A current, bounded result that moves the system toward its vision. A goal says
what result matters now; it does not prescribe the work or assume that the
gaps preventing that result are already understood. It is stated in the system
strategy rather than duplicated in `SYSTEM.md`.

### System strategy

The system's current theory and approach for reaching its current goal: how it
interprets evidence, identifies and chooses among open problems and possible
responses, guides their strategies, plans, executes, validates, learns, and
coordinates its subsystems. It is the sibling `STRATEGY.md` document linked
from `SYSTEM.md` and may change when evidence warrants it.

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

An evidenced, unresolved condition within a system that obstructs or threatens
a current goal. It states a gap to understand or change, not a proposed
solution. Open problems belong to the system's active problem collection and
remain there until closed or otherwise inactive. They do not become child
systems unless they receive an independent boundary, ownership, artifact, and
complete adaptive lifecycle.

An open problem may remain relevant across many working sessions and tasks. It
owns the long-running evidence, desired change, signal, and strategy; it is not
an executable work package.

### Problem file

The authoritative current record for one open problem: its stable ID, affected
goal, evidence, desired change, signal, strategy, and grooming history. Keeping
one problem per file gives the problem an inspectable lifecycle without turning
it into a separate APSS.

### Problem strategy

The current approach for resolving or reducing one open problem. It is informed
by the system strategy, guides the work selected for that problem, and is
revised when its problem signal or other evidence challenges the approach.

### Task

A bounded executable response stored as one file under `tasks/`, such as
implementation, research, experiment, discussion, review, or remediation. Its
file states its status, addressed problems, intended result, approach, owner,
stop condition, current state, and next step.

A task implements or tests part of an open problem's strategy; it does not
duplicate the whole problem or use problem closure as its own scope. Prefer a
task small enough to produce one inspectable result in one working session. If
it contains several independently reviewable results or stopping points, split
it before selection.

### Task collection

The current task files under `tasks/`: selected and active tasks at its root,
captured, grooming, ready, or deferred candidates under `tasks/backlog/`, and
inactive tasks under `tasks/archive/`. The folders and task statuses make a
separate plan or exhaustive index unnecessary.

### Problem signal

An observable qualitative or quantitative condition used to judge whether an
open problem is worsening, improving, or sufficiently resolved. A signal may
be a measure, repeated observation, validation result, or other fit-for-purpose
evidence; APSS does not require artificial numerical scoring.

### Problem grooming

A work session that uses the system strategy to review an open problem's goal
relevance, evidence, impact, framing, strategy, signal, and priority relative to
other problems. It produces an authorized retain, revise, address, or close
result. The affected problem file retains the authoritative summary and
decision; the working-session record retains material discussion, provenance,
and links to affected files.

### Task candidate

A bounded action that may be considered for execution, such as a task,
research inquiry, experiment, discussion, review, or remediation. A candidate
may be captured before its problem relationship is clear, but that gap must be
resolved before selection.

### Selected task

A task selected under declared authority. It identifies at least one open
problem and implements or tests that problem's strategy. Small execution steps
may inherit that relationship from their containing task rather than repeating
it.

### Working-session record

The durable record of one material invocation of a declared work session. It
identifies the session, participants, affected problems and tasks, material
evidence or decisions, and stopping point. It preserves history and provenance;
problem and task files remain authoritative for current state and resumption.

### Archive

Durable inactive material retained outside the current-state views. Closed
problem files belong under `problems/archive/`; closed, cancelled, rejected,
merged, or superseded task files belong under `tasks/archive/`. Archiving
changes visibility, not provenance or meaning.

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
evidence arrives.

### Closed

An authorized decision that the system will no longer treat a problem as open.
A problem may close because it was solved, disproved, duplicated or replaced,
moved outside the system boundary, lost its goal, or had its remaining risk
explicitly accepted. Closure records the reason, evidence, and authority and
does not imply “solved.”

### Learning

A reusable change in understanding derived from evidence and results. Learning
may revise an open problem, goal, strategy, process, validation method, or other
future operation; an observation is not reusable learning merely because it
was recorded.

### Compiled knowledge

A reusable synthesis derived from evidence, interpretations, decisions, and
learning. It preserves material scope and uncertainty and remains revisable as
new evidence arrives.

### Adaptation

An authority-governed change to future operation based on evidence and
learning. Compilation proposes reusable knowledge; adaptation authorizes and
applies a change to task selection, strategy, process, validation, stream,
artifact, or system structure.
