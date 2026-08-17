---
entity:
  identity:
    type: key
    value: APS-R-22
  kind: stream-record
kind: stream-record
value:
  capturedBy:
    agent: null
    type: user
  createdAt: 2026-08-16T19:41:09.314Z
  dispositionNote: "Legacy disposition: groomed"
  groomed: true
  key: APS-R-22
  keyNumber: 22
  labels:
    - repository-import
    - aps-legacy
  originSession: null
  originTask: null
  problem: null
  stream: stream:slug:insights
  updatedAt: 2026-08-16T19:41:34.088Z
---

# Always start simple, add only when needed

## Insight

### Claim

When designing a process or structure, start with the simplest version that
does the job and add distinctions, variants, or machinery only when a real
need demonstrates they are missing.

### Scope

Stated while simplifying Framework Operations — consolidating four per-kind
grooming processes into one — and clarified by the maintainer as a
framework-worthy principle: it should apply to anyone defining systems and
processes with APS, not only to operating this system.

### Reasoning

The maintainer observed that a single grooming process can handle all input
kinds — streams, tasks, problems, verification evidence — and concluded that
simplification is safe because additions remain possible later: "to simplify,
we can always add more later." Starting simple is recoverable; starting
complex imposes its cost immediately and permanently.

## Evidence

### Supporting

- The four grooming processes shared one skeleton (orient, clarify, assess,
  decide, propagate, record) and differed mainly in disposition vocabularies —
  the duplication existed without evidence that any invocation needed it.
- [`STRATEGY.md`](../../../STRATEGY.md) points 2–4 already encode the same
  principle for this system: keep only what one loop needs, add complexity
  only when observed use demonstrates it.
- Prior concept reviews repeatedly reached pruning dispositions (authority,
  goal, boundary, task states), each finding that removed structure was not
  missed.

### Contradictory or limiting

- Asymmetry is not guaranteed: some distinctions are cheap to keep and
  expensive to rediscover after being dropped (the archived processes hedge
  this by keeping the removed vocabularies recoverable).
- None known from observed use yet; the consolidated grooming process has not
  run an invocation.

## Possible implications

- Candidate for compilation into normative framework guidance on defining
  systems and processes; captured as
  [`compile-start-simple-principle`](../../../tasks/archive/compile-start-simple-principle.md)
  for a brainstorming session to execute after grooming.
- Supports future grooming of the operations system itself: prefer removing
  or merging declared structure over elaborating it.

## Open questions

- What observed signal should count as "needed" strongly enough to justify
  adding structure back?

## Intake and clarification record

### 2026-08-06 — captured

Source wording: "always start simple, add only when needed," stated alongside
the request to consolidate grooming ("to simplify, we can always add more
later"). Operator paraphrase in the claim above.

### 2026-08-06 — clarified

Asked whether the claim is an Operations working preference or a
framework-worthy principle; the maintainer answered framework-worthy — it
should eventually be compiled into APS's normative guidance for anyone
defining systems and processes. A compilation task candidate was captured and
linked; compilation still requires grooming of this insight and a
brainstorming session. Further grilling stopped there: the claim, reasoning,
and immediate use were already explicit in the source's own words.

## Grooming record

### 2026-08-07 — act: assessed supported; compilation task ready

- **Participants:** APS framework maintainer, Claude Code operator,
  independent reviewer agent
  ([session](../../working-sessions/2026-08-06-first-cadenced-grooming.md)).
- **Assessment:** **supported.** Strategy points 2–4 already encode the
  principle for this system; seven pruning dispositions found removed
  structure unmissed; the grooming consolidation held. The record's own
  limiting note — that the consolidated grooming process had not run an
  invocation — is cured only by the very invocation recording this entry,
  so the use-evidence is one invocation deep, not long-run.
- **Disposition:** **act** — this assessment clears
  [`apss.compile-start-simple-principle`](../../../tasks/archive/compile-start-simple-principle.md)'s
  open question; the task is recorded ready for a brainstorming session,
  compiling this principle together with
  [[processes-are-compiled-knowledge]].

### 2026-08-07 — compiled into the framework definition

Compiled by the
[start-simple compilation session](../../working-sessions/2026-08-07-start-simple-compilation.md)
into the framework definition's system-creation guidance. The open question —
what observed signal counts as "needed" — is answered in the compiled wording
by the evidence kinds the Operations strategy already names: observed use,
feedback, validation, or a new problem.

---

Repository import provenance: {"sourceCommit":"43b9f6918677ef654578c2276e1c8e4d615fcbf7","sourcePath":"operations/streams/insights/archived/2026-08-06-start-simple-add-only-when-needed.md","legacyId":"apss.insight.start-simple-add-only-when-needed"}

---

[repository-import:stream-record:apss.insight.start-simple-add-only-when-needed@43b9f6918677ef654578c2276e1c8e4d615fcbf7:operations/streams/insights/archived/2026-08-06-start-simple-add-only-when-needed.md]
