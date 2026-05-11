# Public Diagram Concepts

> A reference for future visual work. These are diagram **concepts** —
> not finished assets — for visualizing the venture's thesis in ways
> that do not expose implementation.

The first finished asset is [`assets/diagrams/zeni-public-layer-diagram.svg`](../../assets/diagrams/zeni-public-layer-diagram.svg) — the Humans / Agents / Evidence → Operable Intelligence layered diagram. Additional visuals should match its grammar: dark mineral palette, editorial typography, restraint, no decorative flourish. The visual should look like the essays read.

## Why a diagram reference at all

Most AI marketing diagrams are bad in the same way: they layer logos, gradient ribbons, and "AI brain" iconography over an architecture that does not exist or is too vague to matter. The result is a deck slide that says nothing and survives nowhere.

We want the opposite. Each visual in this repository should be **legible at a glance, defensible under scrutiny, and useful as a thinking tool** rather than as decoration. The concepts below are starting points for visuals that meet that bar.

---

## Concept 1 — From Answer to Workflow

The simplest possible diagram for the venture's thesis. Three rows, vertically stacked:

- **Row 1 — Question and answer.** A human asks. An AI responds. Single arrow. This is the world most current AI products live in.
- **Row 2 — Question and workflow.** A human asks. An agent decomposes the request, calls tools, coordinates steps, returns an output. Multiple arrows, in sequence.
- **Row 3 — Question and operable workflow.** A human asks. The agentic system runs the workflow, emits evidence, surfaces approval points, and lets the human inspect and intervene. The same flow as row 2, but with a parallel "evidence and oversight" track running alongside.

The reader should leave the diagram with the intuition: **ZéNí works on the third row.** Most products work on the first two.

Visual treatment: deliberate, sparse. Each row gets the same vertical weight so the comparison is honest. The evidence track in row 3 is rendered in a slightly different color to indicate it is a *property* of the system, not an additional component.

---

## Concept 2 — The Agentic Web Environment

A wider diagram showing the participants of the Agentic Web in one frame:

- **Humans** — operators, reviewers, approvers.
- **Agents** — autonomous and semi-autonomous systems doing the work.
- **Tools and services** — the capabilities agents invoke.
- **Protocols** — the substrate over which the participants talk (MCP and adjacent).
- **Evidence systems** — registries, audit logs, receipt chains.

The participants are not arranged hierarchically. They sit in a shared environment, with arrows representing exchanges that any participant can initiate. The point is: **this is not a vendor diagram**. It is a diagram of a shared open layer.

A common failure mode in this kind of diagram is to put the vendor's logo at the center and arrows pointing inward. Resist that. The point ZéNí is making is the opposite — the agentic web is horizontal, the vendor is one participant among many.

Visual treatment: nodes as plain rectangles with type-led labels (no icons), arrows as thin neutral lines. Mineral charcoal palette throughout. The neutrality is the point.

---

## Concept 3 — The Trust Layer

A more technical diagram for readers who want to see how trust and governance compose at runtime. From left to right:

1. **Intent.** A structured description of what the operator wants, produced by an intake step.
2. **Agents.** The runtime entities that pick up the intent.
3. **Tools.** The capabilities agents invoke under policy.
4. **Workflows.** The sequenced execution of intent into outcome.
5. **Approvals.** The points where human authorization is required, materialized as approval tokens.
6. **Outputs.** The work product handed back to the operator.

These six elements are *threaded* by two parallel tracks:

- **Governance** — the policy decisions that gate every consequential call.
- **Evidence** — the receipt chain that records what happened at every step.

The reader should leave with the intuition that **governance and evidence are not stages in the workflow — they are properties of every stage**. They sit underneath the diagram, not as a step between intent and output.

Visual treatment: the six elements appear as evenly-weighted columns. The governance and evidence tracks render as horizontal bars under the columns, so the visual reads "across" rather than "down." This is the most diagram-heavy of the three concepts and should only be used where the audience benefits from the technical detail.

---

## What to keep doing

When a new visual is needed, write the concept here first. Diagrams that emerge from a brief like the ones above tend to be defensible. Diagrams that emerge from "we need something for the deck" do not.

If the brief cannot be written in plain text in fewer than five paragraphs, the diagram probably should not exist yet.

---

**Back to** [REPO_STRUCTURE.md](../../REPO_STRUCTURE.md) · **The first finished asset** → [`zeni-public-layer-diagram.svg`](../../assets/diagrams/zeni-public-layer-diagram.svg)
