# Framework operating loop

This process operates the APSS Framework Operations System. Responsibilities
may overlap, but none may be silently omitted.

When an AI agent performs the work, also follow
[`ai-agent-tasks.md`](ai-agent-tasks.md) for claiming, human review, and delivery.

1. Read `operations/SYSTEM.md`, the current plan, relevant backlog items, recent
   work log, published framework knowledge, operational meta-knowledge,
   examples, feedback, and other new evidence.
2. Capture direct consumer reports through `framework-feedback-intake.md` and
   assess them through `framework-feedback-grooming.md`. Preserve feedback as
   evidence; when its disposition is actionable, create or link a distinct work
   candidate through `backlog-intake.md`.
3. Conduct and retain material collaborative exploration through
   `working-session.md`. Keep observations, insights, questions, and decisions
   distinguishable in their source record. Capture a separate executable
   response through `backlog-intake.md` only when action is proposed; groom
   those work candidates through `backlog-grooming.md`.
4. The maintainer selects ready, bounded work into `operations/work/PLAN.md` and
   confirms owner, acceptance conditions, authority, and validation approach.
5. Resolve load-bearing uncertainty through a working session, research, or
   experimentation. Preserve sources and distinguish evidence from inference.
6. For normative framework work, run
   [`knowledge-compilation.md`](knowledge-compilation.md) to compile the
   evidence into a candidate framework artifact and provenance report. For
   operational or example work, make the smallest coherent changes authorized
   by the plan. Record material decisions and deviations in
   `operations/work/LOG.md`.
7. Run `operations/processes/artifact-validation.md` against the candidate and other
   changes. A framework candidate is not publishable while known consistency,
   schema, link, example, or review failures remain.
8. Run or arrange `operations/processes/outcome-validation.md`. Outcome evidence may
   arrive later than artifact validation; record that gap rather than claiming
   effectiveness.
9. Update the compilation report with validation results. Recompile and repeat
   validation if the evidence changes the candidate. Route operations-specific
   lessons to the declared process, validation, plan, stream, or system target,
   and keep raw evidence at its source or durable reference.
10. Run [`framework-adaptation.md`](framework-adaptation.md) to review the
    sealed candidate. The maintainer approves normative publication; only then
    does the compiled candidate update `framework/` and its changelog.
11. Follow `release.md` when publishing a coherent framework version. Otherwise
    record the stopping point, next trigger, or handoff in the plan and log.

The process has completed one full adaptive cycle only when evidence has changed
a subsequent plan, strategy, process, validation, stream, knowledge artifact,
or system structure under declared authority.
