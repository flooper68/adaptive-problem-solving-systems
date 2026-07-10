# Problem grooming

## Purpose

Revisit the Framework Operations System's current open problems so its problem
and task files represent the most relevant evidenced gaps between its goal and
current work. Groom one problem at a time and avoid turning grooming into an
automatic commitment to more work.

## Invocation and authority

Run this process:

- before selecting the next substantial work;
- when material feedback, validation, learning, or completed work changes a
  problem's evidence;
- when a goal, strategy, constraint, or system boundary changes;
- when an open problem has no current strategy or an unclear signal; or
- when the maintainer requests a review.

An operator may gather evidence, facilitate review, and propose updates. The
APSS framework maintainer approves problem reframing, work selection, accepted
risk, and closure.

## Procedure

1. **Frame the session.** Name the current goal, the problem or bounded set of
   problems being reviewed, the trigger, participants, and useful stopping
   point.
2. **Orient.** Read the system strategy and each problem's statement, evidence,
   desired change, strategy, signal, linked work, relevant streams and
   knowledge, and material prior sessions.
3. **Groom one problem at a time.** Ask only the next load-bearing question
   needed to determine:
   - whether the problem still obstructs or threatens a current goal;
   - what evidence now supports or contradicts it;
   - whether the statement describes the gap without embedding a solution;
   - whether the problem strategy follows the system strategy and remains
     supported by evidence;
   - whether the desired change and signal can distinguish activity from
     improvement; and
   - whether its impact and urgency justify work now relative to other open
     problems.
4. **Propose one result.** Choose:
   - **retain** — the framing remains useful, with or without current work;
   - **revise** — update the statement, evidence, desired change, strategy, or
     signal;
   - **address now** — retain or revise it and select linked tasks through the
     normal task-selection authority; or
   - **close** — remove it from the current list and record whether it was
     solved, disproved, replaced, moved out of scope, made irrelevant by a goal
     change, or closed with its remaining risk explicitly accepted.
5. **Update traceability.** Keep concise system-local problem IDs stable while
   the same framing remains recognizable. Update the authoritative file under
   `problems/`, and ensure selected tasks list the problem ID under
   `addresses`. Remove or reconsider orphaned tasks when their problem closes.
6. **Record the result.** Append the material evidence, authorized decision,
   rationale, unresolved question, next trigger, and source reference to the
   problem file's grooming history. Update affected task files with selection,
   execution state, current state, and next step. Link both from the retained
   working-session record. Do not claim improvement or solution without
   evidence against the signal.
7. **Archive inactive state.** On approved closure, record the reason and
   evidence in the problem file, set `status: closed`, and move it under
   `problems/archive/`. Keep candidate or deferred tasks under
   `tasks/backlog/`; move inactive tasks under `tasks/archive/`.

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
