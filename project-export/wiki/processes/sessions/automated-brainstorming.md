# Automated brainstorming

## Purpose

Run a brainstorming session autonomously. The agent takes one maintainer-named
task or topic, performs the work end to end — including any decision or edit
the maintainer could make in an interactive
[`brainstorming`](brainstorming.md) session — an independent reviewer agent
examines the uncommitted result, and the maintainer reviews the changes
together with the recorded decisions and review findings before delivery.
There are no preconditions on what the session may take on: it may edit the
compiled framework, choose dispositions, and revise operational surfaces,
exactly as brainstorming can.

This session type is an experiment. Retain evidence from its first invocations
in the working-session records so grooming can decide whether to keep, revise,
or remove it.

## Procedure

The session follows [`brainstorming.md`](brainstorming.md) with the
maintainer's interactive role deferred to review, and
[`ai-agent-tasks.md`](../ai-agent-tasks.md) for claim and delivery conduct.

1. **Claim.** The maintainer's invocation naming a task or topic is the
   selection signal. When a task file exists, record the claim in it per
   [`ai-agent-tasks.md`](../ai-agent-tasks.md), naming this session type.
2. **Execute.** Work through brainstorming's frame, orient, explore,
   distinguish, challenge, and compile steps autonomously. Where brainstorming
   would put a question or decision to the maintainer, the agent decides and
   keeps going, recording each material decision with its rationale and the
   strongest case against it. Compile the conclusions as uncommitted changes,
   following [`knowledge-compilation.md`](../knowledge-compilation.md) for
   framework knowledge, and run relevant validation.
3. **Agent review.** Launch an independent reviewer agent that did not produce
   the changes. It reviews the uncommitted diff against the session's frame,
   challenges the recorded decisions, checks that this process was followed,
   and examines the validation results. Record its findings in the
   working-session record.
4. **Revise.** Address confirmed findings and rerun validation; record rejected
   findings with the reason they were rejected. Repeat the agent review when
   revisions were material.
5. **Human review.** Present to the maintainer: the uncommitted changes, the
   decisions taken on the maintainer's behalf — most prominently the ones the
   maintainer might plausibly reverse — the reviewer findings with their
   resolutions, the validation results, and any remaining uncertainty. This
   step is always required — no specialized approval signal replaces it. Until
   approval, every decision the session took is a proposal; the maintainer may
   reverse any of them, which returns the session to step 2.
6. **Deliver.** After explicit maintainer approval, stage only the
   session-scoped changes, commit, push, and archive the task per
   [`ai-agent-tasks.md`](../ai-agent-tasks.md).

## Evidence and retention

Retain one working-session record under `streams/working-sessions/` with the
task or topic, the executing agent, the decisions taken autonomously with
their rationale, the reviewer findings and their resolutions, validation
results, the stopping point, and, when accepted, the delivered commit. Raw
agent transcripts stay in their native recoverable sources, linked when
material.
