# FAQ

Common questions from visitors, investors, journalists, prospective collaborators, and curious developers. Answers are written to be honest and direct — short where short is right, longer where the question deserves it.

---

## About the repository itself

**Is this the ZéNí product?**

This is the public editorial home for ZéNí — a place to understand the ideas, vocabulary, and vision behind the venture. It is the context layer, not a source-code distribution. See the [Public Repository Note](PUBLIC_REPOSITORY_NOTE.md) for the framing.

**Is ZéNí open source?**

This repository is open for reading, reference, and public context. It is not structured as an open-source product repository today. If specific protocol-adjacent components are released later, they will be introduced with their own contribution paths.

**Why publish this repository at all?**

The conceptual ground covered here — the case for the Agentic Web, the role of MCP, why coordination is the bottleneck — is genuinely valuable as widely shared public knowledge. Curious people deserve a way to engage with the venture's ideas, vocabulary, and current public materials.

This repository is the path for that engagement.

**Can I quote or reference material from this repository?**

For non-commercial purposes — journalism, academic writing, analyst coverage, classroom use — yes, with attribution. For commercial reuse, redistribution, or derivative works, please reach out first. See [LICENSE](LICENSE).

---

## About ZéNí

**What is ZéNí?**

ZéNí is building governed coordination for autonomous agent teams: a future where AI agents, tools, humans, and protocols need shared systems of coordination, evidence, governance, and trust.

In concrete terms, it ships as three live products in pre-pilot operation: PitStop as the human command surface, SideQuest as the machine routing and accountability layer, and ZéNí as the trust fabric connecting them. The product roles are described in [ABOUT_ZENI.md](ABOUT_ZENI.md).

**What problem does ZéNí solve?**

The agentic AI industry has reached a point where models are no longer the limiting factor. The limiting factor is the **coordination layer** that turns isolated models into accountable, governed, composable agents. ZéNí is built specifically to address that layer.

Without that layer, agentic AI stays in the demo phase forever — impressive in the lab, brittle in production, unauditable in regulated domains. The companies that can use agentic AI seriously are the ones with a real coordination substrate.

**How is ZéNí different from a chatbot platform?**

A chatbot platform makes it easier to deploy a single language model with a conversational interface. ZéNí is concerned with what happens when **multiple agentic systems need to work together** — find each other, route work, prove identity, leave receipts, escalate to humans when needed.

The two categories address different layers of the problem. A chatbot is a feature. A coordination layer is infrastructure.

**Why is "ZéNí" written with accents?**

The full brand is **ZéNí** (with diacritics). In ASCII-only contexts — code, URLs, repository names — we write it **ZeNi**. Both refer to the same venture.

---

## About the technology context

**What is Agentic AI?**

Agentic AI is the class of AI systems whose primary mode of work is **taking action**, not generating responses. An agent decomposes a goal into steps, decides on its own intermediate moves, executes them, and produces an auditable record.

The distinction from a chatbot is structural: chatbots complete a turn; agents complete a workflow.

→ Full explainer: [AGENTIC_AI.md](AGENTIC_AI.md)

**What is the Agentic Web?**

The Agentic Web is the condition the web takes on when its native participants are autonomous systems instead of human readers. Pages and APIs were built for one set of assumptions; the agentic primitives — discovery, capability registries, signed identity, policy-bound work, receipts — are a different set.

→ Full explainer: [AGENTIC_WEB.md](AGENTIC_WEB.md)

**What is MCP?**

MCP — Model Context Protocol — is an open standard, originated by Anthropic, that defines how language models talk to the world outside themselves. It standardizes the surface that capability providers expose, so any compliant model can use any compliant capability without bespoke integration.

MCP solves the wiring problem. It does not solve the governance, evidence, or coordination problems. Those need a layer on top.

→ Full explainer: [WHY_MCP_MATTERS.md](WHY_MCP_MATTERS.md)

**Why does agent coordination matter?**

