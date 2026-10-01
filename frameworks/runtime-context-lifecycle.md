# Runtime context lifecycle

A context system should make runtime selection explicit.

## Available universe

Potential sources include canonical knowledge, evidence, decisions, task state, conversation state, memory, retrieved documents, tool outputs, external research and examples.

Not all of them belong in every call.

## Lifecycle

### 1. Write
Persist information that should survive outside the current model call.

### 2. Select
Retrieve candidate context relevant to the task.

### 3. Prioritize
Rank context using authority, relevance, freshness, evidence status and task dependency.

### 4. Compress
Reduce low-value token usage while preserving information required for the task.

### 5. Isolate
Keep context out of the current call when it belongs to another domain, is stale/superseded, is confidential and unnecessary, belongs to another tool/sub-agent, or costs more context than it is expected to return in value.

### 6. Assemble
Create a context bundle with explicit provenance.

### 7. Execute
Run the task skill / agent.

### 8. Observe and refresh
Tool outputs, decisions and task progress can change what should be loaded next.

Context Engineering is therefore iterative, not a one-time prompt assembly step.
