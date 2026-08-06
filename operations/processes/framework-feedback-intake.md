# Framework feedback intake

## Purpose

Preserve a consumer's experience of APS as evidence before deciding whether
the framework or its supporting artifacts should change. A feedback report is
not a task commitment and must not be rewritten to fit a proposed solution.

## When to capture

Capture feedback when someone reports that APS is unclear, incomplete,
incorrect, burdensome, difficult to apply, or missing a capability, or when
they describe a useful outcome that should be preserved. Reports may concern
the normative framework, supporting tools and examples, or the stewardship
experience.

Use one report for one source experience. Similar reports from different
people or applications remain separate evidence and may link to each other.
Add clarification from the same conversation to the original report with its
date and source.

## Minimum capture

Create `operations/streams/framework-feedback/YYYY-MM-DD-<short-slug>.md`:

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

<What the reporter was trying to do and relevant operating conditions.>

### Observed problem or outcome

<What happened, in the reporter's terms.>

### Desired outcome

<What would have made the experience successful, if known.>

### Suggested response

<Any proposed solution, kept distinct from the observed need.>

### Evidence

<Examples, files, screenshots, results, or “report only; not independently
validated.”>

## Grooming record

Not yet groomed. See
[`framework-feedback-grooming.md`](framework-feedback-grooming.md).
```

Record only the personal information needed to understand and follow up on the
feedback. Reference access-controlled native evidence rather than copying
sensitive material into the repository.

## Capture result

A captured report has a stable ID, provenance, enough context to interpret the
experience, and `status: received`. Acknowledge what was heard without
promising prioritization or accepting the reporter's proposed response as the
only solution.

The next possible action is
[`framework feedback grooming`](framework-feedback-grooming.md). If the report
reveals an urgent safety, security, legal, or data-loss concern, escalate it to
the maintainer immediately rather than waiting for routine grooming.

## Delivery

Delivery is an automatic step of this process, not a separate decision. Once
the minimum capture is complete and any clarification from the same
conversation has been recorded, all information is gathered and the agent must
immediately deliver: stage only the feedback report and necessary source-link
corrections, commit, push the current branch, and report the branch and
commit. Do not pause to ask whether to deliver, and do not leave a completed
report only in an agent's working tree.

When the APS framework maintainer asked for the feedback to be captured and
participated through the capture or reviewed the result, that participation is
the approval that makes this automatic delivery valid. This is the specialized
approval signal permitted by [`ai-agent-tasks.md`](ai-agent-tasks.md); it
approves faithful capture and delivery, not the report's validity, priority,
disposition, or any proposed response.

When the current branch is `main`, this approval explicitly includes pushing
the bounded feedback commit directly to `origin/main`. The agent should not
create a delivery branch or request separate confirmation solely because
`main` is the repository's default or shared branch. Repository protections,
failed validation, non-fast-forward state, or inability to isolate the bounded
changes remain blockers and must not be bypassed.

If the reporter is not authorized to approve repository delivery, review was
unavailable, unrelated working-tree changes cannot be safely excluded, or the
push fails, do not infer approval or broaden the commit. Preserve the record,
state the blocker, and follow the normal human-review and handoff rules in
[`ai-agent-tasks.md`](ai-agent-tasks.md).
