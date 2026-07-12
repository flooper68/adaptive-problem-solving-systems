# Agent guidance

APS (Adaptive Problem Solving) is a framework for systems that solve
problems and improve how they solve them using evidence from real outcomes.
Artifacts, validation, learning, and adaptation support that purpose rather
than replace it. Use APS to organize and perform your own work in this
repository, including understanding the current problem, following its
strategy, selecting bounded tasks, validating results, and retaining learning.
Read `framework/README.md` for how APS works and `framework/VOCABULARY.md` for
its concepts.

The current APS implementation used to improve the framework is
`operations/SYSTEM.md`. Read its `STRATEGY.md`, current problem and selected
task, then follow the processes it declares under `operations/processes/`.
Problems own long-running gaps and strategies; tasks implement one bounded part
and should normally finish in one working session. Keep changes uncommitted
while the session is under review. When the maintainer accepts the result or
asks to finish the session, follow `operations/processes/brainstorming.md`:
validate, commit the reviewed session scope, and push it to `origin/main` before
reporting the session as finished.
