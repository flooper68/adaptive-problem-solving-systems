# AI agent tasks

Use this process when an AI agent performs repository work.

1. **Claim.** Record the task, open problem it addresses, how it implements or
   tests that problem's strategy, scope, agent, and acceptance condition in the
   task file and set its status to `in-progress`.
2. **Do.** Make the scoped changes and run relevant validation.
3. **Record.** Update the task's current state and next step. Retain material
   work, validation, and uncertainty in the working-session record.
4. **Human review.** Present the uncommitted changes for review. Set the status
   to `awaiting-review` and make any requested revisions.
5. **Deliver.** After explicit human approval, stage the scoped changes, commit,
   push, and report the branch and commit. Set the status to `closed` and
   archive the task with its delivery reference and final reason.

An agent must not commit or push before human approval, must not call the task
complete before the approved commit is pushed, and must leave an explicit
handoff in the task if claimed work cannot be completed.

A specialized process may define an explicit, bounded approval signal so the
agent does not ask for redundant delivery confirmation. For example,
[`insight intake`](insight-intake.md) treats maintainer-requested capture plus
participation through its clarification or review stopping point as approval to
commit and push that insight record. Such a signal applies only to the artifact
and delivery scope named by the specialized process; it does not approve
unrelated changes or later normative adoption.

[`Brainstorming`](brainstorming.md) treats the maintainer's acceptance of its
reviewed result or explicit request to finish or end the session as approval to
commit the bounded session changes and transmit them to the already configured
`origin/main` without a separate delivery confirmation. An unresolved question,
pause, silence, or request to review the diff is not that signal. Required risk
disclosure still applies, but one explicit approval after disclosure is enough
to proceed.
