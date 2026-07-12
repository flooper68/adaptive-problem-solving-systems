---
id: apss.insight.surprise-cost-and-verification-regression-signals
type: insight
status: provisional
captured: 2026-07-12
source: APS framework maintainer
source_records:
  - operations/streams/working-sessions/2026-07-12-system-problem-review.md
related_insights: []
related_work:
  - apss.review-problem-grooming
  - apss.review-problem-signal
compiled_into:
  - framework/README.md
delivery: 7c273aa
---

# Surprise, excess resource use, and verification regression are useful review signals

## Insight

### Claim

Three practical questions may reveal information worth grooming: did anything
surprising happen, did anything take more time or resources than expected, and
did anything worsen the verification value function? The underlying raw data
should be preserved or recoverably referenced whenever available so it can be
recompiled under later insights. A positive answer is a signal to preserve and
interpret evidence, not automatic proof that a new problem exists.

### Scope

The heuristic is proposed as a general best practice for operating processes,
source-specific grooming, problem grooming, verification, and retrospection to
notice consequential deviations. Each process definition may adapt the exact
questions, timing, thresholds, context, and evidence handling. The guidance
does not require duplicating data already recoverable from a native source and
does not prescribe a universal metric, cadence, or problem-creation decision.

### Reasoning

Surprise may expose a false assumption or previously unseen condition. Excess
time or resource use may expose an underestimated difficulty, capability gap,
or inefficient strategy. A worsened value function is direct evidence that an
attempt may have harmed the problem condition. Asking these questions creates a
small common screen without assuming every deviation has the same cause or
importance. Preserving the source data separately from the first interpretation
allows later grooming or knowledge compilation to revisit it when strategies,
questions, or insights change.

## Evidence

### Supporting

- The APS framework maintainer proposed the three questions while clarifying
  how streams and processes should surface issues for grooming.
- The current [verification process](../../processes/verification.md) already
  requires recording confounders, failures, and whether a problem improved,
  worsened, or remained unresolved.
- The current [problem-grooming process](../../processes/problem-grooming.md)
  considers new evidence and strategy challenges but does not yet name this
  heuristic.
- The normative framework already requires
  [raw evidence to remain recoverable](../../../framework/README.md#stream-raw-evidence-and-compiled-knowledge)
  because later strategies or questions may make previously ignored details
  important and compiled knowledge should remain revisable.

### Contradictory or limiting

- Surprise may reflect learning without indicating a harmful condition.
- Resource overruns may come from inaccurate estimates rather than a reusable
  problem.
- Temporary verification regression may be an accepted trade-off or measurement
  noise.
- Raw data may be unavailable, unsafe to retain, disproportionately expensive,
  or meaningless without enough context and provenance.
- No observed comparison yet shows that routinely asking these questions
  improves grooming decisions.

## Possible implications

- APS guidance could document the questions as a reusable best practice while
  process definitions specialize their application.
- Repeated positive answers could inform problem proposals, strategy revision,
  estimation learning, or process adaptation.
- The heuristic could help distinguish routine completion reporting from
  deviations worth retaining as evidence.

## Open questions

- What minimum context must accompany raw data so later recompilation remains
  meaningful?
- What observed use would support compiling it into reusable guidance?

## Intake and clarification record

### 2026-07-12 — captured; clarification deferred

The maintainer proposed: “is anything surprising?”, “did anything take more
time/resources than expected?”, and “did anything worsen the verification/value
function?” The operator preserved these as a proposed review heuristic and
added the limiting interpretation that a positive answer prompts evidence
review rather than automatically opening a problem.

The source asked to finish the current problem-grooming questions before being
grilled on follow-up ideas. The next unanswered clarification is whether any
positive signal should always be retained or whether a materiality judgment
comes first.

### 2026-07-12 — raw evidence clarification

The maintainer answered that the system should always try to record available
raw data because later insights may support recompiling it differently. The
operator normalized “raw data” to APS's broader `raw evidence` term and retained
the existing boundary that a recoverable native reference is sufficient; the
system need not create a duplicate copy.

The positive signal therefore triggers an attempt to preserve or reference the
underlying raw evidence, while source-specific grooming still decides what the
evidence means and problem grooming decides whether it warrants a problem. The
next clarification is where in operation the three-question screen should be
asked.

### 2026-07-12 — general guidance with process-specific details

The maintainer answered that the heuristic should be documented as a general
best practice, while each process definition may vary the details. The claim
and scope now separate reusable guidance from process-specific wording, timing,
thresholds, context, and evidence handling.

The final load-bearing intake question is whether the general best practice
belongs in the normative framework guidance or a non-normative Operations
playbook.

### 2026-07-12 — normative recommended-guidance target approved

The maintainer approved documenting the heuristic in normative APS guidance
while leaving implementation details to each process definition. The source
participated through all three clarification decisions and did not identify a
correction to the compiled claim, scope, reasoning, evidence, or limitations.

## Grooming record

### 2026-07-12 — provisional for recommended framework guidance

- **Participants and sources:** APS framework maintainer and Codex operator;
  this insight, the normative raw-evidence guidance, Framework Operations
  verification and problem-grooming processes, and the related evidence-flow
  insight.
- **Clarified claim and use:** the three questions are general recommended
  process-design guidance. Processes specialize timing, wording, thresholds,
  context, and evidence handling. Available raw evidence should be preserved or
  recoverably referenced for later reinterpretation and recompilation.
- **Inference audit:** the questions and intended general use are maintainer
  judgment. Their fit with recoverable raw evidence and verification regression
  is supported by current APS semantics. Their effectiveness across systems is
  not yet observed.
- **Supporting and limiting evidence:** the questions target assumptions,
  estimation error, and harmful attempts, but surprise may be benign, overruns
  may reflect estimates, regression may be noise or trade-off, and raw evidence
  may be unsafe, unavailable, costly, or contextless.
- **Alternative:** keep the heuristic Operations-specific. The maintainer chose
  normative recommended guidance because the screen is domain-independent and
  does not prescribe implementation.
- **Confidence and cost of error:** sufficient confidence for small reversible
  guidance, not for a mandatory process requirement. The primary risk is
  ceremony or overinterpreting deviations; process-specific application and
  explicit non-automatic problem creation limit that risk.
- **Disposition:** `provisional`, approved for compilation into
  `framework/README.md` as recommended guidance. This does not establish that
  using the questions improves outcomes.
- **Reconsideration trigger:** observed use showing improved discovery and
  learning, or feedback that the screen creates noise, burden, or misleading
  conclusions.
- **Source acknowledgment:** the maintainer approved the normative guidance
  target after reviewing the progressively clarified interpretation.
- **Delivery:** delivered with the accepted framework session in commit
  `7c273aa`, pushed to `origin/main` on 2026-07-12.
