# Problem grooming

## Purpose

Review proposed, open, and closed Framework Operations problems so the current
problem set represents the most relevant evidenced decomposition of the system
problem. Source-specific grooming proposes higher-level gaps; problem grooming
alone decides whether they become problems. Groom one problem at a time and
avoid turning grooming into an automatic commitment to more work. An `address
now` decision prioritizes the problem; the separate task-grooming responsibility
still shapes candidate work and establishes readiness before selection.

## Invocation and authority

Run this process:

- before selecting the next substantial work;
- when source-specific grooming proposes a new higher-level problem;
- when material feedback, validation, learning, or completed work changes a
  problem's evidence;
- when a parent problem, strategy, material condition, or system boundary changes;
- when an open problem has no current strategy or an unclear signal;
- when new evidence may justify reopening a closed problem; or
- when the maintainer requests a review.

An operator may gather evidence, facilitate review, and propose updates. The
APS framework maintainer approves problem reframing, work selection, accepted
risk, and closure.

## Strategy scope

Keep strategy changes at the smallest level supported by their evidence:

- The **system strategy** states the approach to the root system problem and
  guides problem discovery, decomposition, comparison, and selection across the
  system. Change it only when the system's overall approach should change.
- A **problem strategy** states how the system will resolve or reduce one open
  problem. Put problem-specific decomposition, task sequencing, experiments,
  and validation there.

Before editing the system strategy, name which other current or future problems
the proposed change should guide. If the answer is only the problem being
groomed, update that problem's strategy instead. Do not generalize a useful
method from one problem without evidence that it belongs at system scope.

## Procedure

1. **Frame the session.** Name the root problem context, the proposal, problem,
   or bounded set being reviewed, the trigger, participants, and useful
   stopping point.
2. **Orient.** Read the system strategy, source-grooming proposals and their
   evidence, and each relevant problem's statement, desired change, strategy,
   signal, linked work, streams, knowledge, and material prior sessions.
3. **Groom one problem at a time.** Ask only the next load-bearing question
   needed to determine:
   - for a proposal, whether it states an evidenced higher-level condition
     rather than merely repeating an observation, insight, question, or task;
   - whether the proposed or existing problem is relevant to the system problem
     and distinct from current problems;
   - whether the problem still represents a useful decomposition of its parent;
   - what evidence now supports or contradicts it;
   - whether the statement describes the gap without embedding a solution;
   - whether the problem strategy follows the system strategy and remains
     supported by evidence;
   - whether proposed strategy changes are scoped to this problem or genuinely
     change the system's root-problem approach;
   - whether the desired change and signal can distinguish activity from
     improvement; and
   - whether its impact and urgency justify work now relative to other open
     problems.
4. **Propose one result.** Choose:
   - **open** — create a new problem when the proposal is evidenced, relevant to
     the system problem, distinct from current problems, and worth tracking;
   - **merge proposal** — use the evidence to revise an existing problem rather
     than create a duplicate;
   - **defer or reject proposal** — leave the proposal in its source with the
     reason and reconsideration trigger when applicable;
   - **retain** — the framing remains useful, with or without current work;
   - **revise** — update the statement, evidence, desired change, strategy, or
     signal;
   - **address now** — retain or revise it and select linked tasks through the
     normal task-selection authority; or
   - **reopen** — return a closed problem to the active hierarchy when new
     evidence challenges its closure; or
   - **close** — remove it from the current list and record whether it was
     solved, disproved, replaced, moved out of scope, made irrelevant by a
     parent-problem change, or closed with its remaining risk explicitly accepted.
5. **Update traceability.** Keep concise system-local problem IDs stable while
   the same framing remains recognizable. Update the authoritative file under
   `problems/`, and ensure selected tasks list the problem ID under
   `addresses`. On reopening, set `status: open` and move the problem from
   `problems/archive/` to `problems/`. Remove or reconsider orphaned tasks when
   their problem closes.
6. **Record the result.** Append the material evidence, authorized decision,
   rationale, unresolved question, next trigger, and source reference to the
   problem file's grooming history. Update affected task files with selection,
   execution state, current state, and next step. Link both from the retained
   working-session record. Do not claim improvement or solution without
   evidence against the signal.
7. **Archive inactive problem state.** On approved closure, record the reason
   and evidence in the problem file, set `status: closed`, and move it under
   `problems/archive/`. Keep every current task directly under `tasks/` without
   a backlog subdivision; move inactive tasks under `tasks/archive/`.

## Completion

A grooming session is complete when every problem in scope has an approved
result, its problem and task files reflect it, selected work remains traceable,
and any missing answer has a clear evidence request or next trigger.
The session can stop between problems without forcing a batch decision.

## Evidence and retention

- The affected problem file is authoritative for the grooming summary, material
  evidence considered, approved decision, rationale, and resulting framing.
- The working-session record preserves participants, discussion, material
  evidence, affected files, and the stopping point.
- Raw transcript, feedback, or research remains in its native recoverable
  source and is linked from the session or problem file when material.
- The problem file owns current problem state; the task file owns current
  execution state and the next step. Do not reconstruct either from session
  history.
