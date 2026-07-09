# Framework operating loop

This process operates the APSS Framework Operations System. Responsibilities
may overlap, but none may be silently omitted.

When an AI agent performs the work, also follow
[`ai-agent-tasks.md`](ai-agent-tasks.md) for claiming, human review, and delivery.

1. Read `operations/SYSTEM.md`, the current plan, relevant backlog items, recent work log,
   compiled knowledge, framework artifacts, examples, feedback, and other new
   evidence.
2. Capture direct consumer reports through `framework-feedback-intake.md` and
   assess them through `framework-feedback-grooming.md`. Preserve feedback as
   evidence; when its disposition is actionable, create or link a distinct work
   candidate through `backlog-intake.md`.
3. Capture other uncommitted ideas through `backlog-intake.md`; groom work
   candidates through `backlog-grooming.md`.
4. The maintainer selects ready, bounded work into `operations/work/PLAN.md` and
   confirms owner, acceptance conditions, authority, and validation approach.
5. Resolve load-bearing uncertainty through declared discussion, research, or
   experimentation. Preserve sources and distinguish evidence from inference.
6. Change the smallest coherent set of normative artifacts, examples, or
   operations authorized by the plan. Record material decisions and deviations
   in `operations/work/LOG.md`.
7. Run `operations/validation/artifact.md`. A framework change is not complete
   while known consistency, schema, link, example, or review failures remain.
8. Run or arrange `operations/validation/outcome.md`. Outcome evidence may
   arrive later than artifact validation; record that gap rather than claiming
   effectiveness.
9. Compile stable, reusable lessons into `operations/knowledge/README.md` and
   append its changelog. Retain raw evidence through its source or durable
   reference.
10. Present proposed adaptations to the maintainer. After approval, update the
   framework, system declaration, processes, plan, or other declared target so
   the next run actually uses the learning.
11. Follow `release.md` when publishing a coherent framework version. Otherwise
    record the stopping point, next trigger, or handoff in the plan and log.

The process has completed one full adaptive cycle only when evidence has changed
a subsequent plan, strategy, process, validation, stream, knowledge artifact,
or system structure under declared authority.
