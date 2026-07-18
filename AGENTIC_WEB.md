# The Agentic Web

> The web was built for humans. APIs were built for callers who wait. Neither was built for agents.

## The web you know

The web you know assumes a human at the keyboard. The fundamental unit is a **page**: a static or templated document, rendered to a human eye, navigated by a human cursor. Almost everything that has made the web great — search, hyperlinks, indexing, accessibility, semantic markup — exists to make pages easier for humans to find, read, and understand.

This is not a criticism. It is the design. The human web is a triumph.

But it is not the right design for agents.

## What changes when the user is a process

An agent reading the web has different needs than a human reading the web. The differences are not subtle.

| Concern | Human web | Agentic web |
|---|---|---|
| **Primary unit** | The page | The capability |
| **Discovery** | Search engines, links | Capability registries, signed manifests |
| **Trust** | Domain reputation, HTTPS | Cryptographic attestation, scoped permissions |
| **Latency** | Acceptable seconds | Often demanded sub-second |
| **Error handling** | "Reload and try again" | Structured fallbacks, escalations, receipts |
| **Audit** | None expected | Cryptographically chained, kept by default |
| **Cost model** | Free or subscription | Per-call, per-token, per-action, per-skill-lease |
| **Authorization** | Cookies, sessions | Approval tokens, policy decisions, scoped leases |

The human web has analogues for most of these — passwords, audit logs, OAuth scopes — but they are accidents of the human pattern, not first-class primitives. An agentic web needs to make them first-class.

## What APIs got right, and where they stop

APIs were the first attempt to make the web machine-usable. They got several big things right:

- A stable contract a non-human can call.
- Authentication built in.
- A predictable response shape.

But APIs still assume:

1. **A specific caller.** "I have an API key" implies you know in advance who is going to use the API. An agent that has _just been told what to do_ does not.
2. **No internal cost discipline.** Most APIs do not surface their cost-per-call in a structured way that lets an agent decide whether to use this API or a cheaper substitute.
3. **No accountability for outcomes.** APIs report HTTP status codes. They do not produce receipts of the form "this action happened, here is the cryptographic proof, here is the chain of who authorized it."
4. **No protocol for dynamic capability composition.** When an agent needs three APIs in sequence with policy gates between each, the agent (or its operator) has to wire that orchestration up by hand.

APIs are the dial tone of the Agentic Web. They are not the Agentic Web.

## What the Agentic Web actually needs

The Agentic Web is what the web becomes when its native unit of interaction is not the page or the API call, but the **governed capability invocation**. The minimum primitives are:

### 1. Capability registries
Machine-readable directories where agents — or systems acting on behalf of agents — can be **discovered** by what they can do, not by where they live. The descriptor needs to include not just "what" but "at what cost," "under what policy," and "with what evidence guarantees."

### 2. Signed identity and attestation
Every actor in the chain — agent, tool, service, model — needs a verifiable identity. Every consequential call needs a signed timestamp, a replay-safe nonce, and a cryptographic chain back to the operator who initiated the work. Not at the application layer, where it gets re-implemented badly every time. At the protocol layer, where it can be relied on.

### 3. Policy-bound work
A capability invocation is not "do this thing." It is _"do this thing, under these constraints, with this approval token, for this budget, with these evidence requirements."_ The policy is not separate from the call. It is the call.

### 4. Skill leases over skill ownership
Specialist agents are the wrong primitive for a world where capability requirements change every workflow. The right primitive is the **skill lease**: a short-lived, governance-scoped checkout of a capability by a runtime entity for a specific task. Skills are first-class, leasable objects. Agents are general workers that compose them.

### 5. Receipts as the natural state
Audit cannot be a feature you turn on. In the Agentic Web, every consequential exchange leaves a receipt **by default**, and the receipt is the unit of truth. If there is no receipt, the action did not happen — even if the output exists.

### 6. Governed model allocation
A workflow's first phase may need a cheap fast model. Its second phase may need a stronger reasoner because the first phase produced a contradiction. The choice of which model is right for which phase needs to be a governed, logged, auditable decision — not an implementation detail buried in someone's vendor SDK.

Most of these primitives are missing from today's stack. The ones that exist — like model-context interop, identity attestation, and signed inter-service calls — are early and unconsolidated.

## Why this matters now

Two observations make this urgent:

**Agentic systems are moving from demonstrations into products.** Frameworks,
model platforms, protocol projects, and application teams are all testing how
far autonomous workflows can go. The more capability is connected through
bespoke interfaces, the more expensive it becomes to change vendors, preserve
evidence, or govern the whole workflow coherently.

**The economic value is in the layer above the model.** Models are commoditizing. The companies that captured value in the previous platform shifts — application servers, browsers, mobile SDKs, cloud — did so by building the **operational layer** above the commodity. The Agentic Web is the operational layer for AI. We are arguing that the prize sits there.

## What ZéNí builds, in this frame

If the Agentic Web is the missing layer, ZéNí is one bet on what that layer
should look like: a connected system spanning human command, machine
coordination, governance, and evidence. It is not an exhaustive answer and it is
not generally available. It is a deployed system now entering structured pilot
use with startup operators.

Read [Why ZéNí, why now](WHY_ZENI.md) for the timing argument and the positioning.

---

**Next →** [Why MCP matters](WHY_MCP_MATTERS.md) — the open standard that started turning isolated models into coordinated agents.
