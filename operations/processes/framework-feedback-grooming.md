# Framework feedback grooming

## Purpose

Interpret a framework-feedback report, assess what it establishes, and record
an explicit response. Grooming preserves the report as evidence while deciding
whether it warrants work, more observation, or no action.

Feedback grooming is distinct from task grooming. It evaluates an observed
experience; if a change or investigation is warranted, it creates a linked
task candidate whose scope and priority are decided separately.

## Invocation and roles

Groom a report when the maintainer requests it, when related reports
accumulate, when the feedback blocks a consumer, or when planning needs usage
evidence.

- An operator facilitates, seeks clarification when proportionate, and records
  the analysis.
- The reporter supplies context when available but need not design the fix.
- The APS framework maintainer approves the disposition and any escalation.

Set `status: grooming` while analysis is materially underway. Do not edit the
original report to match the conclusion; append clarifications and the
grooming record with provenance.

## Procedure

1. **Orient.** Read the report, referenced evidence, related feedback, current
   framework and supporting artifacts, current work, and relevant knowledge.
2. **Clarify the experience.** Ask what the reporter attempted, where the
   framework helped or failed, what they expected, and what effect the gap had.
   Record unavailable context instead of inventing it.
3. **Separate evidence from response.** State the observed experience, the
   underlying consumer need, and the reporter's suggested response separately.
   A suggested implementation is evidence about expectations, not a settled
   requirement.
4. **Classify the scope.** Identify whether the report concerns normative
   semantics, documentation, supporting tooling or examples, stewardship, or
   something outside APS's boundary.
5. **Check identity and reach.** Link duplicates and related reports without
   deleting independent observations. Note whether the issue is reproducible,
   isolated, recurring, or not yet known.
6. **Assess impact and confidence.** Record who is affected, severity, any
   workaround, supporting and contradictory evidence, assumptions, and what
   remains uncertain.
7. **Choose a disposition.** Apply one status below and record the rationale.
8. **Propagate without conflating.** For `actionable` feedback about a gap
   already represented by an open problem, link that problem and create or link
   a task using [`task-intake.md`](task-intake.md) when a bounded response is
   useful. When the report reveals an unrepresented higher-level gap, propose
   it to [`problem grooming`](problem-grooming.md); feedback grooming does not
   open the problem itself. Link both directions. Problem creation, task
   selection, and prioritization remain separate. Feed stable lessons or
   outcome evidence into validation and knowledge compilation.
9. **Close the loop.** Record what acknowledgment or follow-up is owed. If
   linked work is later validated, append the result and set the feedback to
   `addressed`; do not erase the original experience.

## Grooming questions

- What was the consumer trying to accomplish?
- What observable experience or result is actually reported?
- Is the problem in APS, its explanation, its supporting artifacts, or its
  local implementation?
- What consumer outcome is impaired or improved?
- Does the repository already promise or describe the missing behavior?
- Is there a workaround, and what does it cost?
- Is the report independently reproducible or corroborated?
- What part is observation, inference, preference, or proposed solution?
- What is the smallest useful investigation or response?
- What evidence would show that a response addressed the feedback?

## Dispositions and states

- `received` — captured but not yet groomed.
- `grooming` — analysis is materially underway.
- `needs-information` — a load-bearing gap prevents a responsible disposition;
  record the needed evidence and follow-up trigger.
- `actionable` — the evidence justifies a change or bounded investigation;
  link a captured or existing task. This is not a priority commitment.
- `monitoring` — plausible and retained, but more occurrences or outcome
  evidence are needed; record a reconsideration trigger.
- `declined` — no response is warranted or the request is outside the system's
  boundary; preserve the rationale.
- `duplicate` — another report represents the same source experience; link the
  canonical report. Independent corroborating experiences are not duplicates.
- `addressed` — a response has been delivered and outcome evidence indicates
  that it addressed the reported need; link the validation evidence.

## Required grooming record

Replace “Not yet groomed” with a dated entry containing:

- participants and evidence consulted;
- clarified experience, underlying need, and proposed response;
- scope classification, reach, impact, workaround, and confidence;
- facts, assumptions, disagreements, and unresolved questions;
- approved disposition and rationale;
- linked feedback, work item, validation evidence, or reconsideration trigger;
  and
- reporter follow-up or acknowledgment status.
