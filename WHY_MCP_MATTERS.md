# Why MCP matters

> Of every open standard published in the last three years, Model Context Protocol is the one that quietly changed the most. Most people still haven't noticed.

## What MCP is

The **Model Context Protocol (MCP)** is an open standard that defines how language models talk to the world outside themselves — to tools, to data, to other systems, to other models.

Before MCP, every AI integration was a bespoke wiring job. Each vendor invented its own way for the model to call a search engine, read a file, send an email, or query a database. Switching models meant rewriting the wiring. Switching vendors meant rewriting twice. Composing multiple models in one workflow meant rewriting forever.

MCP collapses that into a single protocol: a stable, model-agnostic way to expose a **capability** (a tool, a resource, a data source) to any model that speaks the protocol. Once a system implements MCP, every MCP-compliant model can use it. Once a model speaks MCP, it can consume every MCP-compliant capability.

In one diagram:

```
   Before MCP                          With MCP
   ───────────                         ─────────
                                        ┌───────────┐
   Model A ─── Wiring ─── Tool 1        │           │
   Model A ─── Wiring ─── Tool 2        │   Model A │──┐
   Model A ─── Wiring ─── Tool 3        │           │  │
                                        │   Model B │──┤
   Model B ─── Wiring ─── Tool 1        │           │  │   ┌───────────────┐
   Model B ─── Wiring ─── Tool 2        │   Model C │──┼───┤   MCP layer   │── Tool 1, 2, 3, ...
   Model B ─── Wiring ─── Tool 3        │           │  │   └───────────────┘
                                        │   Model D │──┘
   ...n × m custom wirings...           │           │
                                        └───────────┘
```

The n×m integration problem becomes n+m. That is not a small improvement. That is the difference between an industry that can compose and an industry that cannot.

---

## Why MCP matters more than any single model

It is tempting to evaluate AI progress by looking at which model is currently winning the benchmarks. That measure is misleading. Benchmark leadership rotates every few months. The protocol layer underneath does not.

When the railroads were being built, the people who got rich were not the ones who built the first locomotive. They were the ones who **set the gauge.** Standardize the rails, and every train that has ever been built or will ever be built can run on them. Pick the wrong gauge, and your equipment is permanently isolated.

MCP is the gauge. Anthropic published it as an open standard for a reason: a protocol's value is its adoption, not its ownership. The more systems speak MCP, the more valuable speaking MCP becomes for the next system. We are in the early innings of that flywheel.

This is why a venture's relationship to MCP is, in 2026, a more useful signal of long-term defensibility than its model choice. The model choice will change three times in five years. The protocol choice compounds.

---

## What MCP gets right

Three design choices put MCP on the right side of the durability question:

1. **Open by default.** No central owner. No license trap. Vendors implement it because it's strictly better than the alternative, not because they have to.
2. **Server-side capabilities, client-side models.** The capability provider exposes a stable surface. The model is the consumer. Capabilities outlive models. Designing the protocol around the slower-moving side is the right choice.
3. **Composable, not hierarchical.** A capability can itself consume other capabilities via MCP. An agentic workflow becomes a directed graph of capability calls, each one independently inspectable.

---

## What MCP, deliberately, does not solve

MCP is a transport-and-shape protocol. It says how a model and a capability **talk**. It does not say:

- _Who is allowed to invoke this capability right now?_  (Authorization is not in scope.)
- _How are exchanges audited at the policy level?_  (Evidence is not in scope.)
- _How do agents discover capabilities they have never used before?_  (Registry is not in scope.)
- _How is the cost of a capability invocation reconciled against an operator's budget?_  (Cost governance is not in scope.)
- _Which model should answer which phase of a multi-phase workflow, and how is the handoff packaged?_  (Allocation is not in scope.)

This is not a flaw. A protocol that tried to solve all of those would have been too opinionated to adopt. MCP chose its scope well.

But it does mean: **MCP is necessary and not sufficient.** Around MCP you need a coordination layer that handles discovery, policy, evidence, and allocation. Without that layer, MCP gives you a great pipe and no operating system.

That coordination layer is the Agentic Web problem. (See [The Agentic Web](AGENTIC_WEB.md).)

---

## Why this matters for the next decade

A protocol's value compounds with its adoption. The more systems speak MCP, the more valuable speaking MCP becomes for the next system. The flywheel has started. The question now is what gets built **around** MCP — the registries, the trust layers, the evidence chains, the policy substrates — and who builds them.

That layer of build-out is where the next platform shift happens.

A venture's relationship to MCP is, in 2026, a more useful signal of long-term thinking than its model choice. The model choice will change three or four times in five years. The protocol choice compounds.

ZéNí treats MCP as a real interop surface, not as branding. We are building toward a coordination layer where any compliant model and any compliant capability can participate — without locking participants to a specific vendor's orchestrator, a specific cloud's runtime, or a specific framework's opinion about what an agent is.

The protocol layer is open. The layer above it is the prize.

---

**Next →** [Why ZéNí, why now](WHY_ZENI.md) — the timing argument and the positioning.
