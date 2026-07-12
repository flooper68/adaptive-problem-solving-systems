---
id: apss.insight.problem-decomposition-needs-general-best-practices
type: insight
status: captured
captured: 2026-07-12
source: APS framework maintainer
source_records: []
related_insights:
  - apss.insight.goals-decompose-into-open-problems
related_work:
  - operations/tasks/research-foundations.md
compiled_into: []
---

# Problem decomposition needs discoverable general best practices

## Insight

### Claim

APS should include a clearly discoverable section that synthesizes practical,
evidence-informed best practices for decomposing problems. Defining a problem
hierarchy and naming decomposition as a responsibility are not enough to help a
reader perform decomposition well.

### Scope

The proposed guidance should apply generally across APS domains rather than be
designed first for software, research, organizational work, or another specific
setting. Domain-specific examples may help explain or test general practices,
but the insight does not propose that practices from one domain be generalized
without evidence.

The claim concerns the need for usable and discoverable guidance. It does not
yet establish which practices deserve inclusion, how prescriptive they should
be, or whether the eventual section belongs in the normative framework
definition or in supporting compiled knowledge.

### Reasoning

Problem decomposition is central to moving from a root problem toward smaller
problems with their own strategies and bounded tasks. A reader who understands
that relationship may still need help judging how to identify useful
subproblems, choose boundaries, avoid premature or excessive decomposition,
and revise the hierarchy as evidence changes understanding.

The maintainer became curious about decomposition, looked for such guidance in
the framework, and did not find a clearly identifiable treatment. This suggests
a discoverability and practical-guidance gap. Synthesizing general best
practices could make the existing decomposition model more actionable without
assuming that the current framework already contains or validates those
practices.

## Evidence

### Supporting

- The maintainer looked for guidance on problem decomposition in the current
  framework and did not find it.
- The framework already makes evolving problem decomposition part of the
  system strategy and adaptive loop, so guidance on performing that
  responsibility would address an existing, consequential part of APS rather
  than introduce an unrelated concern.
- The earlier insight
  `apss.insight.goals-decompose-into-open-problems` established the usefulness
  of an evolving problem hierarchy while leaving the practical decomposition
  method largely unspecified.

### Contradictory or limiting

- The framework already describes the problem hierarchy and some decomposition
  effects, so the gap may partly be one of organization and discoverability
  rather than complete absence.
- No research review has yet established a domain-independent set of best
  practices or shown that one set transfers reliably across APS applications.
- Adding a normative section before gathering evidence could overstate
  provisional heuristics and conflict with the MVP strategy of avoiding
  unsupported complexity.

## Possible implications

- Research established problem-decomposition methods across multiple domains
  to identify recurring practices, boundary conditions, and disagreements.
- Compile a practical decomposition guide that covers forming useful
  subproblems, choosing depth and boundaries, maintaining traceability to the
  parent problem, and revising the hierarchy from evidence.
- Make decomposition guidance directly discoverable from the framework's
  problem-hierarchy and loop sections.
- Decide after research and use whether the result is normative framework
  content, supporting knowledge, or a smaller combination of both.

## Open questions

- Which decomposition practices have credible support across multiple domains?
- What makes a decomposition useful, and which observable failure modes reveal
  decomposition that is too coarse, too fine, overlapping, or solution-shaped?
- Which guidance is universally applicable and which must remain
  context-dependent?
- Should APS prescribe a minimum decomposition method or only provide
  heuristics and examples?
- Where should the guidance live so readers can find it without expanding the
  normative MVP unnecessarily?

## Intake and clarification record

### 2026-07-12 — captured and clarified

The maintainer initially stated that APS should have a section on problem
decomposition because it is crucial. When asked what prompted the claim, the
maintainer explained that they were curious about the subject and could not
find it in the framework. This is retained as a direct discoverability
observation rather than evidence that the framework's current decomposition
model is ineffective.

The maintainer clarified that the desired section should help readers find
best practices, not merely add another definition, and that its scope should be
general rather than specific to software, research, organizational work, or
another domain. The operator inferred that research and synthesis are needed
before naming particular practices or adopting normative requirements. The
maintainer participated through the clarification stopping point; no further
source correction was requested before delivery.

## Grooming record

Not yet groomed. See
[`insight-grooming.md`](../../processes/insight-grooming.md).
