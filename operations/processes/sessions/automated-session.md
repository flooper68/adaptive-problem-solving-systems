# Automated session

## Purpose

Execute one selected, bounded task autonomously: the agent performs the scoped
work, an independent reviewer agent examines the uncommitted result, and the
maintainer reviews the changes together with the review findings before
delivery. This complements [`brainstorming`](brainstorming.md), which compiles
knowledge through iterative discussion, and [`grooming`](grooming.md), which
decides dispositions; an automated session is for work already scoped well
enough to not need maintainer input during execution.

This session type is an experiment. Retain evidence from its first invocations
in the working-session records so grooming can decide whether to keep, revise,
or remove it.

## Preconditions

- The task exists under `operations/tasks/`, is `open`, and the maintainer
  names it when invoking this session; that invocation is the selection signal
  grooming requires.
- The task states scope, acceptance conditions, and a validation approach
  concrete enough to execute without mid-session maintainer decisions. When it
  does not, stop before executing and route the gap back to
  [`grooming`](grooming.md) or a [`brainstorming`](brainstorming.md) session.
- An automated session does not edit the compiled framework; brainstorming
  remains the only work session that does. Capture framework-worthy lessons as
  compilation task candidates through [`intake.md`](../intake.md).

## Procedure

The session follows [`ai-agent-tasks.md`](../ai-agent-tasks.md); the steps
below specialize it.

1. **Claim.** Record the claim in the task file per
   [`ai-agent-tasks.md`](../ai-agent-tasks.md), naming this session type.
2. **Execute.** Make the scoped changes and run the task's declared validation.
   When a decision only the maintainer can make blocks progress, record an
   explicit handoff in the task and stop rather than guessing.
3. **Agent review.** Launch an independent reviewer agent that did not produce
   the changes. It reviews the uncommitted diff against the task's scope and
   acceptance conditions, checks that this process was followed, and examines
   the validation results. Record its findings in the working-session record.
4. **Revise.** Address confirmed findings and rerun validation; record rejected
   findings with the reason they were rejected. Repeat the agent review when
   revisions were material.
5. **Human review.** Present to the maintainer: the uncommitted changes, the
   reviewer findings with their resolutions, the validation results, and any
   remaining uncertainty. This step is always required — no specialized
   approval signal replaces it — and the maintainer may request revisions,
   which return the session to step 2.
6. **Deliver.** After explicit maintainer approval, stage only the
   session-scoped changes, commit, push, and archive the task per
   [`ai-agent-tasks.md`](../ai-agent-tasks.md).

## Evidence and retention

Retain one working-session record under `streams/working-sessions/` with the
task, the executing agent, the reviewer findings and their resolutions,
validation results, material decisions and deviations, the stopping point, and,
when accepted, the delivered commit. Raw agent transcripts stay in their native
recoverable sources, linked when material.
