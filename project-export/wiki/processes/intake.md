# Intake

## Purpose

Preserve a potentially useful input faithfully before assessing it. One
process captures every input kind: a consumer's experience of APS (framework
feedback), an interpretation drawn from evidence (insight), and a proposed
executable response (task candidate). Intake preserves the record, its source,
and its provenance; [`grooming`](sessions/grooming.md) decides what it becomes. A
captured record is not established knowledge, an approved decision, or
committed work merely because it was captured, and it must not be rewritten to
fit a proposed solution.

## When to capture

- **Framework feedback** — someone reports that APS is unclear, incomplete,
  incorrect, burdensome, difficult to apply, or missing a capability, or
  describes a useful outcome worth preserving. One report per source
  experience; similar reports from different people or applications remain
  separate, linkable evidence.
- **Insight** — a participant or operator draws a coherent conclusion from
  evidence and the interpretation may need later corroboration, challenge,
  compilation, or reuse beyond its source record. One record per coherent
  claim; keep a passing interpretation inside its source when it needs no
  independent lifecycle.
- **Task candidate** — a bounded inquiry, experiment, review, remediation, or
  other action may improve the framework, Framework Operations, or a future
  application and is not already represented. A report, observation, insight,
  question, or decision stays in its source record; a warranted response
  becomes a separate linked task candidate.

Search the existing records first. Link new evidence to an existing record
instead of creating a duplicate, without erasing independent provenance.

## Announcement

When an agent identifies that a conversation is intake, it says so before
extracting, naming the kind and linking this process, so the source can see
how their input will be preserved, clarified, and delivered. In a chat
interface, use that interface's clickable repository-file form for
`operations/processes/intake.md`. The announcement is orientation, not a
request for permission when the source already asked for the capture. If a
conversation running under another process produces an independently useful
input, announce the transition before extracting it.

## Minimum capture

**Framework feedback** — create
`operations/streams/framework-feedback/YYYY-MM-DD-<short-slug>.md`:

```markdown
---
id: apss.feedback.<stable-id>
type: framework-feedback
status: received
received: YYYY-MM-DD
reporter: <person, role, or anonymous>
source: <recoverable source or description>
related_feedback: []
related_work: []
---

# <Concise description of the feedback>

## Report

### Context
### Observed problem or outcome
### Desired outcome
### Suggested response
### Evidence

## Grooming record

Not yet groomed. See [`grooming.md`](../../processes/sessions/grooming.md).
```

Keep the observed experience, desired outcome, and suggested response
distinct — a proposed solution is evidence about expectations, not a settled
requirement. Record only the personal information needed to follow up, and
reference access-controlled native evidence rather than copying it.

**Insight** — create
`operations/streams/insights/YYYY-MM-DD-<short-slug>.md`:

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
### Scope
### Reasoning

## Evidence

### Supporting
### Contradictory or limiting

## Possible implications

## Open questions

## Intake and clarification record

### YYYY-MM-DD — captured

## Grooming record

Not yet groomed. See [`grooming.md`](../../processes/sessions/grooming.md).
```

Record direct observations, external claims, participant interpretations, and
operator interpretations separately. An operator may make the claim concise
but must not materially change the source's meaning.

**Task candidate** — create `operations/tasks/<short-slug>.md`:

```markdown
---
id: apss.<stable-id>
type: task
status: open
owner: APS framework maintainer
created: YYYY-MM-DD
source: <person, observation, document, validation, or other origin>
source_records: []
---

# <Concise action-oriented title>

## Proposed action
## Intended result
## Motivation
## Evidence
## Open questions

## Grooming log

### YYYY-MM-DD — captured
```

Use the closest executable type (`task`, `research`, `experiment`, `review`,
`remediation`). Capture must not invent evidence, imply approval, or rewrite
the source record as a settled response.

## Clarification

Preserve the initial statement before clarifying. Then select two to four
questions proportionate to the input's ambiguity and likely use. Ask one
load-bearing question at a time, wait for the answer, and adapt the next
question; never present a batch. Do not repeat what the source already
supplied, do not steer toward a preferred response, and do not demand
grooming-level proof merely to preserve an input. Useful directions:

- What was observed or attempted, and what prompted this?
- What exactly follows from that evidence, and why?
- Where does it apply, and where might it not?
- What would a better outcome look like, and for whom?
- What alternative explanation or contradictory evidence should be retained?
- Which understanding, decision, or possible action could this inform?

Accept "unknown" as useful information. If clarification stops, record the
next unanswered question and why it remains open. Update the record with the
answers, keep source words distinct from operator inference, and show the
result to the source for correction when practical.

## Capture result

A captured record has a stable ID, a recoverable source, content another
operator can understand, its clarification recorded or the pending reason
noted, and the correct initial status (`received`, `captured`, or `open`). It
carries no promise of priority, adoption, or implementation. The next possible
action is [`grooming`](sessions/grooming.md). If the input reveals an urgent safety,
security, legal, or data-loss concern, escalate to the maintainer immediately
rather than waiting.

## Delivery

For insight and feedback records, delivery is an automatic step of this
process, not a separate decision. Once the minimum capture is complete, the
clarification has reached a useful stopping point, and source corrections have
been incorporated or their unavailability recorded, the agent immediately
delivers: stage only the captured record, necessary source-link corrections,
and any task candidate captured and linked during the same intake; commit;
push the current branch; and report the branch and commit. Do not pause to ask
whether to deliver, and do not leave a completed capture only in a working
tree. A task candidate captured on its own follows the normal session review
and delivery instead.

When the APS framework maintainer asked for the capture and participated
through the clarification stopping point or reviewed the result, that
participation is the approval making automatic delivery valid — the
specialized approval signal permitted by
[`ai-agent-tasks.md`](ai-agent-tasks.md). It approves faithful capture and
delivery, not the input's truth, priority, disposition, or adoption. When the
current branch is `main`, it explicitly includes pushing the bounded intake
commit directly to `origin/main` without a delivery branch or separate
confirmation. Repository protections, failed validation, non-fast-forward
state, or inability to isolate the bounded changes remain blockers and must
not be bypassed. If the source is not authorized to approve repository
delivery, review was unavailable, or the push fails, preserve the record,
state the blocker, and follow the human-review and handoff rules in
[`ai-agent-tasks.md`](ai-agent-tasks.md).
