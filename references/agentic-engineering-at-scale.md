# Chris Ford — Agentic Engineering at Scale

Source:
- Chris Ford, *Agentic Engineering at Scale*, O'Reilly Early Release
- https://www.oreilly.com/library/view/agentic-engineering-at/0642572344306/

Type: methodology / external reference.

## What informed this research

The work provides a useful framing for the **coding/agent harness**: the system around stochastic generation that helps encode intent, constrain behavior, inspect execution and verify outcomes.

The four-part vocabulary used in this repository — **Guides, Guards, Sensors and Checks** — is an adaptation of that harness framing to marketing, knowledge work, editorial systems and design-system workflows.

## Cereja / Context Engineering adaptation

This research applies the distinction beyond coding agents:

- Guides → task/domain/design/editorial context;
- Guards → policy, permissions, schemas, authority and pre-action constraints;
- Sensors → manifests, traces, runtime observations and human edits;
- Checks → deterministic tests, semantic evals, accessibility verification and human review.

## Boundary

This repository does not reproduce the book's figure or present the adaptation as Chris Ford's implementation.

The book is the conceptual reference. The mappings, examples and operating contracts here are the author's application to Context Engineering for Marketing & Knowledge Work.

## Cross-checks

The same broad separation is visible in current agent platforms:

- OpenAI Agents SDK: agent definitions, guardrails/human review, tracing/observability and evals;
- Anthropic: Agent Skills/context, agent harnesses, transcripts/traces and evaluation harnesses.

These are corroborating implementation patterns, not sources for the four-part terminology.
