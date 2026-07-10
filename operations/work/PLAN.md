# Current plan

## Goal

Complete and validate the first evidence-driven improvement cycle of the APSS
Framework Operations System, from an observed consumer need through an approved
change and its outcome.

## Completed bootstrap

- Separated the normative framework, supporting examples, and framework
  operations at the repository root.
- Declared `operations/` as the system that improves the framework.
- Established durable backlog intake and grooming.
- Validated repository references and declaration structure.

## Current work

### Preserve the framework origin and clarify learning-to-framework adaptation

- Status: awaiting maintainer review; implementation and artifact validation
  completed by Codex operator on 2026-07-10.
- Scope: retain the earliest recoverable framework definition as provenance,
  retain its original source discussion, define a reproducible
  knowledge-compilation process, and make the separate approval-controlled path
  from compiled learning to normative framework changes explicit.
- Acceptance: source discussion and expected output are self-contained,
  separate `operations-work` fixtures; the general compilation and validation
  processes define how to compare a candidate with a hidden historical output
  without answer leakage; the initial application remains pending work rather
  than a separate process; `framework/` is the published compiled-knowledge
  artifact; only approved adaptation publishes a candidate; no secondary
  operations knowledge artifact competes with `framework/`; declarations and
  local references remain valid.

### Define a minimal AI agent task process

- Status: pushed to `origin/main` in commit `45d18a5`.
- Scope: define claim, execution, logging, human review, commit, and push.
- Acceptance: the process is concise, connected to stewardship operations, and
  requires human approval before an agent commits or pushes.
- Delivery: reviewed by the maintainer, committed, and pushed.

## Next milestone

1. Select a consumer need with enough evidence to test an improvement.
2. Groom the linked work to an explicit disposition using the declared process.
3. If ready and approved, select it into this plan with bounded acceptance and
   validation conditions.
4. Execute, validate artifact and outcome, compile learning, and apply an
   approved adaptation to a subsequent run.

## Owner

APSS framework maintainer.

## Open questions

- Which idea should become the first end-to-end validation of the new operating
  loop?
- What real consumer application should supply the first outcome evidence?
