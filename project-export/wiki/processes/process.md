# Framework Operations process

Chaos House is the canonical system of record for APS Framework Operations. The configured R54 repository projection is a one-way backup: it never supplies approval, never writes back into Chaos House, and never substitutes for session, task, problem, record, or wiki history.

## Operating loop

1. Orient from `current-state.html`, the open problem tree, structured signal readings, the selected task, relevant streams, and the canonical `framework/` knowledge package.
2. Groom when requested or triggered. After every third completed working session since the last grooming invocation, run grooming over accumulated records, task candidates, problem state, and next-work selection.
3. Select one bounded task that serves an open problem strategy, or state explicitly that it has no problem.
4. Start the session before the work. A task carries its declared session type; when the maintainer asks to work without naming a task, infer the session type from their message (`list_session_types`) or ask in plain text, and start it before any action that reads as work. Announce the session key and type as the first thing you say after starting. Bind every supported action to that session and preserve material evidence and decisions in its transcript. When the maintainer corrects how the session is being run (not what it decides), add one `session_note` starting with `process:` that says what was corrected and at which step.
5. Execute the declared process. Draft proposed compiled-knowledge changes outside the authoritative wiki until the required human approval is present.
6. Run `verification.md`. Record the addressed problem's signal reading honestly; artifact correctness does not prove problem improvement.
7. When evidence changes reusable APS knowledge, follow `knowledge-compilation.md` and `framework-adaptation.md`. Accepted knowledge is written once to its canonical `framework/` page through session-bound wiki actions and summarized in `framework/CHANGELOG.md`. When evidence concerns how a process performs, follow `sessions/retrospective.md`; a process page changes only through a retrospective or a brainstorming session, and every process edit records the effect it is expected to have by the next retrospective.
8. Refresh affected current-state views, task state, problem history, and session record. When the work seems finished, ask the maintainer explicitly whether to close the session now or continue; close with `end_session` and its record only on their go. Close only a session your own `start_session` returned in this conversation — an open session you did not start is another conversation's work in flight; `session_note` on it if it concerns you and leave it open.
9. Let repository backup converge asynchronously. A failed or pending backup is an operational durability condition to surface, not authority to rewrite or roll back accepted domain state.

The loop has adapted only when evidence changes a later task, problem strategy, process, verification rule, stream, or compiled framework page and the changed operation produces new evidence.
