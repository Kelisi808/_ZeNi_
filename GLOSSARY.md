# Glossary

A working vocabulary for the Agentic Web and the systems that surround it. Definitions here are written to be educational and portable — they apply across the industry, not just to ZéNí.

Terms are ordered conceptually rather than alphabetically, so a reader can move through them as a connected story.

---

## Agentic AI

A class of AI systems whose primary mode of work is **taking action**, not generating responses. An agentic system is given a goal, decomposes it into intermediate steps, decides which tools or counterparts to involve, executes the steps, monitors outcomes, and produces an auditable record of what it did.

The boundary between a sophisticated chatbot and an agentic system is the presence of **autonomous decision-making over multi-step work**. A chatbot completes a turn. An agent completes a workflow.

→ Deep dive: [Agentic AI](AGENTIC_AI.md)

## Agent

A unit that can be assigned a goal it did not ask for, decide on its own intermediate steps, and produce auditable outcomes. The simplest agent is a single model wrapped in a runtime loop. The most complex agent is itself a coordinated team of sub-agents.

An agent is defined by what it can be **held to**, not by what it can produce. Outputs without accountability are not agentic work.

## Agentic Web

The condition the web takes on once its native unit of interaction is no longer the page or the API call, but the **governed capability invocation**. In the Agentic Web, the primary participants are not human readers but autonomous systems that discover each other, negotiate work, and leave receipts.

The Agentic Web is not a single product, a single protocol, or a single company. It is a layer of infrastructure that is currently being assembled across many efforts.

→ Deep dive: [The Agentic Web](AGENTIC_WEB.md)

## Coordination

The set of activities required for multiple agents (or agents and tools, or agents and humans) to work together on a shared goal. Coordination includes discovery (who is available), routing (who gets the work), authorization (who is allowed), accountability (what happened), and escalation (when to stop).

Coordination is the **bottleneck of the agentic era**. Models are commoditizing; coordination is not.

## Operable intelligence

Intelligence that can be deployed, supervised, audited, and corrected in real work. The phrase distinguishes itself from "raw" intelligence — a model that can produce impressive outputs in isolation but cannot be safely integrated into a production environment without bespoke wrapping.

The thesis of ZéNí is that the next decade of value in AI moves to the systems that make intelligence operable.

## Orchestration

The act of sequencing and combining capabilities — multiple agents, multiple tools, multiple models, multiple policy gates — into a single coherent workflow. Orchestration is the mechanical part of coordination.

A pure orchestrator decides what runs and in what order. A coordination layer is broader; orchestration is one of its components.

## Trust layer

A horizontal infrastructure component whose job is to make claims about a system's behavior **verifiable**. A trust layer answers questions like: did this agent actually execute this action? Was it authorized? Are the receipts genuine? Have they been tampered with?

Trust layers replace the social construct of "we believe the vendor" with the engineering construct of "here is the cryptographic chain that proves it."

## Governance

The set of policies and controls that determine what an agentic system is allowed to do, by whom, under what conditions, with what evidence requirements. Governance is the place where business rules, legal requirements, and operational risk live.

Governance is not a feature you bolt onto an agentic system after it ships. It is a property the system either has structurally or does not.

## Evidence

The record produced by an agentic system that documents what happened in a way an external party can verify. Evidence is more than a log. A log is unstructured and operator-readable. Evidence is structured, cryptographically chained, machine-verifiable, and intended for an external audience — auditors, regulators, partners, internal reviewers.

In ZéNí's worldview, **the evidence is the work product**.

## Human oversight

The capacity for a human operator to inspect, intervene in, redirect, or halt an agentic system at any point in its execution. Human oversight is not a button on the UI; it is a property of how the system was designed. An agentic system that cannot be inspected mid-flight does not have meaningful human oversight, regardless of what the marketing material says.

## Receipt

A single auditable record of one consequential event in an agentic workflow. Receipts have a common shape but vary by kind: a routing decision, a skill checkout, an execution, a model selection, an outcome.

The receipt chain — the ordered set of receipts produced over a workflow's lifetime — is the audit trail that allows replay, compliance verification, and post-hoc reasoning about what happened.

## MCP — Model Context Protocol

An open protocol for connecting AI applications to external systems. An MCP
host establishes client connections to servers that expose capabilities such as
tools, resources, and reusable prompts through a common interaction boundary.

MCP can reduce repeated application-to-capability integration without deciding
the business authorization, routing, evidence, or learning policy around that
connection.

→ Deep dive: [Why MCP matters](WHY_MCP_MATTERS.md)

## Capability

A unit of functionality that an agent can invoke. A capability can be a tool (send an email), a data source (query a CRM), a sub-agent (a specialist that handles a particular kind of analysis), or a service (transcribe an audio file).

In the Agentic Web, capabilities are first-class objects with their own descriptors, policies, costs, and evidence requirements. They are not buried inside an application; they are discoverable across an entire ecosystem.

## Intent

The structured description of what an operator wants to happen. A well-formed intent specifies the goal, the constraints, the risk tier, the allowed counterparts, the evidence requirements, and the approval surface. Intent is the input to the coordination layer; receipts are the output.

The translation from natural-language ask to structured intent is itself an act of work, performed by an intake agent or equivalent.

## Skill lease

A temporary, governance-bound checkout of a capability by an agent for a specific task. A skill lease has a start time, an end time, a budget, a policy context, and an issuing authority. When the lease expires, the capability returns to the pool.

Skill leases are the right primitive for a world where the set of capabilities an agent needs changes every workflow. They replace the alternative of "permanent specialization" — where every agent is locked to a fixed set of capabilities — with a more flexible composition.

## Approval token

A one-time-use authorization for an action whose risk level requires explicit operator consent. An approval token is issued by an operator (or by a delegated authority), bound to a specific action, scoped in time, and recorded in the evidence chain. An agent presenting an approval token can perform the action; an agent without one is blocked.

Approval tokens are how high-risk agentic work becomes auditable and reversible: the action either has a token in its receipt chain or it did not happen.

## Policy decision

A structured determination by the coordination layer about whether an action is permitted, denied, or requires approval. A policy decision is itself a receipt. It carries the rule that fired, the inputs that led to the decision, and the consequence.

## Governed model allocation

The set of mechanics by which a coordination layer chooses **which model** answers which phase of a multi-step workflow. Different phases need different model strengths (cost-efficient for routine intake, strong-reasoning for synthesis, careful for review). Governed model allocation makes that choice a logged, auditable event rather than an opaque implementation detail.

---

**Back to** [README](README.md) · **Manifesto →** [MANIFESTO.md](MANIFESTO.md)
