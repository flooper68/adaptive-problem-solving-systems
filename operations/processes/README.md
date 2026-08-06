# Processes

A derived index of the declared processes by loop stage; `SYSTEM.md` and the
process files themselves stay authoritative. Processes are compiled
knowledge — superseded versions live in git history, not archives.

Work-session processes — one per session type declared in `SYSTEM.md`
`work_sessions` — live under [`sessions/`](sessions/); the rest of the
processes support them.

| Loop stage | Process |
| --- | --- |
| Orchestrate the whole loop | [`process.md`](process.md) |
| Capture inputs (feedback, insights, task candidates) | [`intake.md`](intake.md) |
| Assess inputs and decide (all kinds, incl. problems) | [`grooming.md`](sessions/grooming.md) |
| Deliberate and compile changes | [`brainstorming.md`](sessions/brainstorming.md), [`knowledge-compilation.md`](knowledge-compilation.md) |
| Execute a selected task autonomously (experimental) | [`sessions/automated-session.md`](sessions/automated-session.md) |
| Propose dispositions autonomously (experimental) | [`sessions/automatic-grooming.md`](sessions/automatic-grooming.md) |
| Check results against signals | [`verification.md`](verification.md) |
| Adopt and publish | [`framework-adaptation.md`](framework-adaptation.md), [`release.md`](release.md) |
| Agent conduct and handoffs | [`ai-agent-tasks.md`](ai-agent-tasks.md) |

Current state and next work live in [`../STATE.md`](../STATE.md) and each
problem file's `Current state` section.
