# Context Engineering for Marketing

**Applied research, patterns and experiments for AI-native marketing and knowledge work.**

This repository studies the layer around prompts and models: the context architecture that determines what an agent knows, what it trusts, what it retrieves, and how its output is verified.

## Thesis

Marketing is a useful stress test for Context Engineering because the work depends on multiple kinds of context that should not be flattened into one prompt:

- brand strategy;
- market evidence;
- ICP and persona knowledge;
- offer logic;
- editorial rules;
- claims and proof;
- channel constraints;
- historical decisions;
- current campaign context.

The goal is not maximum context.

The goal is **minimum sufficient, authoritative context with measurable effect**.

## Research map

```text
Context sources
      ↓
Authority + boundaries
      ↓
Routing / retrieval
      ↓
Task skill
      ↓
Agent execution
      ↓
Checks + evals
      ↓
Human gate
      ↓
Artifact + provenance
```

## Repository

```text
principles/
  context-is-not-a-prompt.md
  progressive-disclosure.md
  context-quality.md

patterns/
  brand-context.md
  evidence-context.md
  market-intelligence-context.md

experiments/
  context-ablation.md
  stale-context-conflict.md

case-studies/
  knowledge-operating-system.md
  bussola.md
```

The experiments are proposed protocols. No measured results are claimed in this release. The implementation-oriented companion is [Marketing Context System](https://github.com/eusouakell/marketing-context-system).

## Questions I am testing

1. What belongs in persistent context versus task context?
2. When should knowledge be retrieved instead of injected?
3. How should agents resolve conflict between a canonical spec and a newer-looking but derived artifact?
4. When does additional context stop improving performance?
5. Which marketing controls can be deterministic?
6. Which require model judgment?
7. How should evidence and provenance travel with a claim?
8. How do skills and context interact?
9. What should trigger a human gate?

## Positioning boundary

This repository is not an attempt to recast marketing practice as software engineering.

It uses engineering ideas where they are useful — bounded contexts, provenance, deterministic checks, evals, routing and state — to make AI-assisted knowledge work more reliable.

The standard of proof is applied experimentation, not terminology.

## Start here

- [Context is not a prompt](principles/context-is-not-a-prompt.md) — the working definition.
- [Brand context](patterns/brand-context.md) and [evidence context](patterns/evidence-context.md) — reusable design patterns.
- [Knowledge operating system](case-studies/knowledge-operating-system.md) — a public architectural abstraction, excluding proprietary evidence.
- [Bússola](case-studies/bussola.md) — a collaborative agent case with explicit attribution and links to public project documentation.
- [Context ablation](experiments/context-ablation.md) and [stale-context conflict](experiments/stale-context-conflict.md) — proposed protocols, with results still to be produced.

These artifacts demonstrate how the thesis is specified. They are not evidence of a measured performance advantage. Future results should include failures as well as gains.
