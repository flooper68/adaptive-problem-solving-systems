# Intake

Intake preserves an observation faithfully before deciding what it means or what work follows.

1. Identify the declared stream and source. Conversation is not captured automatically; the owner must authorize the capture scope.
2. Preserve the source claim, context, evidence or recoverable reference, scope, uncertainty, and any requested clarification without upgrading it into a requirement.
3. Present the exact proposed record and stream. On approval, call `capture_record` session-bound.
4. Link an originating task, session, or problem when the available action surface supports it; otherwise preserve the authoritative reference in the record.
5. Leave interpretation and disposition to grooming. Capture never silently creates a problem, task, decision, or compiled knowledge.

The record is durable when Chaos House accepts it. Repository backup follows asynchronously and is not a second intake destination.
