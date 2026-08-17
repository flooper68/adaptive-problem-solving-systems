# APS system declaration

This document is the human-readable contract and authoring template for APS
`SYSTEM.md`. The framework definition controls APS semantics. APS deliberately
has no separate machine-readable schema while the framework is still being
polished.

The declaration is a small orientation surface:

- `name` identifies the system;
- `problem` states the root condition it exists to change;
- `verification` links the process that evaluates attempts against the problem;
- `strategy` links the current approach to solving that root problem;
- `process` links the implementation of the complete loop;
- `work_sessions` lists the bounded session types the system offers;
- `streams` declares relevant information sources.

The declared `problem` is constitutive and stable for that system. Evolving
understanding or clarification belongs in the linked strategy; APS does not
define a root-problem replacement transition.

APS does not mandate particular work-session types. Each entry has a local
`id`, description, and defining process. The array may be empty when a system
has no bounded session types. Continuous and automated processes remain in the
linked loop without artificial session declarations.

Stream entries have the same shape as work-session entries: a local `id`, a
`description` of what the stream carries — mentioning source or capture
method when relevant — and the `process` that consumes it.

Planning, execution, learning, participation, uncertainty handling,
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
    description: <what the stream carries, with source or capture when relevant>
    process: <path to the process that consumes what the stream carries>
---
```

After the frontmatter, add only system-level context that is not clearer in a
linked source. The linked process owns the complete loop; problems, strategies,
and processes own contextual decomposition and implementation detail.

Framework Operations is the first concrete application:
[operations/SYSTEM.md](../operations/SYSTEM.md).
