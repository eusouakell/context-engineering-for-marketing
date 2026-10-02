# Context Engineering for Marketing

**Applied research on context systems for marketing and organizational knowledge work.**

This repository studies the layer around prompts and models: how an agent's usable context is **written, selected, prioritized, compressed, isolated, assembled and verified**.

## Working definition

> Context Engineering for Marketing is the design of systems that determine what an AI agent should know, retrieve, trust and use for a marketing task — and how the resulting work is verified.

Marketing is a useful stress test because one task may depend on different forms of context: brand strategy, market evidence, ICP and persona knowledge, offer logic, proof and claim status, historical decisions, current task state, tool results, channel constraints and human approvals.

Flattening all of that into one prompt is not a system.

## Marketing Context Stack v1

```text
┌─────────────────────────────────────┐
│ 6. GOVERNANCE                       │
│ Decisions · permissions · owners    │
├─────────────────────────────────────┤
│ 5. EVALUATION                       │
│ Checks · sensors · evals · gates    │
├─────────────────────────────────────┤
│ 4. EXECUTION                        │
│ Skills · agents · tools             │
├─────────────────────────────────────┤
│ 3. RUNTIME CONTEXT                  │
│ Select · prioritize · compress      │
│ isolate · assemble · refresh        │
├─────────────────────────────────────┤
│ 2. KNOWLEDGE AUTHORITY              │
│ Specs · evidence · decisions · state│
├─────────────────────────────────────┤
│ 1. BUSINESS CONTEXT                 │
│ Brand · market · audience · offer   │
│ content · proof · GTM               │
└─────────────────────────────────────┘
```

Read: [Marketing Context Stack v1](frameworks/marketing-context-stack.md).

## The two problems

### 1. Knowledge authority

Where is truth stored, and which source wins?

```text
SPEC
→ CONCEPTS
→ DECISIONS + EVIDENCE
→ VIEWS
→ APPLICATIONS
```

### 2. Runtime context

What from the available universe should actually enter this model call?

```text
AVAILABLE CONTEXT
→ SELECT
→ PRIORITIZE
→ COMPRESS
→ ISOLATE
→ ASSEMBLE
→ EXECUTE
→ OBSERVE
```

A knowledge architecture without runtime selection is incomplete. A runtime context strategy without source authority is fragile.

## Research program

The first benchmark compares four conditions:

| Condition | Configuration |
|---|---|
| A | Prompt only |
| B | Prompt + full context dump |
| C | Prompt + routed context |
| D | Routed context + verification harness |

The hypothesis is deliberately falsifiable:

> Routed context should improve quality / grounding per unit of context compared with both prompt-only execution and indiscriminate context dumping.

No measured advantage is claimed until the benchmark is run.

## Start here

- [Marketing Context Stack v1](frameworks/marketing-context-stack.md)
- [Runtime context lifecycle](frameworks/runtime-context-lifecycle.md)
- [Context ablation benchmark](experiments/context-ablation-v01.md)
- [Knowledge operating system case](case-studies/knowledge-operating-system.md)
- [From brand manuals to runtime context](articles/from-brand-manuals-to-runtime-context.md)

## Companion implementation

The executable reference implementation lives in [Marketing Context System](https://github.com/eusouakell/marketing-context-system).

## Principles and provenance

**The goal is not maximum context. The goal is minimum sufficient, authoritative context with measurable effect.**

The v2 stack extends the existing [principles](principles), [patterns](patterns) and [case studies](case-studies), preserving their provenance. The [pilot case study](case-studies/marketing-context-stack-pilot.md) documents the intervention, not measured model superiority.


## License

Original research and documentation are available under **CC BY-NC-SA 4.0**, except where otherwise noted. See [LICENSE.md](LICENSE.md) and [NOTICE.md](NOTICE.md). Commercial reuse requires separate permission.
