# Grooming

Groom captured inputs, tasks, problems, verification evidence, and session lessons into explicit, approved decisions guided by the system strategy. One process implements source-specific, problem, and task grooming; their responsibilities remain distinct in the questions asked and the state changed.

Grooming is where the loop exercises its judgement, not an inbox-clearing pass: a conforming invocation reads the in-scope signals itself, tests the problem picture against the strategy, and decides adaptation from what was learned before any work is selected.

Exact problem-state history lives in the ordinary project-owned [problem state log](../../records/problem-state-log.md); signal definitions remain in Verification and latest meaning remains in Current state.

## Invocation and scope

Groom on maintainer request, before substantial work selection, when new evidence accumulates, when a dependency resolves, when verification cannot read a signal, when an item blocks a consumer, or after every third completed working session since the last grooming invocation.

At the start, declare one proportional scope:

- **item** — one captured record, task, proposed problem, or existing problem;
- **branch** — one named problem and its descendants, reading its ancestor chain only for alignment; or
- **root** — the system problem and the whole active decomposition.

The same process and dispositions apply at every scope. Narrow work reads only enough system context to judge its item honestly. Branch work does not silently assess siblings. Root work supplies project-level grooming without creating another session type. A cadenced invocation defaults to root scope; the maintainer may explicitly narrow it when all material change lies in one branch, with excluded areas recorded as unassessed.

**Item scope is the quick groom.** It exists so one task or record can be decided without a full pass, and it is the only quick form — no separate session type. At item scope, step 2 is one sentence naming the problem the item serves; step 3 cites the most recent logged reading for that problem instead of taking a new one, and states its date; steps 4–6 collapse into naming the item; step 8 asks one question — does anything learned since the item was created change the decision — and records the answer; step 9 records the one disposition and the state change. Completion at item scope is met by that recorded disposition, the cited reading, and the step 8 answer. Item scope may move a task between backlog, todo, and cancelled, revise it, or link it; it may not close or open a problem, change a strategy, or create more than one task — any of those escalates to branch or root scope.

## Procedure

1. **Freeze the evidence boundary.** Name the scope and the latest event, session, or record included. Later arrivals wait unless they reveal immediate harm. Recover the previous grooming stopping point and its reconsideration triggers.

2. **Orient to the stable system model.** Before recent or loud arrivals set the agenda, read the system problem, strategy, verification, process, current state, and the problem, task, stream, and compiled-knowledge context relevant at the declared depth. State briefly: the current condition, theory, verification basis, operating constraints, and unresolved assumptions.

3. **Read the signal.** For each problem admitted at the declared scope, take its declared signal reading per Verification during this invocation — elicit the maintainer-judged components from the maintainer — and append the reading to the problem state log with optimistic `append_wiki_file`. Compare it with the prior entry and state improved, worsened, unchanged, unresolved, or unreadable. Reusing a recent reading instead of taking one is itself a maintainer decision, recorded with its reason; it is never the default. Do not invent a reading for an unreadable signal — an unreadable signal is a grooming finding that step 5 must face. At root scope, state the health judgement the readings support, or record why health stays unset.

4. **Reduce arrivals into material changes.** Deduplicate and group new records, completed or failed work, verification evidence, and session lessons by affected problem and consequence. Preserve links to the underlying evidence. Repeated symptoms of one condition are one material change, not priority multiplied by volume. Activity with no consequence remains context and stops here.

5. **Review the scoped problem picture against the strategy.** Before opening detailed histories, test each in-scope problem against the strategy's grooming guidance: it identifies its parent and states evidence, a desired outcome, a strategy, and a signal readable while it remains open; its relevance, impact, and current reading justify holding it; and change since the previous pass is stated. A problem that fails the test gets a disposition proposal — complete its declaration, reframe, merge, split, close, or investigate — not a pass. Keep activity distinct from improvement. Do not invent a reading or health verdict for an unreadable signal.

6. **Select a deliberately small focus.** Choose the items whose detailed grooming can change a decision, ordinarily one to three problems or coherent input groups for a root or branch invocation. Prefer evidence challenging strategy, material consumer harm, the highest-impact worsening or unresolved conditions, and owner-only decisions blocking them. Record excluded or unchanged areas and what would admit them later; running out of time is not a disposition.

7. **Groom each selected item deeply.**
   1. Orient to its authoritative Chaos House entity, linked evidence, decomposition context, and related work.
   2. Clarify the observation, inference, proposed response, scope, uncertainty, and relationship to problems and strategy without rewriting the source.
   3. Assess supporting and contradicting evidence, impact, confidence, cost of being wrong, and whether a missing answer could reverse the decision.
   4. Challenge duplication, stale state, unsupported inference, circular framing, conflicting sources of truth, ceremonial structure, and premature work creation. State the strongest objection or alternative before asking for a decision, and what later evidence would reopen it.
   5. Apply the responsibility specific to the item:
      - source-specific grooming interprets the observation and may propose propagation;
      - problem grooming tests framing, evidence, desired outcome, signal, strategy, relevance, priority, and lifecycle;
      - task grooming tests bounded scope, problem-strategy relationship, expected result, dependencies, validation, responsibility, and stopping condition.
   6. Propose exactly one disposition: **act**, **revise**, **keep** with a reconsideration trigger, **merge/link**, or **close** with reason. Evidence never creates work without this separate decision.
   7. Present the exact canonical mutations and obtain owner approval. Apply only approved actions session-bound; silence never authorizes them. Preserve provenance in both directions where the action model supports it and state normalization that remains only in content.

8. **Adapt from what was learned.** Enumerate the material learnings since the previous invocation — from completed and failed work, the readings taken in step 3, session lessons, and events outside the system — and for each record an explicit maintainer decision on whether it changes the problem statement, the decomposition, the problem or system strategy, verification, a process, or a stream. Retaining the current model is a recorded decision with its reason; an empty enumeration, not a skipped step, is the only way to record "nothing was learned". Decide adaptation before selecting tasks against the old model. Grooming may update problem, task, and stream state under its authority. A lesson about how a process runs schedules a retrospective on that process (`retrospective.md`) rather than a direct process edit; a framework-worthy lesson becomes a brainstorming or compilation task.

9. **Reconfirm work and close the scoped picture.** Compare candidate actions only after the problem picture and applicable strategy are current, and select work only when it implements or tests the problem strategy. Record selected next work or the explicit reason none is selected. Close with the scope and as-of boundary, orientation, readings taken and their comparisons, material changes, the strategy test's findings, selected focus, approved dispositions, adaptation decisions, handoffs, unassessed areas, and next trigger. Append any remaining approved assessments to the problem state log with optimistic `append_wiki_file`; project a root judgement to project health with `save_project`, and leave health unset when no defensible root judgement exists.

## Completion

An invocation is complete when every problem admitted at the declared scope has a signal reading taken this invocation and appended to the log, or a recorded maintainer decision reusing a recent reading, or a recorded unreadability finding; every in-scope problem has passed the strategy test or carries a disposition proposal for its failure; the adaptation enumeration and its decisions are recorded, including retained-unchanged decisions; every item admitted to deep grooming has one approved, recorded disposition; propagation is recoverable; selected next work is explicit or its absence is explained; excluded areas are named; and missing answers have evidence requests or reconsideration triggers.

The working-session record preserves the invocation boundary and decisions. Authoritative Chaos House entities and wiki pages retain current state; the session does not become a parallel source of truth.

## Signal

Read by the retrospective from session records: invocations meeting "Completion" ÷ invocations run; maintainer corrections of procedure per invocation; decisions reversed at a later grooming.
