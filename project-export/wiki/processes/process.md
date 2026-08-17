# Framework Operations process

Chaos House is the canonical system of record for APS Framework Operations. The configured R54 repository projection is a one-way backup: it never supplies approval, never writes back into Chaos House, and never substitutes for session, task, problem, record, or wiki history.

## Operating loop

1. Orient from `current-state.html`, the open problem tree, structured signal readings, the selected task, relevant streams, and the canonical `framework/` knowledge package.
2. Groom when requested or triggered. After every third completed working session since the last grooming invocation, run grooming over accumulated records, task candidates, problem state, and next-work selection.
3. Select one bounded task that serves an open problem strategy, or state explicitly that it has no problem.
4. Start the task's declared session type before work. Bind every supported action to that session and preserve material evidence and decisions in its transcript.
5. Execute the declared process. Draft proposed compiled-knowledge changes outside the authoritative wiki until the required human approval is present.
6. Run `verification.md`. Record the addressed problem's signal reading honestly; artifact correctness does not prove problem improvement.
7. When evidence changes reusable APS knowledge, follow `knowledge-compilation.md` and `framework-adaptation.md`. Accepted knowledge is written once to its canonical `framework/` page through session-bound wiki actions and summarized in `framework/CHANGELOG.md`.
8. Refresh affected current-state views, task state, problem history, and session record. Close only on the owner's explicit go.
9. Let repository backup converge asynchronously. A failed or pending backup is an operational durability condition to surface, not authority to rewrite or roll back accepted domain state.

The loop has adapted only when evidence changes a later task, problem strategy, process, verification rule, stream, or compiled framework page and the changed operation produces new evidence.
