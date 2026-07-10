# Insight grooming

## Purpose

Assess a captured insight as an interpretation: clarify its scope, audit how it
follows from evidence, seek support and contradiction, and record an explicit
epistemic disposition. Grooming does not silently convert the insight into
compiled knowledge, a decision, or executable work.

## Invocation and roles

Groom an insight when a planning or adaptation decision may depend on it, when
related evidence accumulates, when compilation needs to evaluate it, or when a
participant requests review.

- An operator facilitates analysis and preserves provenance and disagreement.
- The source clarifies intended meaning when available but need not prove or
  implement the claim.
- Relevant consumers or subject-matter validators may provide corroborating or
  contradictory evidence.
- The APSS framework maintainer approves the disposition for this operations
  system; normative adoption still requires framework compilation, validation,
  and adaptation approval.

Set `status: grooming` while assessment is materially underway. Do not rewrite
the source claim to fit the conclusion; append clarification and the grooming
record with provenance.

## Procedure

1. **Orient.** Read the insight, every material source record, related insights,
   current framework knowledge, relevant feedback, research, validation, work,
   and decisions.
2. **Restate the claim and scope.** Identify the smallest coherent conclusion,
   its intended context, affected consumers, and any ambiguous terms. Preserve
   the source's original meaning and record disagreements about restatement.
3. **Audit the inference.** Separate direct observations, external claims,
   assumptions, participant inference, and operator inference. Identify missing
   steps, causal claims, generalization, and alternative explanations.
4. **Test the evidence.** Seek corroborating and contradictory evidence
   proportionate to the claim. Use brainstorming, research, validation, or
   experiment when a missing answer could materially reverse the disposition.
5. **Assess usefulness and risk.** Record which understanding, compilation,
   decision, or possible response the insight could affect; the cost of being
   wrong; confidence; and contexts where it should not be applied.
6. **Choose a disposition.** Apply one status below with a rationale. The status
   is scoped to the assessed claim and evidence, not a universal truth label.
7. **Route without conflating.** Link supported or explicitly provisional
   insights into [`knowledge compilation`](knowledge-compilation.md) when
   relevant. Create separate work through
   [`task intake`](task-intake.md) only for an executable response, link
   an authorized decision to its decisional artifact, and leave the insight
   unchanged when no propagation is warranted.
8. **Close the loop.** Record source acknowledgment, disagreement, or
   unavailable review. Later evidence may reopen grooming without deleting the
   previous assessment.

## Dispositions and states

- `captured` — preserved but not yet assessed.
- `grooming` — assessment is materially underway.
- `supported` — the available evidence supports the scoped claim strongly
  enough for its recorded use; this is not automatic normative adoption.
- `provisional` — plausible and potentially useful, but material uncertainty
  remains; record what evidence or event should trigger reconsideration.
- `contested` — credible evidence or participant interpretations materially
  conflict; preserve the positions and needed resolution evidence.
- `unsupported` — the available evidence does not support the claim for the
  proposed scope or use; preserve the rationale and original source.
- `withdrawn` — the source no longer endorses the interpretation; preserve the
  original record and the source's correction without inferring that the claim
  was disproven.
- `superseded` — a later insight more accurately represents the interpretation;
  link it without deleting this record.

Compilation is a relationship recorded in `compiled_into`, not a disposition:
one insight may inform multiple compilations while retaining its epistemic
status. Likewise, an actionable response links through `related_work` rather
than changing the insight to an execution state.

## Required grooming record

Append a dated entry containing:

- participants and evidence consulted;
- clarified claim, scope, intended use, and source acknowledgment;
- observations, external claims, assumptions, and inference steps;
- supporting, contradictory, and unavailable evidence;
- alternative explanations, confidence, and cost of error;
- approved disposition and rationale;
- reconsideration trigger where relevant; and
- links to related insights, compilation, decisions, or separate work.
