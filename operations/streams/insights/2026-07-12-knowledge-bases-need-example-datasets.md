---
id: apss.insight.knowledge-bases-need-example-datasets
type: insight
status: captured
captured: 2026-07-12
source: APS framework maintainer
source_records: []
related_insights: []
related_work:
  - apss.review-compiled-knowledge
  - apss.software-and-research-examples
compiled_into: []
---

# Every knowledge base should include an example dataset

## Insight

### Claim

A knowledge base should include a set of examples that functions as a dataset
for learning how to interpret and apply its knowledge. The examples should
support both human learning and machine or agent learning and evaluation,
rather than leaving application knowledge implicit.

### Scope

The claim applies to knowledge bases generally, not only to APS. What belongs
in the example dataset depends on the knowledge base's subject, users, and
intended uses. Successful applications, failures, boundary cases, and
counterexamples may all be useful, but the insight does not prescribe a
universal mix or representation.

### Reasoning

Knowing propositions or instructions does not necessarily teach a learner how
to recognize when they apply, instantiate them in context, or distinguish
adequate from inadequate applications. Examples make those interpretations
inspectable. Treating examples as a dataset also makes them reusable for
teaching people, supplying context to agents, and evaluating whether either can
apply the knowledge.

## Evidence

### Supporting

- While considering how to share APS with others, the maintainer identified
  examples as a necessary part of learning the knowledge base rather than an
  optional APS-specific supplement.
- The maintainer expects the examples ideally to support both people and
  machines or agents.

### Contradictory or limiting

- No observed comparison has yet established that every kind of knowledge base
  benefits from maintaining examples as a dataset.
- The useful composition, structure, coverage, and maintenance rules may vary
  substantially by context.
- Some knowledge bases may depend on externally maintained examples rather
  than embedding them in the same artifact; whether linked examples satisfy
  the claim remains unresolved.

## Possible implications

- Knowledge-base design and compilation could treat example coverage as a
  first-class responsibility.
- APS could eventually ship with maintained application examples that teach
  its concepts and provide cases for agent evaluation.
- Verification could assess whether humans and agents can apply a knowledge
  base to held-out or newly encountered cases, not merely restate its content.

## Open questions

- Must the example dataset be contained within the knowledge base, or may it be
  a separately maintained but linked artifact?
- What minimum coverage makes an example set adequate for a particular
  knowledge base and audience?
- How should examples be structured so that the same source remains useful to
  humans, agents, and evaluators without creating unnecessary duplication?

## Intake and clarification record

### 2026-07-12 — captured and clarified

The maintainer initially stated that part of each knowledge base must be a set
of examples: effectively a dataset for learning the knowledge base. Although
this seems obvious, the maintainer observed that knowledge bases often omit it.

The prompting context was considering how to share APS with others. The
maintainer clarified that the claim applies to any knowledge base, not only
APS; the examples should ideally serve both humans and machines or agents; and
whether to include successes, failures, boundary cases, or counterexamples
depends on context.

The operator made explicit—but did not attribute to the maintainer—the
possible evaluation use and the uncertainty about whether linked examples must
be physically part of the same artifact. The source was shown the resulting
record for correction through the current Codex task.

## Grooming record

Not yet groomed. See
[`insight-grooming.md`](../../processes/insight-grooming.md).
