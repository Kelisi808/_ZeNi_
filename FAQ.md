# FAQ

Common questions from visitors, investors, journalists, prospective collaborators, and curious developers. Answers are written to be honest and direct — short where short is right, longer where the question deserves it.

---

## About the repository itself

**Is this the ZéNí product?**

No. This repository is the **public editorial face** of the venture. It is informational. It does not contain the product, the implementation, or the source code. See [PUBLIC_BOUNDARIES.md](PUBLIC_BOUNDARIES.md) for the explicit line between this repository and the private ones.

**Is ZéNí open source?**

No. The ZéNí implementation is closed and is maintained in private repositories. Specific protocol-adjacent components may be open-sourced after the venture's first pilot, but the core product is not an open-source project.

**Why publish this repository at all, then?**

Two reasons. First, because the conceptual ground covered here — the case for the Agentic Web, the role of MCP, why coordination is the bottleneck — is more valuable as widely-shared public knowledge than as a competitive secret. Second, because curious people need a way to engage with the venture before there is a product they can run.

This repository is the path for that engagement.

**Can I quote or reference material from this repository?**

For non-commercial purposes — journalism, academic writing, analyst coverage, classroom use — yes, with attribution. For commercial reuse, redistribution, or derivative works, no. See [LICENSE](LICENSE).

If you would like to do something the license does not clearly cover, contact the founder. We are reasonable, but we are not unlimited.

---

## About ZéNí

**What is ZéNí?**

ZéNí is an editorial and infrastructure vision for the Agentic Web: a future where AI agents, tools, humans, and protocols need shared systems of coordination, evidence, governance, and trust.

In concrete terms, it ships as three live products that hold three corners of that coordination layer. The product roles are described in [ABOUT_ZENI.md](ABOUT_ZENI.md). The implementation details are private.

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

Same channel. The current state of the venture is pre-pilot, so the conversation is exploratory rather than transactional. We are selective about pilots because each one shapes the implementation in ways that matter.

**I want to write about ZéNí — what's appropriate?**

The conceptual material in this repository is publicly quotable with attribution. The venture's positioning, the manifesto, the educational explainers — those are all on the record. For interviews, specific implementation details, financials, customer/partner identities, or any non-public information, please request a conversation through the founder's channels rather than inferring or guessing.

**I'm a developer interested in contributing — is that possible?**

Not currently in the public repository. The editorial material is a deliberate, founder-voiced artifact and is not structured for outside contributions. If you have a piece of writing or analysis you think belongs here, you are welcome to propose it via outreach, but contributions are by invitation rather than open submission.

When public software components ship in the future, they will have their own contribution paths.

---

## About what's coming

**Will there be open-source releases?**

Specific protocol-adjacent components are planned for open-source release after the venture's first pilot. The components that make the most sense to open-source are the ones that benefit the broader ecosystem more than they benefit the venture's defensibility — things like an agent schema definition, a UI kit for agentic-mode visualization, or an MCP server template. The core implementation will remain closed.

**Will this public repository grow?**

Yes. As the venture matures, additional essays, glossary entries, and educational artifacts will land here. Substantial growth — for example, a polished site at a custom domain, or short-form analyst-style pieces — will be considered when the underlying work warrants it.

**Where is the venture now and where is it going?**

The venture is currently in pre-pilot operation. The pipeline of three live products exists and is reachable; private demonstration is available on request. The near-term focus is first pilot deployment with a serious operational partner. The long-term focus is the coordination layer for the agentic ecosystem.

The shape of the answer to "where is it going" is articulated in the [Manifesto](MANIFESTO.md) and the [Why ZéNí](WHY_ZENI.md) page. The specific timeline is held privately because it is operationally sensitive.

---

**Back to** [README](README.md) · **More on the venture →** [ABOUT_ZENI.md](ABOUT_ZENI.md)
