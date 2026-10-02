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

## 5. Agentic Harness

The harness separates four responsibilities around execution:

| | Feedforward | Feedback |
|---|---|---|
| **Descriptive** | **Guides** — context, examples, architecture, format contracts | **Sensors** — traces, manifests, drift/runtime observations |
| **Normative** | **Guards** — permissions, schemas, policy and pre-action constraints | **Checks** — assertions, evals, tests and review criteria |

This prevents several common category errors:

- documentation does not become enforcement merely because an agent can read it;
- observability does not become validation merely because a problem is visible;
- semantic evals do not replace deterministic checks;
- human approval can act as a Guard or Check depending on where it sits in the workflow.

See [Agentic Harness for Marketing & Knowledge Work](agentic-harness.md).

## 6. Governance

Defines ownership, accountability and escalation across the harness: who can change Guides/Guards, who owns Sensors/Checks, and where explicit human authority remains required.

Examples include new positioning, new public claims, ICP changes, offer architecture changes, sensitive publication and control overrides.

## End-to-end model

```text
BUSINESS KNOWLEDGE
        ↓
AUTHORITY MODEL
        ↓
RUNTIME CONTEXT OPERATIONS
        ↓
GUIDES + GUARDS
        ↓
SKILL / AGENT / TOOL
        ↓
SENSORS
        ↓
CHECKS
        ↓
HUMAN DECISION WHEN REQUIRED
        ↓
ARTIFACT + PROVENANCE + LEARN-BACK
```

## Design principle

The target is not maximum context.

The target is the **smallest authoritative context bundle that materially improves task performance and survives verification**.
