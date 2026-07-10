---
id: apss.session.records-and-work
type: working-session
status: retained
recorded: 2026-07-10
participants: [APSS framework maintainer, Codex operator]
source: Maintainer-agent discussion in the current Codex task
related_sessions:
  - apss.session.insight-stream-design
related_feedback: []
related_insights:
  - apss.insight.evidence-deliberation-action-learning
related_work:
  - operations/work/LOG.md
---

# Separate retained records from executable work

## Frame

The session began by asking what the current APSS operations system could
report and where a meeting, discussion, or brainstorming exchange should be
recorded. Its scope then narrowed to whether insights, questions, and decisions
belong in an executable backlog and how the framework should retain this kind
of collaborative exploration.

A useful stopping point was an agreed conceptual boundary, a name for the
source stream, and authorization to define the process and retain this first
session. Repository implementation performed after that authorization is work
history rather than part of the source discussion.

## Source boundary

This is a topic-focused summary of the maintainer-agent conversation in the
current Codex task. It preserves the material distinctions, corrections, and
decisions rather than a full transcript. Repository files inspected during the
conversation supplied context; no external research or consumer-use report was
introduced.

## Discussion summary

The existing framework already recognizes meetings and discussions as
information streams and discussion/grilling as an uncertainty-resolution
capability. The operations implementation nevertheless put `insight`,
`question`, and `decision` in a backlog whose later states are `planned`,
`in-progress`, and `completed`.

The maintainer observed that those records cannot themselves be executed and
therefore should be treated like retained discussion outcomes rather than
backlog work. The operator initially classified that observation as framework
feedback. The maintainer corrected the classification: feedback should remain
a report of an attempted experience and observed outcome, while this exchange
was brainstorming that produced an insight.

The discussion concluded that APSS's existing concepts are sufficient if their
roles are clarified. A bounded working session is a source record in a declared
stream; observations are evidence, insights are interpretations, questions are
uncertainty, and authorized decisions are decisional artifacts. Any executable
response is separate linked work. The stream name `working-sessions` was chosen
because it describes the source plainly and can include synchronous or
asynchronous exchanges bounded by a topic or intended outcome.

## Outcomes

### Observations

- The framework already names meetings and customer threads as information
  streams and says a durable discussion summary becomes evidence.
- The framework currently groups tasks, issues, insights, questions, decisions,
  research, and experiments together as work types.
- The operations backlog applies execution states to every ready item.
- Framework feedback has a narrower report contract based on a consumer's
  context, attempted use, observed result, and desired outcome.

### Insights

- The current setup conflates source or interpretive records with executable
  responses.
- Streams should be declared around source, purpose, access, and consumption;
  insights, questions, and decisions are roles within or derived from evidence,
  not automatically separate streams.
- A retained-record convention is useful operationally but does not need to
  become another mandatory APSS primitive.

### Questions

- When should an insight, question, or decision be extracted from its source
  session into an independently managed record?
- Should issue records also be separated explicitly from remediation work in a
  later refinement?

### Decisions

- Name the stream and directory `working-sessions`.
- Define a lightweight process for framing, conducting, closing, retaining, and
  routing a working session using APSS's existing discussion/grilling
  capability.
- Narrow backlog intake and lifecycle handling to executable candidate actions.
- Retain this conversation as the first working-session record.

### Candidate actions

- Revise the normative planning guidance so retained evidence, insight,
  uncertainty, and decisional records are not mislabeled as executable work.
- Update the operations declaration, loop, intake, grooming, and documentation
  to implement the clarified boundary.
- Reclassify existing action-shaped backlog entries that currently use
  `type: insight`.

## Routing and review

The maintainer explicitly authorized the candidate actions above in the same
Codex task. They are claimed in `operations/work/LOG.md` and are being performed
as one bounded repository change. No framework-feedback report was created.

The maintainer reviewed the summary on 2026-07-10, confirmed that it accurately
represents the session, and requested delivery of the implementation. The
record is retained.

## Follow-up after review

The maintainer identified two topics for a subsequent working session:

- improve the insight stream and its intake, processing, and grilling process;
  and
- examine a potentially missing high-level framework concept for working
  sessions, including meetings, grooming, discussion, research, and related
  forms of deliberate knowledge work.

The maintainer also proposed an insight for later capture once the insight
stream and process exist: APSS can be understood as obtaining data through
streams, digesting it through processes such as grooming or grilling, planning
resulting actions such as research or discussion, and learning or compiling
through a specialized process to produce artifacts. The exact relationship
between a planned session, its retained record, ordinary execution, and
knowledge compilation remains intentionally unresolved for that later session.

This proposal remains in its source session and has not been converted into a
feedback report, insight record, or backlog commitment.

## Subsequent routing

On 2026-07-10, the maintainer requested creation of the insight stream and
process. The proposal was then extracted as
`apss.insight.evidence-deliberation-action-learning` and linked back to this
session. It remains a captured, ungroomed insight and has not become feedback,
compiled knowledge, a normative framework concept, or backlog work.
