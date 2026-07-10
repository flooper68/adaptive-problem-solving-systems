# Insight intake

## Purpose

Preserve a potentially useful interpretation with its source, reasoning, scope,
and uncertainty before assessing whether it is supported or deciding what it
should influence. An insight is not a feedback report, established knowledge,
approved decision, or executable work merely because it was captured.

## When to capture

Create an independent insight record when a participant or operator draws a
coherent conclusion from evidence and that interpretation may need later
corroboration, challenge, compilation, comparison, or reuse beyond its source
record. Keep a passing interpretation inside its working session or other
source when it does not need an independent lifecycle.

Use one record for one coherent claim. Related claims may link to each other,
but do not combine materially different interpretations only to reduce file
count. Search existing insights first and add new evidence or a related record
without erasing independent provenance.

## Minimum capture

Create `operations/streams/insights/YYYY-MM-DD-<short-slug>.md`:

```markdown
---
id: apss.insight.<stable-id>
type: insight
status: captured
captured: YYYY-MM-DD
source: <person, role, agent, or source description>
source_records: []
related_insights: []
related_work: []
compiled_into: []
---

# <Concise insight statement>

## Insight

### Claim

<The interpretation being proposed.>

### Scope

<Where, for whom, or under what conditions the claim may apply.>

### Reasoning

<How the source moved from observations or source claims to this inference.>

## Evidence

### Supporting

<Recoverable observations or sources that support the inference.>

### Contradictory or limiting

<Known counterevidence, alternative explanations, limits, or “none known”.>

## Possible implications

<What understanding, decision, compilation question, or possible response this
might affect without implying commitment.>

## Open questions

- <What remains uncertain or would materially change confidence?>

## Intake and clarification record

### YYYY-MM-DD — captured

<Source wording, operator paraphrase, clarification, and provenance.>

## Grooming record

Not yet groomed. See
[`insight-grooming.md`](../../processes/insight-grooming.md).
```

Record direct observations, external claims, participant interpretations, and
operator interpretations separately. An operator may make the claim concise,
but must not materially change the source's meaning. Give the source an
opportunity to correct the record when available; otherwise record that review
was unavailable.

## Adaptive clarification grill

Preserve the initial claim before clarification. Then select two to four
questions proportionate to its ambiguity and likely use. Ask one load-bearing
question at a time, wait for the answer, and adapt the next question. Do not
repeat information the source has already supplied.

Useful questions include:

- What observation or source prompted this conclusion?
- What exactly do you think follows from that evidence, and why?
- In what context does the claim apply, and where might it not apply?
- What alternative explanation or contradictory evidence should be retained?
- What evidence would materially increase or reduce confidence?
- Which understanding, decision, or possible action could this insight inform?

Accept uncertainty and disagreement. Do not steer the source toward a preferred
response or require grooming-level proof merely to preserve an interpretation.
If clarification stops, record the next unanswered question and why it remains
open.

Update the claim, scope, reasoning, evidence, implications, open questions, and
intake record with the answers. Distinguish source corrections from operator
analysis and show the resulting record to the source for correction when
practical.

## Capture result

A captured insight has a stable ID, recoverable source, explicit claim and
scope, visible inference, supporting and limiting evidence, and unresolved
questions. `status: captured` means only that the interpretation is preserved;
it does not establish truth, priority, normative status, or authorization.

The next possible action is
[`insight grooming`](insight-grooming.md). If an executable response is
proposed, capture it separately through [`backlog-intake.md`](backlog-intake.md)
and link both records.
