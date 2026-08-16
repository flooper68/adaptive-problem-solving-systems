---
id: apss.compile-start-simple-principle
type: task
status: closed
owner: APS framework maintainer
created: 2026-08-06
closed: 2026-08-16
addresses: [P1]
source: APS framework maintainer, during the grooming-consolidation session
source_records:
  - ../../streams/insights/archived/2026-08-06-start-simple-add-only-when-needed.md
  - ../../streams/insights/archived/2026-08-06-processes-are-compiled-knowledge.md
  - ../../streams/working-sessions/2026-08-06-grooming-consolidation.md
---

# Compile the start-simple principle into framework guidance

## Proposed action

In a brainstorming session, compile the maintainer's principle — always start
simple, add only when needed — into the normative framework's guidance on
defining systems and processes, following `knowledge-compilation.md`.

## Intended result

The framework explicitly tells someone defining an APS system to declare the
simplest structure that does the job and to add distinctions, processes, or
fields only when observed use demonstrates need — rather than the principle
living implicitly in one instantiation's strategy.

## Motivation

The maintainer clarified during insight intake that the principle is
framework-worthy, not an Operations-local preference. Operations has applied
it repeatedly (strategy points 2–4, seven pruning dispositions, the grooming
consolidation) and the framework never states it for consumers.

## Evidence

- [Insight: Always start simple, add only when
  needed](../../streams/insights/archived/2026-08-06-start-simple-add-only-when-needed.md).
- [Grooming-consolidation
  session](../../streams/working-sessions/2026-08-06-grooming-consolidation.md),
  where four per-kind grooming processes collapsed into one with no loss the
  first invocations have contradicted.

## Open questions

- Where does the guidance belong — the framework README's system-definition
  guidance, the System vocabulary entry, or both?
- The linked insight must be groomed to `supported` or explicitly provisional
  before compilation.

## Grooming log

### 2026-08-06 — captured

Captured by the Claude Code operator during insight intake, at the
maintainer's clarification that the insight is framework-worthy. Not yet
groomed.

### 2026-08-07 — ready; scope widened to both principles

Groomed in the
[first cadenced grooming invocation](../../streams/working-sessions/2026-08-06-first-cadenced-grooming.md);
approved by the maintainer. Both source insights are now assessed
**supported**: [start-simple](../../streams/insights/archived/2026-08-06-start-simple-add-only-when-needed.md)
and [processes-are-compiled-knowledge](../../streams/insights/archived/2026-08-06-processes-are-compiled-knowledge.md),
which grooming linked here so one brainstorming session compiles both —
"declare the simplest current version; let history hold the rest." That
clears this task's open question; the task is **ready** for selection,
proposed after the information-stream review. Carried forward unresolved,
per the reviewer's caveat: whether compiled framework knowledge consumed by
others needs citable releases rather than git history alone — the
brainstorming session decides how far the second principle's compilation
reaches.

### 2026-08-07 — claimed by automated brainstorming

Claimed by the Claude Code operator for an
[automated brainstorming](../../processes/sessions/automated-brainstorming.md)
invocation, per [`ai-agent-tasks.md`](../../processes/ai-agent-tasks.md).
Addresses P1: compiling validated maintainer principles into the framework
exercises the compilation responsibility of P1's loop and implements system
strategy point 4 by stating, for consumers, the rule the strategy already
applies. Scope: compile both supported source insights into the framework
definition and vocabulary with a changelog entry, update the insights'
`compiled_into` links, and retain a working-session record. Acceptance: the
framework explicitly tells someone defining an APS system to start simple and
to treat processes as compiled knowledge, verification checks pass, and the
maintainer approves the uncommitted diff.

### 2026-08-07 — executed; awaiting maintainer review

Current state: both principles compiled as uncommitted changes — start-simple
guidance in the framework definition's system-creation steps, the
records-versus-compiled boundary in the `Compiled knowledge` vocabulary
entry, the replace-not-archive rule with its cautions in the framework
definition, changelog entry appended, both insights' `compiled_into` updated.
Decisions, validation, and reviewer findings are in the
[working-session record](../../streams/working-sessions/2026-08-07-start-simple-compilation.md).
Next step: maintainer review of the uncommitted diff; on approval, deliver
and archive this task per `ai-agent-tasks.md`.

### 2026-08-16 — accepted and closed

The maintainer reviewed and accepted both material choices: start-simple
remains operational guidance rather than a separate vocabulary concept, and
citable releases remain a strategy choice rather than an APS requirement.
Final reason: the intended framework guidance is compiled, source limits and
uncertainty are preserved, validation passes, and the reviewed session scope
is approved for delivery to `origin/main`.
