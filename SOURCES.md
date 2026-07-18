# Sources and Further Reading

This repository is an editorial artifact. The essays advance a thesis but they do not exist in isolation — they sit on top of an open ecosystem of standards, documentation, and prior work. The sources below are the ones we consider load-bearing for a reader who wants to verify, extend, or argue with the arguments in this repository.

We deliberately keep this list short. The goal is to point at the few sources a curious reader should actually read, not to demonstrate familiarity with everything published.

---

## Model Context Protocol (MCP)

MCP appears throughout this repository because it is an important open
connection boundary for AI applications. If you read only one set of primary
sources from this list, read these:

- **[MCP — Getting Started](https://modelcontextprotocol.io/docs/getting-started/intro)** — The official entry point. Conceptual overview, plus enough detail to understand what the protocol is actually proposing.
- **[MCP — Specification](https://modelcontextprotocol.io/specification/)** — The formal specification. Read it when you want to know what is and is not in scope at the protocol layer. The boundary between "MCP solves" and "MCP deliberately leaves to the layer above" is the load-bearing distinction in [`WHY_MCP_MATTERS.md`](WHY_MCP_MATTERS.md).
- **[MCP — Architecture](https://modelcontextprotocol.io/docs/learn/architecture)** — The host, client, and server roles, plus the protocol's capability-negotiation model.
- **[MCP — Governance](https://modelcontextprotocol.io/community/governance)** — The public governance structure for the evolving project.
- **[Anthropic — Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol)** — The original announcement. Context for why the standard was published openly rather than as a proprietary protocol.
- **[Model Context Protocol GitHub organization](https://github.com/modelcontextprotocol/modelcontextprotocol)** — The reference implementations, the schema, and the conversation. The protocol is fast-moving; the GitHub organization is the canonical place to track what is current.

A note on currency: MCP is being adopted, extended, and implemented across many systems simultaneously. The specification is the safest source for what is part of the protocol today. Vendor-specific extensions vary.

---

## Adjacent concepts worth your time

We do not maintain a sprawling bibliography. The following are the few areas where the existing public literature is genuinely useful as background for the arguments in this repository:

- **Standards as infrastructure.** The general argument that protocol layers, not products, define platform shifts has a long lineage in writing about the internet's history. Tim Berners-Lee's original web proposal and the IETF's design principles for HTTP and DNS are both worth reading as analogies. The pattern repeats in our era.

- **The economics of platform shifts.** The observation that value migrates to the operational layer above a commoditizing substrate is older than software. Carlota Perez's framework on technological revolutions and financial capital is the most useful long-form treatment we know.

- **Audit and evidence as engineering primitives.** Most domains that have scaled — finance, medicine, law — externalized trust into evidence chains long before software did. The literature on audit trails in those domains predates AI by decades and remains relevant.

We are not suggesting these specific texts are essential. We are pointing at the bodies of work that inform the arguments here, so a reader can locate them on their own and read what fits.

---

## What this list is not

This is not an exhaustive bibliography of AI research, agentic systems papers, or vendor documentation. The field moves too quickly for that list to be useful, and we are not in the business of maintaining a literature review.

For the current state of any single concept — agentic frameworks, model evaluations, capability registries — the working hypothesis is that the relevant project's own documentation is the most up-to-date source. Search accordingly.

---

**Back to** [README](README.md)
