# Agentic Harness for Marketing & Knowledge Work

Status: working framework.

A context system does not become reliable merely because it retrieves good information.

An agent also needs a **harness** around generation: mechanisms that inform behavior, constrain behavior, observe what happened and verify whether the result is acceptable.

This repository uses four operating classes:

| | Before / during generation | After / around execution |
|---|---|---|
| **Descriptive** | **Guides** | **Sensors** |
| **Normative** | **Guards** | **Checks** |

The names and quadrant framing are adapted from Chris Ford's *Agentic Engineering at Scale* (O'Reilly Early Release). See [reference note](../references/agentic-engineering-at-scale.md).

## 1. Guides

**Descriptive + feedforward**

Guides help an agent understand the environment before or while it works.

Examples in marketing/knowledge work:
- canonical brand and audience context;
- domain glossaries;
- architecture and system maps;
- task examples;
- format contracts;
- design-system documentation;
- source-authority rules expressed as explanatory context;
- task-specific context bundles.

A Guide should improve orientation without pretending to enforce behavior.

### Test

Ask:

> If this artifact disappeared, would the agent mainly lose useful understanding?

If yes, it is probably a Guide.

## 2. Guards

**Normative + feedforward**

Guards constrain what the agent may do before a risky or invalid action proceeds.

Examples:
- structured input/output schemas;
- tool allowlists;
- permissions;
- confidentiality boundaries;
- maximum claim scope;
- publication permissions;
- rights constraints;
- approval required before side effects;
- explicit "do not invent evidence" rules;
- context-isolation policy.

A Guard can be deterministic, policy-driven or human-mediated.

### Test

Ask:

> Does this mechanism constrain or pause an action before its consequence is accepted?

If yes, it is probably a Guard.

## 3. Sensors

**Descriptive + feedback**

Sensors record or surface what actually happened.

Examples:
- context manifest;
- retrieved source IDs;
- source age;
- token/context payload;
- tool calls;
- handoffs;
- traces;
- runtime duration/cost;
- human edits;
- publication outcomes;
- traceability graph;
- stale/conflicting knowledge signals.

A Sensor is evidence about a run or system state. It does not automatically decide pass/fail.

### Test

Ask:

> Is this artifact primarily telling us what happened or what changed?

If yes, it is probably a Sensor.

## 4. Checks

**Normative + feedback**

Checks compare an observed result against an explicit expectation.

Examples:
- deterministic assertions;
- schema validation;
- evidence coverage checks;
- claim-to-source checks;
- semantic evals;
- channel-fit evals;
- accessibility tests;
- regression suites;
- trace graders;
- human publication review.

Checks may be binary or scored. A failed Check should have an explicit consequence: revise, block, escalate or collect more evidence.

### Test

Ask:

> Does this mechanism evaluate an observed state against a criterion?

If yes, it is probably a Check.

## Sensors are not Checks

This distinction is important.

A traceability graph showing an orphan node is a **Sensor**.

A rule stating:

> every high-impact component must trace to an approved requirement and at least one verification artifact

plus logic that fails when that rule is violated is a **Check**.

Likewise:
- recording token use = Sensor;
- enforcing a context-budget ceiling = Check;
- recording human edits = Sensor;
- scoring whether the edit rate exceeds an agreed threshold = Check.

## Guards are not Guides

A brand manual can explain how the brand behaves: Guide.

A machine-readable rule that prevents an unapproved color token from entering production: Guard.

The same source may support both, but the **operating mechanism** determines the category.

## Human authority

Human judgment can appear in more than one quadrant.

Examples:
- human approval before publishing a sensitive claim = Guard;
- human review of a finished newsletter against editorial criteria = Check;
- human edits recorded for learn-back = Sensor.

"Human in the loop" is therefore not one control type.

## End-to-end operating model

```text
KNOWLEDGE AUTHORITY
        ↓
RUNTIME CONTEXT
        ↓
GUIDES + GUARDS
        ↓
AGENT / SKILL / TOOL
        ↓
SENSORS
        ↓
CHECKS
        ↓
HUMAN DECISION WHEN REQUIRED
        ↓
ARTIFACT + PROVENANCE + LEARN-BACK
```

The arrows are not strictly linear. Sensors can emit during execution and Guards can pause tool calls. The diagram describes responsibility, not a synchronous implementation requirement.

## Relation to Context Engineering

Context Engineering answers:

> What should this execution know, retrieve, trust and use?

Harness Engineering adds:

> What constrains the execution, what do we observe, and how do we know whether the result is acceptable?

The two systems overlap but should not be collapsed.

A context bundle is usually a Guide.

The authority and isolation rules deciding what may enter that bundle are Guards.

The context manifest describing what was actually loaded is a Sensor.

A test verifying that all required authoritative domains were present is a Check.

## Implementation maturity

A documented quadrant is not evidence that it works.

For each mechanism, record:

- **status** — proposed / implemented / automated / validated;
- **owner**;
- **input**;
- **output or signal**;
- **failure consequence**;
- **evidence of effectiveness**, when available.

This prevents diagrams from overstating operational maturity.

## External alignment

This framework is not tied to one model provider.

OpenAI's current Agents SDK separates agent definitions, tools/handoffs, guardrails/human review, tracing/observability and evals. Anthropic similarly distinguishes agent/skill context, agent harnesses, traces/transcripts and evaluation harnesses.

Those implementations are useful cross-checks, but this model remains provider-neutral.
