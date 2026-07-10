# Working sessions

## Purpose

Use a bounded discussion to explore a topic, elicit knowledge or judgment,
surface uncertainty, and retain a trustworthy source record. A working session
implements APSS's discussion/grilling capability. It produces evidence and may
produce insights, questions, decisions, or candidate actions; it does not
silently turn any of them into backlog commitments.

A session may be synchronous or asynchronous, but it must have a coherent topic
or intended outcome. Routine conversation does not need a durable record unless
it may inform later work, compilation, adaptation, or review.

## Roles and invocation

- A facilitator frames the session, keeps observations distinguishable from
  interpretation, and prepares the retained record.
- Participants contribute knowledge, proposals, questions, and corrections.
- Only a participant with declared authority may turn agreement into an
  approved decision or authorize resulting work.

Invoke a working session when a topic needs collaborative exploration, owner or
expert judgment, a design discussion, brainstorming, or clarification that is
broader than a single feedback report or already-bounded work item.

## Procedure

1. **Frame.** State the topic, purpose, participants, relevant boundary, and
   what a useful stopping point would be.
2. **Orient.** Read or name relevant declarations, evidence, prior sessions,
   feedback, decisions, and work. Record missing context rather than filling it
   with assumptions.
3. **Explore.** Elicit observations, interpretations, alternatives,
   constraints, trade-offs, and desired outcomes. When grilling a participant,
   ask one load-bearing question at a time and adapt the next question to the
   answer.
4. **Distinguish outcomes.** Keep these roles explicit:
   - observations and source claims are evidence;
   - insights are participant or operator interpretations linked to evidence;
   - questions are unresolved uncertainty;
   - decisions require an authority, rationale, and explicit decision act; and
   - candidate actions are possible responses, not commitments.
5. **Close.** Summarize material agreement, disagreement, uncertainty, and the
   stopping point. Give participants a chance to correct the record. Do not
   infer consensus from silence or exploratory language.
6. **Route without conflating.** Keep insights and questions in the session by
   default, extracting a linked record only when it needs an independent
   lifecycle. Route:
   - a consumer's reported experience through
     [`framework-feedback-intake.md`](framework-feedback-intake.md);
   - an independently reusable or assessable interpretation through
     [`insight-intake.md`](insight-intake.md);
   - an authorized material decision to its authoritative artifact or work log;
   - a proposed executable response through
     [`backlog-intake.md`](backlog-intake.md), unless declared authority
     directly selects already-bounded work into the plan or work log;
   - reusable learning through
     [`knowledge-compilation.md`](knowledge-compilation.md); and
   - no further action when retaining the session is sufficient.

## Minimum retained record

Create `operations/streams/working-sessions/YYYY-MM-DD-<short-slug>.md`:

```markdown
---
id: apss.session.<stable-id>
type: working-session
status: draft # draft | retained
recorded: YYYY-MM-DD
participants: [<person, role, or agent>]
source: <recoverable source or description>
related_sessions: []
related_feedback: []
related_insights: []
related_work: []
---

# <Session topic>

## Frame

<Purpose, context, boundary, and intended stopping point.>

## Source boundary

<What source material the record includes or references, and what it excludes.>

## Discussion summary

<Concise account of the material exploration and alternatives.>

## Outcomes

### Observations

### Insights

### Questions

### Decisions

### Candidate actions

## Routing and review

<Where any outcomes were routed, who reviewed the summary, and corrections or
unresolved disagreement.>
```

Omit empty outcome subsections when that improves clarity. Prefer a concise,
topic-focused summary with a recoverable source reference over a full
transcript. Retain a transcript only when exact wording or complete source
replay is materially important. Record only necessary personal information and
reference access-controlled evidence rather than copying sensitive material.

Set `status: retained` after participant review or after recording why review
was unavailable. Later corrections are appended with date and provenance; they
do not rewrite what participants originally said.
