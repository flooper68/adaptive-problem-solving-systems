# Framework stewardship backlog

This directory contains durable ideas that have not yet been selected into the
current plan. Presence here does not imply commitment or priority.

Use [backlog intake](../../processes/backlog-intake.md) to capture a new idea and
[backlog grooming](../../processes/backlog-grooming.md) to clarify it and assign
an approved disposition.

## States

- `captured` — preserved but not yet analyzed enough for disposition.
- `grooming` — analysis is materially underway.
- `ready` — can be considered during planning.
- `deferred` — retained with an explicit reconsideration trigger.
- `rejected` — retained with rationale so the decision is recoverable.
- `merged` — represented by another durable item.

Selection into `operations/work/PLAN.md` changes a ready item to `planned`.
Execution may then use `in-progress`, `completed`, or `cancelled`; material
events still belong in `operations/work/LOG.md`.

## Items

- [Refine the knowledge-compilation process](knowledge-compilation-refinement.md)
  — captured; the failure modes, desired guarantees, and smallest useful
  refinement remain to be established.
- [Define a grilling protocol for backlog candidates](backlog-candidate-grilling.md)
  — captured; should extend the existing intake and grooming processes without
  adding unnecessary ceremony.
- [Define a process for reporting current context and state](current-state-reporting.md)
  — captured; consumers, triggers, and the boundary with plans and logs require
  grooming.
- [Create a practical guide for defining a system](system-definition-guide.md)
  — captured as an extension of the framework's concise creation checklist;
  format and validation approach remain open.
- [Compile and maintain a domain dictionary](compiled-domain-dictionary.md)
  — captured; compilation rules, artifact location, and normative status are
  unresolved.
- [Modularize growing concerns from `SYSTEM.md`](modular-system-concerns.md)
  — captured with strategy as the first candidate; extraction thresholds and
  declaration/schema implications require grooming.
- [Generate visual HTML from APSS system declarations](visual-html-generator.md)
  — captured from actionable framework feedback; implementation scope and
  acceptance conditions require backlog grooming.
- [Add software-development and research-project examples](software-and-research-examples.md)
  — captured; candidate examples and validation approaches are not yet chosen.
- [Define reusable processes for producing good evidence](general-evidence-processes.md)
  — captured; grooming must determine scope and normative status.
- [Map APSS to organizational management frameworks](management-framework-mappings.md)
  — captured; the framework set, comparison method, and wiki shape remain open.
- [Research established foundations related to APSS](research-foundations.md)
  — includes scientific literature on adaptive systems; deferred until after
  the first operating cycle or until related evidence becomes load-bearing.
