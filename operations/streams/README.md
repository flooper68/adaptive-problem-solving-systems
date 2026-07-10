# Stewardship evidence streams

The system retains raw evidence where it naturally originates when practical
and keeps a durable summary or reference when the source is external. Git is
the detailed provenance record for repository changes.

## Stewardship work

Backlog items, the current plan, and the work log preserve candidate actions,
dispositions, decisions made during execution, execution history, and gaps.
They are operational evidence, not normative framework content. Sealed
compilation candidates and their provenance reports are retained under
[`../work/compilations/`](../work/compilations/).

## Working sessions

Bounded meetings, discussions, brainstorming exchanges, and asynchronous
working threads are retained in the [`working-sessions/`](working-sessions/)
stream through the
[working-session process](../processes/working-session.md). A session may
contain observations, insights, questions, decisions, and candidate actions,
but only an explicitly created response enters the executable backlog.

The initial APSS
[kickoff session](working-sessions/2026-07-09-initial-framework-kickoff.md) and
its separately retained
[framework definition](working-sessions/2026-07-09-initial-framework-definition.md)
provide input and hidden expected-output fixtures for a compilation replay.
Later-discovered contemporaneous source material may be added to the kickoff
session's source boundary; retrospective recollections must be labelled as
reconstructions rather than original records.

## Insights

Independently useful interpretations are retained in the
[`insights/`](insights/) stream through
[intake](../processes/insight-intake.md) and
[grooming](../processes/insight-grooming.md). Insight records preserve the
source claim, inference, scope, supporting and limiting evidence, uncertainty,
and an epistemic disposition. They may link to compilation, decisions, or
separate executable responses without becoming those artifacts.

## Framework usage

Examples, reviews, discussions, and observed applications provide evidence of
whether consumers can understand and apply APSS. A retained summary should say:

- who or what applied the framework and in what context;
- what they attempted;
- where interpretation or execution failed or succeeded;
- what outcome was observed; and
- where the native evidence can be recovered, subject to privacy and access.

## Direct framework feedback

Direct reports from consumers are retained in the
[`framework-feedback/`](framework-feedback/) stream using the declared
[intake](../processes/framework-feedback-intake.md) and
[grooming](../processes/framework-feedback-grooming.md) processes. The report
preserves what the consumer experienced; grooming records interpretation and a
disposition. Actionable reports link to separate work candidates rather than
being silently converted into requirements.

## External foundations

Research items retain citations and distinguish source claims from APSS
interpretation. Prefer authoritative or primary sources when a claim affects
the normative framework. Absence of research is recorded as uncertainty, not
as evidence that no prior work exists.

## Validation evidence

Artifact checks, example conformance, consumer trials, and outcome observations
are retained in the relevant work item or work log with enough context to
repeat or challenge the conclusion.
