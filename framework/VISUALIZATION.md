# Visualizing APS

System declarations and their linked strategies, problems, processes, and
streams are the sources of truth. Visualizations are derived projections for
orientation, diagnosis, and improvement. Correct them whenever they conflict
with those sources.

No single diagram should show every relationship. APS uses four standard
views plus a repeatable local-system motif.

## 1. Problem decomposition

Purpose: answer “how has the root system problem been decomposed, and which
smaller problems have been delegated to child systems?”

Derive within-system edges from whatever decomposition relationships the
system's process declares. Derive child-system edges from delegation links in
problem definitions, strategies, or processes. Keep the first view to roughly
six to eight nodes, then allow readers to zoom into a selected problem branch.

```mermaid
flowchart TB
    root["System problem + strategy"]
    delivery["Delivery problem + strategy"]
    quality["Quality problem + strategy"]
    devLoop["Development-loop problem + strategy"]
    child["Child system\nroot problem + strategy"]

    root --> delivery
    root --> quality
    delivery --> devLoop
    quality -.->|"delegated"| child
```

Node labels name the problem and may include the owning system where needed.
Edges identify decomposition; delegated edges identify child-system ownership.
Detail views may add relevant verification signals; do not fill the orientation
map with unrelated streams and process detail.

## 2. Contextual artifact flow

Purpose: when the solution produces artifacts, answer “how do they contribute
to problem improvement, and who uses them?”

Use producer-to-consumer edges labeled with the artifact. Include outcome
feedback when it materially closes the loop.

```mermaid
flowchart LR
    direction["Direction\nartifact: system problem and strategy"]
    planning["Planning\nartifacts: problem and task state"]
    delivery["Delivery\nartifact: completed output"]
    consumer["Consumer"]
    learning["Outcome learning\nartifact: validated insight"]

    direction -->|"current direction"| planning
    planning -->|"selected tasks"| delivery
    delivery -->|"primary artifact"| consumer
    consumer -.->|"use and feedback"| learning
    learning -->|"strategy evidence"| direction
```

Use this view only when artifacts materially help explain the solution.

## 3. Evidence, compilation, and adaptation

Purpose: answer “how does this system learn, and where does that learning
change future operation?”

Show raw streams, compilation, knowledge artifacts, adaptation authority, and
the target process or strategy. Use it during maintenance and redesign rather
than as the first view for newcomers.

```mermaid
flowchart LR
    streams["Raw evidence streams"] --> compiler["Compilation process"]
    compiler --> knowledge["Compiled knowledge artifact"]
    knowledge --> proposal["Adaptation proposal"]
    proposal --> approval["Declared approver"]
    approval --> strategy["Strategy / process / subsystem change"]
    strategy --> nextRun["Next execution"]
    nextRun --> streams
```

## 4. Stream, work-session, and artifact processing

Purpose: answer “which bounded work processes which inputs, and what does it
produce?”

Show streams and existing artifacts as inputs to work sessions, with their
authoritative outputs and retained session records. Use this view to distinguish
the sessions from their evidence sources and current-state artifacts.

```mermaid
flowchart LR
    inputStreams["Input streams"] --> brainstorming["Brainstorming"]
    knowledge["Compiled knowledge"] --> brainstorming
    brainstorming --> artifact["Reviewable knowledge or instantiation changes"]
    artifact --> review["Iterative user review"]
    review --> brainstorming

    inputStreams --> grooming["Problem grooming"]
    problems["Active problem state"] --> grooming
    tasks["Current task state"] --> grooming
    grooming --> problems
    grooming --> tasks
    grooming --> session["Working-session record"]
```

The system declaration and same-named process remain the source of truth.

## Local-system motif

Every system can be understood through the same compact model:

```mermaid
flowchart LR
    problem["System problem + strategy"] --> openProblem["Smaller problem + strategy"]
    openProblem --> smallerProblem["Further decomposed problem + strategy"]
    smallerProblem --> process["Adaptive execution loop"]
    process --> attempt["Solution attempt"]
    attempt --> verification["Verification"]
    verification --> learning["Evidence → knowledge → adaptation"]
    learning --> problem
    learning --> openProblem
    learning --> smallerProblem
```

## Generation contract

A generator derives the views from the minimal declaration and its linked
sources. It should follow the human-readable [declaration contract](SCHEMA.md)
rather than maintaining a second required-field list:

| View | Fields |
|---|---|
| Problem decomposition | System problem, system-defined problem relationships and strategies, plus child-system links in problems, strategies, or processes |
| Artifact flow | Contextual artifacts and consumers named by the linked processes or problems |
| Learning | `process`, `streams`, and linked learning or adaptation sources |
| Work-session processing | `work_sessions.*`, `streams`, and linked processes |

It should also report structural problems:

- ambiguous system names within the mapped scope;
- unresolved problem-decomposition targets;
- decomposition cycles that are not deliberately modeled feedback;
- systems missing required APS fields;
- unresolved strategy, loop, verification, work-session, or stream process
  references;
- duplicate work-session or stream IDs;
- linked loop processes that omit verification, learning, or adaptation; and
- declarations that reference nonexistent local files.

The generated output is disposable. Never edit generated maps as if they were
the system definition.

## Visual discipline

- Start with the smallest useful view; reveal detail by branch or system.
- Use system names and problem labels, not folder paths, as visible text.
- Pair edge labels with line styles; do not rely on color alone.
- Keep problem-decomposition edges visually distinct from artifact, evidence,
  and governance relationships.
- A diagram with no verification or feedback edge is a prompt to check whether
  the declared loop is actually closed.
