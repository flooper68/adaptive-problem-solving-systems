---
entity:
  identity:
    type: slug
    value: key-aps-s-5-record
  kind: session-record
kind: session-record
value:
  endedAt: 2026-08-06T23:59:59.999Z
  outcome: completed
  session: session:key:APS-S-5
---

# Define automated session types and group session processes

## Frame

The maintainer proposed a new work-session type — an automated session — in
which an agent handles a selected task on its own, runs a subagent as an
independent reviewer, and then presents the result for human review before
delivery. During the session the maintainer extended the scope twice: move all
session-type processes under a `processes/sessions/` subfolder so declared
session types are visible at a glance, and define automatic grooming in the
same autonomous-execute, agent-review, human-approve fashion. The maintainer
framed both automated types as an experiment that may not be kept.

## Orientation

- [`ai-agent-tasks.md`](../../processes/ai-agent-tasks.md) already defines the
  spine the automated types need: claim in the task file, do the scoped work,
  record state, present uncommitted changes for human review, and deliver only
  after explicit approval. Both new processes are thin specializations of it.
- [`brainstorming.md`](../../processes/sessions/brainstorming.md) declares
  itself the only work session that edits the compiled framework, and
  [`grooming.md`](../../processes/sessions/grooming.md) reserves every
  disposition approval and task selection to the maintainer. Both invariants
  are preserved: the automated session refuses framework edits, and automatic
  grooming only proposes dispositions.
- The session ran while the intake-consolidation changes (single `intake.md`)
  were concurrently uncommitted in the working tree; the new processes
  reference the consolidated `intake.md`.

## Decisions

1. **Automated session type.** An initial draft was compiled, then reverted at
   the maintainer's request and retained here as a draft; after extending the
   scope the maintainer's "let's also define" plus the experiment framing was
   taken as direction to compile both types as uncommitted changes for review.
   The adopted design is the compiled
   [`automated-session.md`](../../processes/sessions/automated-session.md):
   maintainer invocation with a named task is the selection signal; the task
   must be concrete enough to execute without mid-session maintainer
   decisions, otherwise the session stops and routes back; an independent
   reviewer agent examines the uncommitted diff before the maintainer sees it;
   human review is always required with no specialized approval shortcut; no
   compiled-framework edits.
2. **Automatic grooming type.** Compiled as
   [`automatic-grooming.md`](../../processes/sessions/automatic-grooming.md):
   the agent runs grooming's orient–clarify–assess steps autonomously and
   drafts one proposed disposition per item, recording open questions instead
   of assuming answers and defaulting to `keep` with an evidence request when
   a missing answer could reverse the disposition; an independent reviewer
   agent checks the proposals; the maintainer approves, adjusts, or rejects
   each disposition; per-item approvals are the delivery signal for exactly
   the recorded entries.
3. **Session processes grouped.** `brainstorming.md` and `grooming.md` moved
   with history to `operations/processes/sessions/`, joined by the two new
   processes. Live pointers updated: `SYSTEM.md`, `AGENTS.md`
   (`CLAUDE.md` is its symlink), the processes README and cross-links in
   `process.md`, `ai-agent-tasks.md`, `knowledge-compilation.md`, and
   `intake.md` (including its record templates), stream READMEs, the "Not yet
   groomed" pointers in ungroomed stream records, and live links in the open
   tasks `general-evidence-processes.md` and `task-candidate-grilling.md`.
   Following the grooming-consolidation precedent, in-body links in retained
   historical records were left as written; git history resolves them. The
   compiled framework was left unchanged — its `processes/brainstorming.md`
   snippet is an illustrative example, and the framework does not mandate a
   folder layout.
4. **Experiment status.** Both new processes carry an explicit experiment
   note: evidence from their first invocations is retained in working-session
   records so grooming can decide whether to keep, revise, or remove them.

## Open questions

- Whether the reviewer stage should be parameterizable per task (the task
  declaring review focus) or stay uniform; uniform was chosen per the
  start-simple strategy until observed use shows need.
- Whether the four-disposition grooming set remains expressive enough when
  proposals are drafted autonomously; the first automatic-grooming
  invocations are the reconsideration trigger.

## Changes

- [`processes/sessions/`](../../processes/sessions/) — new subfolder holding
  all work-session processes.
- [`automated-session.md`](../../processes/sessions/automated-session.md),
  [`automatic-grooming.md`](../../processes/sessions/automatic-grooming.md) —
  new experimental session processes.
- [`SYSTEM.md`](../../SYSTEM.md) — `work_sessions` gained `automated` and
  `automatic-grooming` entries marked experimental; all session process paths
  now point into `processes/sessions/`.
- [`processes/README.md`](../../processes/README.md) — notes the `sessions/`
  convention and indexes the two new processes.
- Live pointer updates enumerated in decision 3.

## Acceptance and delivery

The maintainer reviewed the compiled scope and accepted it with an explicit
request to finish the session and ship it; per the brainstorming process that
acceptance approves delivery to `origin/main`. The concurrent
intake-consolidation scope was delivered separately by its own session during
this one, so this delivery contains only this session's changes. The
still-uncommitted `review-authority.md` archive update remains excluded, as in
prior deliveries. Delivered as commit 30462aa; this delivery reference was
recorded in a follow-up commit per the established pattern.

---

Legacy participants: APS framework maintainer, Claude Code operator

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/working-sessions/2026-08-06-automated-session-type.md","legacyId":"apss.session.automated-session-type"}

---

[repository-import:session:apss.session.automated-session-type@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/working-sessions/2026-08-06-automated-session-type.md]
