---
id: apss.insight.learning-from-decision-quality-and-course-correction
type: insight
status: provisional
captured: 2026-07-12
source: APS framework maintainer
source_records:
  - operations/streams/working-sessions/2026-07-12-system-problem-review.md
related_insights:
  - apss.insight.evidence-deliberation-action-learning
  - apss.insight.surprise-cost-and-verification-regression-signals
related_work:
  - apss.review-learning
  - apss.review-problem-signal
compiled_into:
  - framework/README.md
  - framework/VOCABULARY.md
delivery: 7c273aa
---

# Learning should assess decision quality and explain course corrections

## Insight

### Claim

Learning should include an assessment of which decisions helped, which made the
problem worse, and what was learned from course corrections. It should also
retain a hypothesis about why the decision had that effect so later attempts
can test and refine the explanation rather than merely copy or avoid an action.
The assessment compares the decision's expected effect with later problem-
signal or outcome evidence and retains relevant context and confounders.
Processes should consider whether an explicit causal hypothesis would improve
future decisions, but need not create one for every grooming invocation.
When such a hypothesis is retained, keep it simple and include a credible
alternative or challenging evidence only when material.

### Scope

The interpretation applies when a system has recoverable decisions, task
results, verification evidence, and subsequent corrections. It concerns
learning and adaptation, not a claim that every decision has a knowable single
cause or that correlation establishes causation. Causal explanations remain
hypotheses unless stronger evidence supports them.
The hypothesis is most relevant when the explanation may influence later
strategy, verification, task selection, or adaptation.

### Reasoning

Problem solving changes course through decisions about framing, strategy,
tasks, verification, and process. If learning retains only the final outcome,
the system loses which choice preceded improvement or regression and why the
later correction may have worked. Connecting decisions to changes in the value
function and stating a falsifiable explanation can make later adaptation more
deliberate while preserving uncertainty and confounders.

## Evidence

### Supporting

- The APS framework maintainer proposed assessing good and harmful decisions,
  learning from course correction, and recording a hypothesis about why.
- The related
  [evidence–deliberation–action–learning insight](2026-07-10-evidence-deliberation-action-learning.md)
  already interprets APS as a recurring flow from evidence and decisions into
  action and later learning.
- The related
  [surprise and regression heuristic](2026-07-12-surprise-cost-and-verification-regression-signals.md)
  identifies worsened verification as a possible trigger for review.
- The proposed problem decision history supplies recoverable decisions that
  could be compared with later signal changes.
- The maintainer approved comparing expected effects with later problem signals
  or outcomes while retaining context, confounders, and causal uncertainty.

### Contradictory or limiting

- Outcome changes may have several causes, delayed effects, or confounders.
- A decision that worsens one signal may improve another or be rational under
  the evidence available at the time.
- Post-hoc explanations can become unjustified stories unless retained as
  hypotheses and tested against later evidence.
- No observed APS cycle yet shows that this practice improves later decisions.

## Possible implications

- Learning could connect material decisions, expected effects, observed signal
  changes, course corrections, and causal hypotheses.
- Verification records may need enough context to compare expected and actual
  effects without becoming a duplicate decision log.
- Adaptation could state which learned hypothesis justifies a change and what
  later evidence would challenge it.

## Open questions

- What observed use would show that this guidance improves later decisions
  without creating retrospective ceremony?

## Intake and clarification record

### 2026-07-12 — captured; clarification deferred

The maintainer proposed that learning assess which decisions were good, which
made the problem worse, what course correction taught, and a hypothesis about
why. The operator preserved causal explanation as a hypothesis rather than an
established fact.

Clarification is deferred while the maintainer finishes the active
problem-grooming questions. The next unanswered question is what evidence
should justify labeling a decision helpful or harmful.

### 2026-07-12 — decision-quality evidence clarified

The maintainer agreed that a helpful or harmful assessment should compare the
decision's expected effect with later problem-signal or outcome evidence and
retain context and confounders. Causation remains a hypothesis unless stronger
evidence exists.

The next clarification is whether every material course correction needs an
explicit causal hypothesis or only corrections whose explanation may affect
future decisions or adaptation.

### 2026-07-12 — hypothesis materiality clarified

The maintainer decided that a causal hypothesis should be considered but is not
required for every grooming invocation. Retain one when the explanation may
materially inform later strategy, verification, task selection, learning, or
adaptation; otherwise do not create ceremonial analysis.

The final clarification is whether a retained causal hypothesis should include
credible alternatives and the evidence that would challenge it when those are
material.

### 2026-07-12 — simple hypothesis boundary approved

The maintainer agreed that a retained hypothesis should note a credible
alternative or challenging evidence when material, while keeping the practice
simple. The source participated through the complete clarification sequence and
approved the progressively narrowed interpretation.

## Grooming record

### 2026-07-12 — provisional for lightweight learning guidance

- **Participants and sources:** APS framework maintainer and Codex operator;
  this insight, the related evidence-flow and surprise/regression insights, the
  proposed problem decision history, and current learning and verification
  definitions.
- **Clarified claim:** for a material decision or course correction, compare the
  expected effect with later problem-signal or outcome evidence and retain
  context and confounders. Consider a brief causal hypothesis when it may
  improve future work; add an alternative or challenging evidence only when
  material. Do not require this for every grooming invocation.
- **Inference audit:** the desired practice and simplicity boundary are
  maintainer judgment. Current APS evidence, verification, decision-history,
  learning, and adaptation concepts support the relationship, but no completed
  cycle yet demonstrates improved later decisions.
- **Supporting and limiting evidence:** recoverable decisions and signals make
  comparison possible; delayed effects, confounders, multi-signal trade-offs,
  and post-hoc stories limit causal confidence.
- **Alternative:** require a hypothesis for every material correction. The
  maintainer rejected that as unnecessary ceremony and chose consideration
  based on future usefulness.
- **Confidence and cost of error:** sufficient for short reversible guidance,
  not a mandatory analytic template. The main risks are false causal certainty
  and excessive retrospection; explicit hypothesis language and materiality
  limit them.
- **Disposition:** `provisional`, approved for compilation into the framework's
  learning guidance. Effectiveness remains unverified.
- **Reconsideration trigger:** a later APS cycle shows whether the practice
  improves decisions or instead creates burden or misleading explanations.
- **Source acknowledgment:** the maintainer approved the simple final boundary.
- **Delivery:** delivered with the accepted framework session in commit
  `7c273aa`, pushed to `origin/main` on 2026-07-12.
