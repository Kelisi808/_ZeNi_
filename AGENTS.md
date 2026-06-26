# AGENTS.md

> Guidance for AI assistants working in this repository. This is the
> public-facing `_ZeNi_` repo — read this before generating, editing,
> or recommending any change.

## What this repository is

The `_ZeNi_` repository is the **public editorial home** for the ZéNí venture. It is intentionally separate from the product working trees. Everything here is meant to be read by curious visitors — developers, students, journalists, investors, prospective collaborators — and to leave them with sharper understanding of agentic AI, the Agentic Web, MCP, coordination, governance, and evidence.

You are working on the venture's public voice. Treat that responsibility seriously.

## How to think about edits

When you propose or make a change to this repository, hold yourself to four editorial commitments:

- **Confident without overclaiming.** A position the reader can disagree with is healthier than a marketing line they can dismiss.
- **Substantive without being academic.** Every concept earns its place by its consequence in real work, not by theoretical density.
- **Plainspoken without being thin.** Short prose where short prose is honest; long prose where the argument earns it.
- **Educational, not promotional.** A reader who never engages with the venture should still walk away smarter about the field.

The tone of the existing essays is editorial-grade — declarative sentences, deliberate paragraph breaks, occasional block quotes, comparison tables when they help. New content should match. The repository is curated, not dumped.

## What does not belong here

The line between this repository and the product working trees is deliberately strict. Do not add:

- Product source code or partial source fragments.
- Internal architecture diagrams, schemas, store layouts, API contracts.
- Proprietary routing logic, model allocation specifics, or other implementation mechanics.
- Internal strategy memos, post-mortems, or decision documents.
- Architecture-kit materials or any of their contents.
- Roadmaps with dates, dependencies, or commitment language.
- Secrets, credentials, deployment configurations, environment variables, or local file paths.
- Customer, partner, or investor identities, conversation transcripts, or any non-public detail of a relationship.

The `.gitignore` blocks source extensions and secret patterns at the version-control layer as a safety belt. Operational discipline closes the rest of the gap.

## What does belong here

Add only material that meets all three tests in the [`PUBLIC_REPOSITORY_NOTE`](PUBLIC_REPOSITORY_NOTE.md): publishable as an essay or talk without competitive harm, conceptually educational about a public idea, and useful to the venture as widely-read public knowledge rather than as a secret.

In practice this means:

- Conceptual explainers on the Agentic Web, MCP, governance, evidence, trust.
- Editorial framing of ZéNí's worldview and positioning.
- Glossary entries, FAQ answers, primers, brand context.
- Diagrams and visual concepts that operate at the level of "humans, agents, evidence" rather than at the level of system internals.

## When in doubt

If you cannot decide whether a piece of content belongs, ask:

> Would a curious reader — not connected to the venture — be **better off** for having read this, **even if they never engage with the venture afterward**?

If the answer is yes, the content is appropriate. If the answer is no, or if the value is only legible to someone already inside the venture, the content belongs in a product working tree.

## Practical pointers

- The repository's reading distances are documented in [REPO_STRUCTURE.md](REPO_STRUCTURE.md). When adding content, decide where it sits on that ladder (manifesto → essay → primer → reference) and write to that distance.
- Cross-link new content from the README and from related essays. The repository is a deliberate network, not a flat folder of files.
- For new languages or large editorial expansions, follow the precedent set in [`Language Options/`](Language%20Options/) — hand-written summaries, not machine-translated stubs.
- The thesis is public. The work is operational. Hold that boundary in every edit.

The goal is to help visitors understand why ZéNí matters without turning this public context layer into internal system documentation.
