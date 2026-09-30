# Case study — Bússola

Bússola was built for the **Batalha de Agentes — Itaú × Google** hackathon.

The original technical repository and implementation were led by **Victor Lopes (`theguitarvity`)**. Kell participated in the hackathon team and contributed to strategy, context, research, Responsible AI, narrative and shared project materials. Her GitHub fork is treated as a collaborative artifact, not as a claim of sole technical authorship.

## Why the case matters for Context Engineering

The agent could not operate from one undifferentiated prompt.

Its behavior depended on distinct context layers:

```text
User goal
↓
Financial-health context
↓
Known vs inferred data
↓
Scenario / deterministic calculations
↓
Product and policy knowledge
↓
Regulatory RAG
↓
Consent and action scope
↓
Agent response / tool action
↓
Trace and follow-up
```

Important boundaries included:

- demographic information could not be inferred from missing data;
- deterministic financial calculations should not be delegated to free-form model reasoning;
- future regulation should not be presented as current;
- product actions required consent;
- recommendation context and action context had to remain separable;
- provenance and confidence mattered.

That makes Bússola useful as an applied agent-context case even though the software implementation itself was collaborative.

## Public evidence and limits

See the collaborative artifact's [architecture](https://github.com/eusouakell/bussola/blob/main/docs/arquitetura.md), [scope](https://github.com/eusouakell/bussola/blob/main/docs/escopo-decisoes.md) and [constitution](https://github.com/eusouakell/bussola/blob/main/.specify/memory/constitution.md). These document design constraints; no measured context-engineering improvement is claimed here.
