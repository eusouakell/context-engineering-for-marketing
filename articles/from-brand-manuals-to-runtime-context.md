# From brand manuals to runtime context: what changes when marketing work becomes agentic

A brand manual was designed for a person.

A person can skim it, interpret hierarchy, remember what changed last quarter, notice when two pages conflict, ask a colleague which version is current, and decide that a campaign example should not override the official positioning.

An AI agent does not inherit that organizational judgment automatically.

Giving an agent the brand manual is therefore not the same as giving it reliable brand context.

## The hidden problem is authority

Marketing organizations accumulate documents continuously: brand manuals, campaign decks, personas, sales presentations, research, competitive intelligence, case studies, website copy, executive messages and old “final” files.

When an agent can retrieve all of them, access improves. Authority does not.

Which file defines the current positioning? Is a website page a source of truth or an application of the source of truth? Can an analyst report validate a market problem without becoming proof that the company can solve it? Does a newer timestamp mean a document is more authoritative?

These are context questions before they are writing questions.

## Knowledge architecture is necessary, but not sufficient

One response is to organize knowledge more rigorously.

```text
SPEC
→ CONCEPTS
→ DECISIONS + EVIDENCE
→ VIEWS
→ APPLICATIONS
```

A spec describes current truth. A decision records why something changed. Evidence supports a claim. A view translates canonical knowledge for human consumption. An application uses the knowledge in a channel.

That structure reduces ambiguity.

But an agent still faces a runtime problem:

> Of everything available, what should enter this task now?

## Runtime context is a selection problem

A context system needs operations beyond storage.

It needs to select relevant sources, prioritize authority, compress low-value material, isolate irrelevant or risky context, assemble a task-specific bundle and refresh that bundle as state and tool outputs change.

This is where Context Engineering becomes distinct from simply maintaining a good knowledge base.

The agent should not receive an entire company wiki every time it writes a LinkedIn post. It should receive the smallest set of high-signal context that is sufficient for the task.

## Marketing makes the trade-offs visible

Consider an executive article about AI agents in banking.

A useful bundle may require current company positioning, the intended executive audience, current evidence, editorial rules, claim/proof constraints and a task skill.

It probably does not require every past campaign, all personas, old decks, every vendor document or unrelated market research.

The exclusion decision matters as much as retrieval.

## Verification closes the loop

Even a well-routed context bundle does not guarantee a correct artifact.

Different controls are useful for different failure modes.

Use deterministic checks for questions such as: does this public claim have evidence? Is this source superseded? Is a protected client identifier present?

Use semantic evals for questions such as: does this preserve the positioning? Is the language generic? Is the argument useful for the intended executive?

Use a human gate where accountability should not be delegated: changing positioning, introducing a new public claim, redefining an ICP or publishing sensitive evidence.

## A falsifiable thesis

The useful question is not whether “Context Engineering sounds better than Prompt Engineering.”

The useful question is whether a context system produces measurable improvement.

A simple experiment can compare prompt only, full context dump, routed context and routed context plus verification. Then measure task quality, unsupported claims, source-authority errors, revision count and token cost.

If routed context does not improve the trade-off, the system needs to change.

That is the standard I find more useful for Context Engineering in marketing: not more terminology, but more inspectable decisions and better evidence about what the context actually changed.

## References

- Anthropic — Effective context engineering for AI agents  
  https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
- LangChain — Context Engineering  
  https://www.langchain.com/blog/context-engineering-for-agents
- OpenAI Cookbook — Context Engineering: Short-Term Memory Management with Sessions  
  https://developers.openai.com/cookbook/examples/agents_sdk/session_memory