Because every realistic deployment of agentic AI involves multiple components: multiple agents, multiple tools, multiple models, sometimes multiple vendors. Without coordination primitives — discovery, routing, authorization, evidence — those components either cannot collaborate at all or collaborate brittly through bespoke wiring.

Coordination is what turns "an interesting demo" into "a system a regulated industry can use." Every domain that matters in white-collar work — law, medicine, finance, operations, education — has audit and accountability requirements. None of those are met by an unobserved agent.

**Why does governance matter?**

Two reasons.

The **regulatory reason**: agentic systems making consequential decisions on someone's behalf are going to be subject to the same scrutiny as any other automated decision system. The systems with governance baked in survive that scrutiny. The systems that bolted it on after the fact do not.

The **operational reason**: governance is the only way an organization can confidently let agentic systems operate. The alternative — every action gated by a human reviewer — is not agentic. It is dictation. Governance is what makes meaningful autonomy possible without losing oversight.

**Why does evidence matter?**

Because trust by assertion does not survive contact with the real world. Every consequential domain humans have built — banking, medicine, law — eventually moved from trust ("we say we did the thing") to evidence ("here is the verifiable record of the thing").

Agentic AI will not be different. The systems that get adopted in serious contexts will be the ones whose every consequential decision is inspectable, attributable, and replayable. That is what evidence-by-default makes possible.

---

## About engagement

**How do I follow the venture's progress?**

The most direct channels are the founder's [LinkedIn](https://www.linkedin.com/in/kelisi/) and [GitHub](https://github.com/Kelisi808). When narrow open-source moves or major public-facing announcements happen, they will be referenced from this repository.

**I'm an investor — how do I get in touch?**

Through the founder's LinkedIn, with a short note indicating the nature of the conversation. Outreach with a clear thesis or specific question gets answered faster than generic interest.

**I'm a prospective pilot customer — how do I engage?**

Same channel. The current state of the venture is pre-pilot, so the conversation is exploratory rather than transactional. We are selective about pilots because each one shapes the product direction in ways that matter.

**I want to write about ZéNí — what's appropriate?**

The conceptual material in this repository is publicly quotable with attribution. The venture's positioning, the manifesto, the educational explainers, and the current public deck are on the record. For interviews, financials, customer or partner references, and roadmap-sensitive questions, request a conversation through the founder's channels rather than inferring or guessing.

**I'm a developer interested in contributing — is that possible?**

Not currently in the public repository. The editorial material is a deliberate, founder-voiced artifact and is not structured for outside contributions. If you have a piece of writing or analysis you think belongs here, you are welcome to propose it via outreach, but contributions are by invitation rather than open submission.

When public software components ship in the future, they will have their own contribution paths.

---

## About what's coming

**Will there be open-source releases?**

Possibly, but not as a promise in advance of the right use case. The components that make the most sense to release publicly are the ones that benefit the broader ecosystem without weakening the venture's defensibility — for example, an agent schema definition, a UI kit for agentic-mode visualization, or an MCP server template.

**Will this public repository grow?**

Yes. As the venture matures, additional essays, glossary entries, and educational artifacts will land here. Substantial growth — for example, a polished site at a custom domain, or short-form analyst-style pieces — will be considered when the underlying work warrants it.

**Where is the venture now and where is it going?**

The venture is currently in pre-pilot operation. The pipeline of three live products exists and is reachable; demonstration is available on request. The near-term focus is first pilot deployment with a serious operational partner. The long-term focus is the coordination layer for the agentic ecosystem.

The shape of the answer to "where is it going" is articulated in the [Manifesto](MANIFESTO.md), the [Why ZéNí](WHY_ZENI.md) page, and the [ZéNí Pitch Deck](Z%C3%A9N%C3%AD%20Pitch%20Deck.html).

---

**Back to** [README](README.md) · **More on the venture →** [ABOUT_ZENI.md](ABOUT_ZENI.md)
