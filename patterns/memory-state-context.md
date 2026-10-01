# Pattern — Memory and task state

Not every previous message belongs in the next model call.

Separate durable knowledge, user preference/memory, current task state, transient conversation detail and tool state.

Prefer explicit task-state artifacts for long-running work.

A new execution should be able to answer:

- what has been completed?
- what remains?
- what decisions are locked?
- what evidence was used?
- what must be reloaded?

This reduces dependence on raw conversation history.
