# APS system declaration contract

This document is the human-readable contract for declaring an adaptive
problem-solving system. It defines the information a declaration must make
recoverable; it does not prescribe one file, storage technology, or physical
layout. The framework definition controls APS semantics. APS deliberately has
no separate machine-readable schema while the framework is still being
polished.

## Required orientation

A system declaration is the smallest orientation surface, or set of connected
surfaces, from which a reader can find:

- the system's `name`;
- its stable root `problem`;
- its current system `strategy`;
- the `verification` process that evaluates attempts against the problem;
- the `process` that implements the complete adaptive loop;
- the bounded `work_sessions` the system offers; and
- the relevant information `streams` the loop consumes.

The declaration may colocate these parts or keep them in separate files, wiki
pages, database records, or other systems of record. When they are separate,
the orientation surface or the surrounding tool must connect them clearly.
Local field names and navigation may differ, but the APS responsibilities and
their relationships must remain recoverable.

The declared system problem is constitutive and stable for that system.
Evolving understanding or clarification belongs in the system strategy; APS
does not define a root-problem replacement transition.

Each work-session entry supplies a local identifier, a concise description,
and the process that defines the work. A system with no bounded session types
declares an empty set. Continuous and automated processes remain in the
complete loop without artificial session declarations.

Each stream entry likewise supplies a local identifier, a description of what
the stream carries — mentioning source or capture when relevant — and the
process that consumes it.

Planning, execution, learning, participation, uncertainty handling,
contextual artifacts, operating conditions, problem decomposition, and other
relationships belong in the strategies, problems, processes, verification, or
streams that own them. A system may add information for genuine contextual
needs, but should not recreate removed universal structure by habit.

## Declaration review

Review confirms that:

- the system name is unambiguous within the relevant scope;
- the root problem, strategy, verification, and complete-loop process are
  present and connected;
- every declared work session has a unique local identifier, a description,
  and a resolvable defining process;
- every declared stream has a unique local identifier, a description, and a
  resolvable consuming process; and
- the complete-loop process implements problem solving, verification,
  learning, and adaptation rather than only naming them.

## Representation profiles

These profiles show valid encodings of the contract. They are examples, not
additional framework requirements.

### Repository capsule

A repository may use one `SYSTEM.md` orientation file whose links resolve to
the other parts:

```yaml
---
name: <system-name>

problem: <condition this system exists to change>
verification: <path to the process that evaluates attempts against the problem>
strategy: <path to the current system strategy>
process: <path to the process that defines the complete loop>

work_sessions: [] # entries supply id, description, and process
streams: []       # entries supply id, description, and process
---
```

After the frontmatter, add only system-level context that is not clearer in a
linked source.

### Structured project

A project-management or orchestration system may represent the same contract
through a project name, separate problem, strategy, verification, and process
declarations, plus native work-session and stream records. The tool's project
view supplies the connecting orientation surface.

Framework Operations is the first concrete application and uses this
structured-project profile in Chaos House:
[APS Framework Operations](../problem.html).

