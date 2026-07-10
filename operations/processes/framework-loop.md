# Framework operating loop

This process operates the APSS Framework Operations System. Responsibilities
may overlap, but none may be silently omitted.

When an AI agent performs the work, also follow
[`ai-agent-tasks.md`](ai-agent-tasks.md) for claiming, human review, and delivery.

1. Read `operations/SYSTEM.md`, the current plan, relevant backlog items, recent
   work log, published framework knowledge, operational meta-knowledge,
   examples, feedback, insights, and other new evidence.
2. Capture direct consumer reports through `framework-feedback-intake.md` and
   assess them through `framework-feedback-grooming.md`. Preserve feedback as
   evidence; when its disposition is actionable, create or link a distinct work
   candidate through `backlog-intake.md`.
3. Use [`brainstorming.md`](brainstorming.md) to discuss an idea, task, or
   research topic with the maintainer and iteratively compile reviewable changes
   into the framework or a concrete instantiation. Keep observations, insights,
   questions, and decisions distinguishable. Capture independently useful
   interpretations through `insight-intake.md` and assess them through
   `insight-grooming.md`. Capture a separate executable response through
   `backlog-intake.md` only when action is proposed; groom those work candidates
   through `backlog-grooming.md`.
4. The maintainer selects ready, bounded work into `operations/work/PLAN.md` and
   confirms owner, acceptance conditions, authority, and validation approach.
5. Resolve load-bearing uncertainty through brainstorming, research, or
   experimentation. Preserve sources and distinguish evidence from inference.
6. For normative framework work, run
   [`knowledge-compilation.md`](knowledge-compilation.md) to compile the
   evidence directly into uncommitted framework changes and its changelog. For
   operational or example work, make the smallest coherent changes authorized
   by the plan. Record material decisions and deviations in
   `operations/work/LOG.md`.
7. Run [`artifact-validation.md`](artifact-validation.md) against the proposed
   changes. A framework change is not publishable while known consistency,
   schema, link, example, or review failures remain.
8. Run or arrange [`outcome-validation.md`](outcome-validation.md). Outcome
   evidence may arrive later than artifact validation; record that gap rather
   than claiming effectiveness.
9. Recompile and repeat validation if new evidence changes the proposed
   knowledge. Route operations-specific lessons to the declared process,
   validation, plan, stream, or system target, and keep raw evidence at its
   source or durable reference.
10. Run [`framework-adaptation.md`](framework-adaptation.md) to review the
    uncommitted changes. The maintainer approves normative publication and use.
11. Follow `release.md` when publishing a coherent framework version. Otherwise
    record the stopping point, next trigger, or handoff in the plan and log.

The process has completed one full adaptive cycle only when evidence has changed
a subsequent plan, strategy, process, validation, stream, knowledge artifact,
or system structure under declared authority.
