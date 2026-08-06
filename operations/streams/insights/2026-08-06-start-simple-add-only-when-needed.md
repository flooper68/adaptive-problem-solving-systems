---
id: apss.insight.start-simple-add-only-when-needed
type: insight
status: captured
captured: 2026-08-06
source: APS framework maintainer
source_records:
  - ../working-sessions/2026-08-06-grooming-consolidation.md
related_insights: []
related_work:
  - ../../tasks/compile-start-simple-principle.md
compiled_into: []
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
- [`STRATEGY.md`](../../STRATEGY.md) points 2–4 already encode the same
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
  [`compile-start-simple-principle`](../../tasks/compile-start-simple-principle.md)
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

Not yet groomed. See
[`grooming.md`](../../processes/sessions/grooming.md).
