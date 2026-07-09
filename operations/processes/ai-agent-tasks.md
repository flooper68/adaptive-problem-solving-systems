# AI agent tasks

Use this process when an AI agent performs repository work.

1. **Claim.** Record the task, scope, agent, and acceptance condition in the
   current plan or work log. Set its status to `claimed`.
2. **Do.** Make the scoped changes and run relevant validation.
3. **Record.** Add a concise work-log entry describing what changed, validation
   results, uncertainty, and unfinished work.
4. **Human review.** Present the uncommitted changes for review. Set the status
   to `awaiting review` and make any requested revisions.
5. **Deliver.** After explicit human approval, stage the scoped changes, commit,
   push, and report the branch and commit. Set the status to `pushed`.

An agent must not commit or push before human approval, must not call the task
complete before the approved commit is pushed, and must leave an explicit
handoff in the log if claimed work cannot be completed.
