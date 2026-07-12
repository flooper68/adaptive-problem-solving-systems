# APS system declaration

This document is the human-readable contract and authoring template for APS
`SYSTEM.md`. The framework definition controls APS semantics. APS deliberately
has no separate machine-readable schema while the framework is still being
polished.

The declaration is a small orientation surface:

- `name` identifies the system;
- `problem` states the condition it exists to change;
- `verification` links the process that evaluates attempts against the problem;
- `strategy` links the current direction;
- `process` links the implementation of the complete loop;
- `work_sessions` lists the bounded session types the system offers;
- `streams` declares relevant information sources.

APS does not mandate particular work-session types. Each entry has a local
`id`, description, and defining process. The array may be empty when a system
has no bounded session types. Continuous and automated processes remain in the
linked loop without artificial session declarations.

Stream entries identify their purpose, source, access method, consuming
process, and optional source-specific elicitation guidance. Their richer shape
is retained pending the separate stream-concept review.

Planning, execution, learning, participation, authority, uncertainty handling,
contextual artifacts, operating conditions, problem decomposition, and other
relationships belong in the strategies, problems, processes, verification, or
streams that own them. Systems may add fields for genuinely contextual needs,
but should not recreate removed universal fields by habit.

Declaration review confirms that:

- system names are unambiguous within the relevant scope;
- the strategy, loop process, verification, work-session process, and stream
  process references resolve;
- each work-session ID is unique within the system;
- each stream ID is unique within the system; and
- the linked process implements a complete problem-solving, verification,
  learning, and adaptation loop rather than only declaring one.

## Template

```yaml
---
name: <system-name>

problem: <condition this system exists to change>
verification: <path to the process that evaluates attempts against the problem>
strategy: STRATEGY.md
process: <path to the process that defines the complete loop>

work_sessions: [] # entries use id, description, and process

streams:
  - id: <stream-id>
    purpose: <why the system reads this stream>
    source: <native source or location>
    access: <how the evidence is captured or retrieved>
    consumed_by: <process or responsibility>
    grill: null # optional source-specific elicitation guidance
---
```

After the frontmatter, add only system-level context that is not clearer in a
linked source. A short boundary explanation may clarify why this is an
independent system. The linked process owns the complete loop; problems,
strategies, and processes own contextual decomposition and implementation
detail.

Framework Operations is the first concrete application:
[operations/SYSTEM.md](../operations/SYSTEM.md).
