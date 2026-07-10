# Task grooming

## Purpose

Turn a captured candidate action into an explicit, evidence-aware disposition
without silently treating it as committed work. Grooming improves decision
quality; it does not itself authorize execution or a normative framework
change.

## Invocation and roles

Groom an item when the maintainer requests it, new evidence makes it timely, a
dependency is resolved, or the current problem set needs another ready task.

- An operator facilitates the analysis and updates the durable item.
- The item owner supplies context or identifies who can.
- The APSS framework maintainer approves the final disposition and alone
  changes a ready task to `selected`.

Set `status: grooming` while analysis is materially underway.

## Procedure

1. **Orient.** Read the item, its source, current framework and examples,
   current strategy, problem files, compiled knowledge, related task files, and
   relevant session history.
2. **Check identity.** Merge duplicate actions, split unrelated actions, and
   preserve links to their original source records and IDs.
3. **Frame the response.** State the affected consumer, current goal and open
   problem, its strategy, proposed action, expected outcome, and why it belongs
   within this system's boundary. If no current open problem represents the
   evidenced gap, propose a problem file before treating the work as ready.
4. **Classify the effect.** Identify whether it may change the normative
   framework, a supporting example, stewardship operations, or only current
   understanding. One item may affect several, but the distinction must remain
   explicit.
5. **Resolve load-bearing uncertainty.** Use discussion, research, or a bounded
   experiment when a missing answer could materially reverse the disposition.
   Record facts, assumptions, disagreements, and unavailable evidence
   separately.
6. **Shape candidate work.** Describe the smallest coherent change or inquiry,
   affected artifacts, dependencies, risks, validation approach, and an owner.
   Split work that cannot be evaluated or completed as one bounded result.
7. **Check readiness.** Apply the readiness questions below. Unanswered
   questions are allowed only when the task approach explicitly resolves them
   before they become dangerous or expensive.
8. **Propose and approve a disposition.** The maintainer records one disposition
   and its rationale. Do not equate desirability with current priority.
9. **Propagate the result.** Update the item's frontmatter and grooming log.
   If selected, set `status: selected` and list its problem IDs under
   `addresses`, then move it from `tasks/backlog/` to the task root. Keep
   ready or deferred tasks in the backlog and move rejected or merged tasks to
   `tasks/archive/`. Do not erase the source or its rejected alternatives.

## Readiness questions

An item is ready only when the responsible operator can answer:

- Which current open problem does this address, and which goal makes that
  problem relevant?
- How does the work implement or test that problem's strategy?
- What consumer problem or opportunity are we addressing?
- What observable outcome would make the work worthwhile?
- Is the proposed scope bounded enough for one task?
- Which normative artifact, example, or operating process may change?
- What evidence supports acting now, and what remains assumption?
- Which discussion, research, or experiment is still necessary?
- How will artifact correctness and consumer outcome be validated separately?
- What dependencies, compatibility risks, or migration costs exist?
- Who owns execution, validation, and approval?
- What acceptance conditions permit the work to stop or be reconsidered?

## Dispositions and states

- `ready` — sufficiently understood to be considered for selection. This is
  not a commitment or priority promise.
- `deferred` — potentially valuable but blocked, premature, or deliberately
  postponed. Record a reconsideration trigger, condition, or date.
- `rejected` — outside the boundary, unsupported, harmful, or not worth
  pursuing. Preserve the rationale and evidence.
- `merged` — represented by another durable item. Record the target ID.

`captured` and `grooming` describe candidate work before disposition. They do
not apply to the source reports, insights, questions, issues, or decisions that
motivated it. Selection sets a ready task to `selected`; execution may then use
`in-progress`, `awaiting-review`, `closed`, or `cancelled`. Keep candidate
states under `tasks/backlog/`, selected and active states at the task root, and
inactive states under `tasks/archive/`. The task owns current state; session
records own material history.

## Required durable result

Append a grooming-log entry containing:

- date, participants, and evidence consulted;
- clarified problem, expected outcome, and scope;
- the current problem-file reference and relevant goal;
- important facts, assumptions, and unresolved questions;
- readiness gaps or acceptance conditions;
- approved disposition and rationale; and
- reconsideration trigger or target task when applicable.

Any normative change still follows the
[framework operating loop](framework-loop.md) and declared adaptation authority.
