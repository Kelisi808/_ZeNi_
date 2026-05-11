# Public Boundaries

> This repository is informational and editorial. It does not contain the private ZéNí implementation, internal architecture, proprietary routing logic, private product roadmap, or production system details.

This page exists so the boundary between public material and private intellectual property is **explicit and machine-checkable**, not just implicit.

---

## What this repository is

The `Kelisi808/_ZeNi_` repository is the **public face** of the ZéNí venture. It is a thought-leadership artifact. It is an educational guide. It is a public-facing manifesto. It is the path by which a curious visitor, a prospective collaborator, an analyst, an investor, or a journalist can develop a genuine understanding of:

- the conceptual terrain ZéNí operates in (Agentic AI, the Agentic Web, MCP, governance, evidence);
- the worldview that informs the venture;
- the founder, the venture's status, and how to make contact.

Everything here is intentionally **portable knowledge**. You should be able to copy any sentence in this repository into a slide, an article, a class lecture, or a conversation, and have it land as a clean, defensible statement about where AI is going.

---

## What this repository is not

This repository is **not**:

- The ZéNí source code.
- A clone, mirror, or summary of the private repositories.
- An SDK, library, framework, or installable package.
- A specification of the internal product mechanics.
- A description of the system's architecture, deployment topology, secrets, or schemas.
- A roadmap of unreleased features.
- A document trail of internal strategy discussions.

If you arrived here expecting any of the above, the expectation was mistaken and this repository will not satisfy it.

---

## What you will not find here, by design

The following categories of material are deliberately excluded:

| Category | Why it is excluded |
|---|---|
| Source code (TypeScript, JavaScript, Python, configuration files) | Implementation is closed. The `.gitignore` blocks these extensions as a safety belt. |
| Internal API contracts, endpoint paths, request/response schemas | Reveals attack surface and integration mechanics. Not for the public layer. |
| Database schemas, store layouts, table definitions | Implementation-specific. Belongs in the private repos. |
| The internal architecture kit (versioned design specs) | A private working document. Its contents would reveal multi-year strategy evolution. |
| Routing algorithms, model allocation logic, lease policy details | Proprietary. The conceptual category is publicly discussed; the mechanics are not. |
| Private strategy memos, post-mortems, internal critique documents | Operational hygiene material. Not for outside readers. |
| Investor demo notes, fallback scripts, known weaknesses | Sensitive to active fundraising and pilot conversations. |
| Secrets, credentials, environment variables, deployment configurations | Self-evident. |
| Internal product roadmap with dates and dependencies | Locks public communication into commitments that may change. |
| Customer or partner identities, conversation transcripts | Confidentiality of relationships. |

---

## What you will find here

The complementary list:

| Category | Why it is included |
|---|---|
| Conceptual essays on Agentic AI, the Agentic Web, MCP | Educational content that benefits the broader field, not just ZéNí. |
| ZéNí's worldview and manifesto | Public positioning. Establishes the frame the venture operates within. |
| High-level mission and product roles | A visitor should know what the three products are and what role each plays — without learning how any of them is built. |
| Glossary and FAQ | So the conceptual vocabulary is accessible to non-specialists. |
| Founder identity and contact path | So engagement is possible. |
| Restrictive license | So the educational material is not appropriated. |

---

## A practical test

If you are unsure whether a piece of content belongs in this public repository, ask the following questions in order:

1. **Could this content be in a published essay, an industry article, or a conference talk** without compromising anything competitively sensitive?
2. **Does this content educate about a public concept** (Agentic AI, MCP, coordination) rather than describing an internal mechanism?
3. **Would the venture be better off if this content were widely read** than if it were never read at all?

If all three answers are yes, the content is appropriate for this repository. If any answer is no or uncertain, the content belongs in the private repositories.

---

## Repository safety mechanisms

In addition to this explicit policy, the public repository is protected by:

- **`.gitignore`** that blocks source extensions (`*.ts`, `*.tsx`, `*.js`, `*.jsx`, common application directories) and secret patterns (`.env`, `Secrets/`) at the version-control layer. Files matching these patterns cannot accidentally land in a commit.
- **A restrictive [LICENSE](LICENSE)** establishing that the editorial material is published for visitor education and is not licensed for redistribution, derivative works, or commercial reuse. The implementation is not covered by any license here because it is not present here.
- **Operational discipline**: contributions to this repository are reviewed against this `PUBLIC_BOUNDARIES.md` policy before being committed.

---

## A note on transparency

The venture is private at the level of implementation. The venture is **not** private at the level of intent.

We believe that the conceptual ground covered by this repository — the case for the Agentic Web, the role of MCP, the centrality of coordination and evidence, the framing of operable intelligence — is more valuable as widely-shared public knowledge than as a competitive secret. The conceptual contribution is part of how the venture earns its place in the conversation.

This repository is the formal artifact of that contribution.

---

**Back to** [README](README.md)
