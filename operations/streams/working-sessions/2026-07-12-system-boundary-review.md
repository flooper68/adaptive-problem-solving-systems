---
id: apss.session.system-boundary-review
type: working-session
status: active
recorded: 2026-07-12
participants: [APS framework maintainer, Codex operator]
source: Maintainer-agent discussion in the current Codex task
related_problems: [P1]
related_tasks: [apss.review-system-boundary]
---

# Review the system boundary concept

## Frame

Give system boundary the smallest clear meaning and role needed by the complete
loop. The responsible consumer is a person defining or interpreting an APS
system. A useful stopping point is one reviewed disposition propagated through
the normative framework and Framework Operations, with authority and subsystem
questions left to their own downstream reviews.

## Current sources and interpretation

- The normative [system-problem definition](../../../framework/VOCABULARY.md#system-problem)
  says the stable root problem defines the system's problem-owning boundary.
- The [system definition](../../../framework/README.md#system-and-subsystem)
  says loop ownership does not require every action or approval to reside
  inside the system boundary; processes assign participation and authority.
- The same framework section distinguishes a child system from an internal
  problem by independent problem and loop ownership, while current wording
  also refers to an independent boundary.
- The [declaration contract](../../../framework/SCHEMA.md) does not require a
  boundary field. It permits a short boundary explanation only when needed to
  explain why the declared unit is independently useful.
- [Framework Operations](../../SYSTEM.md#boundary) uses a local boundary section
  to distinguish the operating system, its framework output, the containing
  repository, and external APS applications.

Current interpretation: the framework does not yet define system boundary as
an independent vocabulary concept, durable object, or declaration field.
Instead, boundary language currently explains three related distinctions:
which root problem and loop the system owns; when decomposed work becomes a
child system; and what a concrete implementation includes or excludes. The
review must determine whether those distinctions need one additional normative
concept or can remain consequences of already retained concepts plus optional
application-specific explanation.

## Maintainer interpretation

After reading the current sources, the maintainer did not recognize system
boundary as a first-class concept and instead understood it as contextual
description. This supports demoting the term rather than defining another APS
primitive: the system problem and complete-loop ownership establish system
identity, while a concrete declaration may describe relevant inclusions and
exclusions for orientation.

The remaining wording question is whether references to an "independent
boundary" incorrectly make the description sound like an additional criterion
for child-system identity. The existing retained criteria can state the
distinction directly: a decomposed problem becomes a child system when it is
given its own root problem and complete problem-solving loop.

The maintainer reviewed the two normative child-system passages and found the
existing wording acceptable. In context, "independent boundary" is useful
descriptive shorthand alongside complete-loop ownership; it does not require a
separate vocabulary entry, declaration field, identity, state, or lifecycle.

The maintainer then found no remaining value in the declaration contract's
invitation to add a boundary explanation or in Framework Operations' concrete
boundary section. The Operations prose duplicated the root repository README,
which already explains the normative framework, the first application, and the
repository-container distinction. The optional schema guidance could make a
contextual description appear expected or first-class. The maintainer directed
that both be removed.

## Current stopping point

The proposed disposition is **demote**: keep boundary as ordinary contextual
description, not a first-class normative concept. The declaration-specific
guidance and duplicated Operations section are removed; existing descriptive
child-system wording remains. The changelog records the normative decision.
Immediate validation confirms that the Operations declaration retains every
required field; all declared strategy, loop, verification, work-session, and
stream process paths resolve; the selected task references P1; the root README
retains the removed repository-orientation information; current terminology
requires neither a boundary field nor a standalone vocabulary concept; and
`git diff --check` passes. The uncommitted proposal is awaiting maintainer
review.
