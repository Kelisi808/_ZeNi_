# Agentic Web — Primer

> The ten-minute version of [The Agentic Web](../../AGENTIC_WEB.md).
> Same ideas, shorter reading distance.

## What changes

The web you know assumes a human at the keyboard. Pages, links, forms, search — the entire stack of conventions exists because a person was meant to read, click, and decide. APIs added a machine-callable surface on top of that pattern, but they still assumed a caller who waited for instructions.

The Agentic Web is what arrives when **the active participant is not a human and not a passive API consumer, but an autonomous agent that finds counterparts, negotiates work, executes against tools, and produces evidence on its own initiative.**

That is a different design problem.

## What the primitives have to do

A web built for agentic participants requires six primitives that today's stack either lacks or implements as accidents of the human pattern:

- **Capability discovery.** Agents need to find what is possible by what it does, not by where it lives. A registry indexed on capability, cost, and policy — not on domain name.
- **Verifiable identity.** Every actor in a consequential call needs a cryptographic chain back to the operator who initiated the work. Identity at the protocol layer, not the application layer.
- **Policy-bound invocation.** "Do this thing" is not a complete request. "Do this thing, under this budget, with this approval token, with these evidence requirements" is. The policy is the call.
- **Skill leases.** Capabilities should be leasable, not owned. A general-purpose runtime entity acquires a skill for a specific task, executes, and releases. Time-bound, scope-bound, auditable.
- **Receipts by default.** Every consequential exchange leaves a cryptographically chained receipt without the operator having to opt in. The receipt chain is the audit trail and, in the strongest version, the work product.
- **Governed model allocation.** Which model handles which phase of a multi-step workflow is a logged, auditable decision — not an implementation detail inside someone's vendor SDK.

None of these primitives are technically novel in isolation. What is missing is a coherent layer that brings them together, makes them composable, and exposes them to any compliant participant — agent, model, tool, framework — without locking the participant to a single vendor.

That layer is the Agentic Web. It is what ZéNí is building.

## Why this is urgent

Every serious software company is now building agents. Frameworks proliferate. Demos proliferate. Vendor lock-in is starting to harden. Every month that passes without consolidation primitives is a month where companies wire bespoke integrations that they will pay to undo for the next decade.

The companies that captured value in previous platform shifts — application servers, browsers, mobile SDKs, cloud — did so by building the operational layer above the commodity beneath. The model is commoditizing. The operational layer is open. The window for staking out a credible position is short.

## What this primer leaves out

The fuller [Agentic Web essay](../../AGENTIC_WEB.md) covers:

- A point-by-point comparison of human-web vs agentic-web concerns
- Where APIs help and where they stop being enough
- How protocols like MCP fit into the broader layer (see also [Why MCP matters](../../WHY_MCP_MATTERS.md))
- The economic logic of why the prize sits at the operational layer

If the primer convinced you the framing is real, the essay is worth the twenty minutes.

---

**Back to** [README](../../README.md) · **Full essay** → [AGENTIC_WEB.md](../../AGENTIC_WEB.md)
