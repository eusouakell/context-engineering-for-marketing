# Marketing Context Stack v1

The Marketing Context Stack is a working model for applying Context Engineering to marketing and organizational knowledge work.

It separates six responsibilities that are often mixed inside a single prompt.

## 1. Business Context

The domain knowledge the organization uses to make marketing decisions: Brand, Market, Audience, Offer, Content, Proof and Go-to-Market.

This layer answers: **What does the organization know about itself, its market, its audience and its claims?**

## 2. Knowledge Authority

Defines what is allowed to establish truth.

```text
SPEC
→ CONCEPTS
→ DECISIONS + EVIDENCE
→ VIEWS
→ APPLICATIONS
```

A website page may express positioning, but it should not silently become the source of positioning.

This layer answers: **Which source has authority, what is current, and what is only derived?**

## 3. Runtime Context

Transforms the universe of available knowledge into the context bundle for one execution.

Operations:

- **write** — persist state or useful context outside the immediate window;
- **select** — retrieve only relevant context;
- **prioritize** — favor higher-authority / higher-signal material;
- **compress** — reduce context without removing required meaning;
- **isolate** — keep irrelevant or risky context outside the call;
- **assemble** — create a task-specific context bundle;
- **refresh** — update the bundle as tools, conversation and task state change.

This is the key distinction between a knowledge base and a context system.

## 4. Execution

Task skills, agents, tools, MCP servers, deterministic utilities and generation models.

A task skill is not the same as a context system.

A skill says **how to perform a task**. The context layer determines **what the task should know and trust**.

## 5. Evaluation

### Deterministic checks
Use when a rule can be validated exactly: evidence present, source status, protected identifiers, required metadata.

### Sensors
Observe drift or risk: aging evidence, bundle growth, canonical conflicts.

### Semantic evals
Use model judgment only when the criterion is inherently semantic: positioning fit, brand voice, executive relevance, generic language.

## 6. Governance

Defines where human accountability remains required: new positioning, new public claims, ICP changes, offer architecture changes, sensitive publication and gate overrides.

## End-to-end model

```text
BUSINESS KNOWLEDGE
        ↓
AUTHORITY MODEL
        ↓
RUNTIME CONTEXT OPERATIONS
        ↓
SKILL / AGENT / TOOL
        ↓
CHECKS + EVALS
        ↓
HUMAN GATE
        ↓
ARTIFACT + PROVENANCE
```

## Design principle

The target is not maximum context.

The target is the **smallest authoritative context bundle that materially improves task performance and survives verification**.
