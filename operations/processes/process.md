# Framework Operations process

This process operates the APS Framework Operations System. Responsibilities
may overlap, but none may be silently omitted.

When an AI agent performs the work, also follow
[`ai-agent-tasks.md`](ai-agent-tasks.md) for claiming, human review, and delivery.

1. Read `operations/SYSTEM.md`, `operations/STRATEGY.md`, the current problem
   and task files, relevant recent working sessions, published framework
   knowledge, operational meta-knowledge, observed applications, feedback,
   insights, and other new evidence.
2. Capture direct consumer reports through `framework-feedback-intake.md` and
   assess them through `framework-feedback-grooming.md`. Preserve feedback as
   evidence. When grooming identifies a gap already represented by an open
   problem, link it and propose bounded work through `task-intake.md` when
   useful. When the gap is not represented, propose it to problem grooming
   before selecting work.
3. Use [`brainstorming.md`](brainstorming.md) to discuss an idea, task, or
   research topic with the maintainer and iteratively compile reviewable changes
   into the framework or a concrete instantiation. Keep observations, insights,
   questions, and decisions distinguishable. Capture independently useful
   interpretations through `insight-intake.md` and assess them through
   `insight-grooming.md`. Source-specific grooming may propose a higher-level
   problem without opening one. Capture a separate executable response through
   `task-intake.md` when action is proposed; do not select it until problem
   grooming has opened or linked the problem it addresses. Groom work
   candidates through `task-grooming.md`.
4. Follow [`problem-grooming.md`](problem-grooming.md) to revisit relevant open
   problems in `operations/problems/`, then select ready, bounded tasks in
   `operations/tasks/` that state which problems they address and confirm
   owner, acceptance conditions, authority, and validation approach.
5. Resolve load-bearing uncertainty through brainstorming, research, or
   experimentation. Preserve sources and distinguish evidence from inference.
6. For normative framework work, run
   [`knowledge-compilation.md`](knowledge-compilation.md) to compile the
   evidence directly into uncommitted framework changes and its changelog. For
   operational or application work, make the smallest coherent changes
   authorized by the selected task. Update the task's current state and retain
   material decisions and deviations in the working-session record or native
   evidence.
7. Run [`verification.md`](verification.md). Complete immediate correctness
   checks, compare available evidence with the addressed problem's signal, and
   record any delayed observation without claiming effectiveness.
8. Recompile and repeat verification if new evidence changes the proposed
   knowledge. Route operations-specific lessons to the declared process,
   verification, task, stream, or system target, and keep raw evidence at its
   source or durable reference.
9. Run [`framework-adaptation.md`](framework-adaptation.md) to review the
   uncommitted changes. The maintainer approves normative publication and use.
10. Follow `release.md` when publishing a coherent framework version. Otherwise
   record the stopping point, next trigger, or handoff in the task and session
   record.

The process has completed one full adaptive cycle only when evidence has changed
a subsequent task, strategy, process, verification, stream, knowledge artifact,
or system structure under declared authority.
