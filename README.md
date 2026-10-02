# Context Engineering for Marketing

**Applied research on context systems for marketing and organizational knowledge work.**

This repository studies a layer that prompts alone do not solve: how an AI system decides **what context exists, what is authoritative, what belongs in the current task, what should be excluded, and how the result is verified**.

## Working definition

> **Context Engineering for Marketing** is the design of systems that determine what an AI agent should know, retrieve, trust and use for a marketing task, and how the resulting work is verified.

Marketing is a useful stress test because a single task can depend on very different context: brand strategy, market evidence, ICP/persona knowledge, offer logic, proof and claim status, historical decisions, current task state, tool results, channel constraints and human approvals.

Flattening all of that into one prompt is not a context system.

## Marketing Context Stack

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

Read [Marketing Context Stack v1](frameworks/marketing-context-stack.md) and the [runtime context lifecycle](frameworks/runtime-context-lifecycle.md).

## Two different problems

### Knowledge authority

Where does truth live, and which source wins when sources disagree?

```text
SPEC
→ CONCEPTS
→ DECISIONS + EVIDENCE
→ VIEWS
→ APPLICATIONS
```

### Runtime context

What from the available context universe should enter this execution?

```text
AVAILABLE CONTEXT
→ VALIDATE
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

The first controlled comparison uses four conditions:

| Condition | Configuration |
|---|---|
| A | Prompt only |
| B | Prompt + full context dump |
| C | Prompt + routed context |
| D | Routed context + verification harness |

The hypothesis is deliberately falsifiable:

> Routed context should improve quality and grounding per unit of context compared with prompt-only execution and indiscriminate context dumping.

**No measured advantage is claimed until the benchmark is run.**

## What is already here

- principles for context quality and progressive disclosure;
- reusable patterns for brand, evidence, decision, market-intelligence and memory/state context;
- the Marketing Context Stack;
- experiment protocols;
- public-safe case studies;
- articles connecting brand systems and runtime context.

## Start here

- [Marketing Context Stack](frameworks/marketing-context-stack.md)
- [Runtime context lifecycle](frameworks/runtime-context-lifecycle.md)
- [Context ablation experiment](experiments/context-ablation-v01.md)
- [Knowledge operating system case](case-studies/knowledge-operating-system.md)
- [Marketing Context Stack pilot](case-studies/marketing-context-stack-pilot.md)
- [From brand manuals to runtime context](articles/from-brand-manuals-to-runtime-context.md)

## Companion implementation

The executable reference implementation lives in [Marketing Context System](https://github.com/eusouakell/marketing-context-system).

The research repo explains **why and what to test**. The implementation repo makes context selection **inspectable and executable**.

## Research posture

The goal is not maximum context.

The goal is **minimum sufficient, authoritative context with measurable effect**.

This repository distinguishes architecture, hypothesis, intervention and measured result. A documented mechanism is not evidence of model-quality improvement.

## License

Original research and documentation are available under **CC BY-NC-SA 4.0**, except where otherwise noted. See [LICENSE.md](LICENSE.md) and [NOTICE.md](NOTICE.md). Commercial reuse requires separate permission.
