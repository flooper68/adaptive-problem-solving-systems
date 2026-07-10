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

### Define work sessions as the system-owned processing layer

- Status: approved by the maintainer on 2026-07-10 and delivered to
  `origin/main` by the commit containing this entry.
- Scope: use the current brainstorming to compile its domain-independent
  conclusions, define `brainstorming` as the first work session in the normative
  framework, and exercise it in Framework Operations and the CNC example.
- Acceptance: streams remain input/evidence channels; `work_sessions` entries
  contain only an ID, description, and same-named process link; brainstorming
  iteratively discusses and compiles reviewable changes with the user; other
  loop responsibilities remain ordinary processes; compilation uses the
  authoritative artifact and simple changelog without a candidate archive or
  report; supporting documentation validates; no commit or push occurs before
  review.

### Make completed insight capture self-delivering

- Status: pushed to `origin/main` in commit `c543cc0` after maintainer review
  and approval on 2026-07-10.
- Scope: require agents to announce insight gathering with a direct link to the
  governing process, and define when completed maintainer-led intake is
  committed and pushed without a redundant delivery prompt.
- Acceptance: the intake process makes the workflow visible at invocation,
  defines a safe and bounded delivery signal consistent with maintainer
  authority, preserves normal review when that signal is absent, and the
  current open-problem insight is ready to ship with the approved process
  change.

### Preserve the framework origin and clarify learning-to-framework adaptation

- Status: pushed to `origin/main` in commit `a6def80` after maintainer review
  and approval on 2026-07-10.
- Scope: retain the earliest recoverable framework definition as provenance,
  retain its original source discussion, define a reproducible
  knowledge-compilation process, and make the separate approval-controlled path
  from compiled learning to normative framework changes explicit.
- Acceptance: the source discussion is retained as the first working session
  and its expected output is a separate, self-contained fixture in the same
  stream; the general compilation and validation processes define how to
  compare a candidate with a hidden historical output without answer leakage;
  the initial application remains pending work rather than a separate process;
  `framework/` is the published compiled-knowledge artifact; only approved
  adaptation publishes a candidate; no secondary operations knowledge artifact
  competes with `framework/`; declarations and local references remain valid.

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
