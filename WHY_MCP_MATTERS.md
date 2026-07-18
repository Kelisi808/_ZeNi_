# Why MCP matters

> MCP standardizes connection. It does not make a connected system trustworthy
> by itself.

## What MCP is

The **Model Context Protocol (MCP)** is an open protocol for connecting AI
applications to external systems. An MCP host can establish client connections
to servers that expose capabilities such as tools, resources, and reusable
prompts through a common protocol.

That distinction matters. MCP is not a model, an agent framework, or a universal
registry. It is a standardized interaction boundary between an AI application
and the systems it can use.

Official references:

- [Introduction](https://modelcontextprotocol.io/docs/getting-started/intro)
- [Architecture](https://modelcontextprotocol.io/docs/learn/architecture)
- [Specification](https://modelcontextprotocol.io/specification/)
- [Governance](https://modelcontextprotocol.io/community/governance)

## The integration problem it improves

Without a shared protocol, every application-to-capability connection risks
becoming bespoke. A search tool, document store, database, or internal service
may need a different adapter for every host.

MCP creates a reusable boundary:

```text
AI application / host
        │
        ├── MCP client ── MCP server ── tools
        ├── MCP client ── MCP server ── resources
        └── MCP client ── MCP server ── prompts and workflows
```

Servers can describe what they support. Clients and servers negotiate
capabilities. Hosts retain control over connection, consent, and how exposed
capabilities are presented to a model or user.

This reduces repeated integration work and makes capability providers less
dependent on one model vendor's private interface.

## What MCP gets right

### A shared boundary

Capability providers can expose a consistent protocol instead of rebuilding
their interface for every AI application.

### A host-controlled architecture

The host coordinates client connections and the user experience. A model does
not become an unbounded network actor merely because an MCP server exists.

### Explicit capability negotiation

Clients and servers can identify supported features rather than assuming every
participant implements the same surface.

### An evolving open ecosystem

The specification, SDKs, and governance process are public. Implementations can
improve without tying the protocol's value to a single model release.

## What MCP does not solve for ZéNí

MCP standardizes communication. A production operating layer still has to
answer questions outside that boundary:

- Which capability should receive this mission?
- Is the requesting actor allowed to use it now?
- What budget, risk, and approval limits apply?
- Which model should handle each phase?
- What evidence proves the route, action, and outcome?
- How should failures, revisions, and cleanup be represented?
- What may a later mission learn from this one?

Those are coordination and governance responsibilities. Treating MCP as if it
solves them would weaken both the protocol and the systems built around it.

## Why it matters to ZéNí

ZéNí is designed to remain model- and capability-agnostic at the connection
layer. MCP is one important way to make that boundary real.

PitStop gives the operator a legible command surface. SideQuest coordinates
machine-facing capabilities and records outcomes. ZéNí preserves policy,
evidence, readiness, and learning boundaries across the loop. MCP helps those
surfaces connect to an open capability ecosystem without turning one vendor's
SDK into the architecture.

The protocol is the connection. The governed operating loop is the product.

---

**Back to** [README](README.md) · **Read next →**
[Why ZéNí, why now](WHY_ZENI.md)
