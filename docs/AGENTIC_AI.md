# Agentic AI

> Most people, asked what "agentic AI" means, will describe a smarter chatbot. They will be wrong.

## The shift, in one sentence

Chatbots **answer**. Agents **act**.

A chatbot's job is to produce useful tokens when you talk to it. An agent's job is to produce real-world consequences — to plan a multi-step workflow, route subtasks to specialized counterparts, use tools, surface evidence, and stop when something looks unsafe.

The distinction is structural, not cosmetic. A chatbot is a function. An agent is a process.

---

## What an agent actually is

The minimum definition of an agent is: **a unit that can be assigned a goal it did not ask for, decide on its own intermediate steps, and produce auditable outcomes.**

That definition forces three things to exist:

1. **A description of intent.** The agent has to translate "what the user wants" into a structured, machine-routable specification — a target, constraints, allowed actions, evidence requirements. The industry calls this an _intent packet_ when it is formal.
2. **A theory of who else exists.** A single model in isolation can answer questions. An agent in a real workflow has to know which other agents (or tools, or services) are reachable, what they are good at, and what they cost in latency, dollars, and risk. This is the **capability discovery** problem.
3. **A trail of what happened.** Without an auditable record — a receipt for every decision and every action — agents are not deployable in serious contexts. Compliance, debugging, model improvement, and operator trust all depend on the trail.

Most "agentic" demos give you the first one and skip the other two. They are demos because the other two are hard.

---

## Why this is the harder problem

For five years the AI industry treated the model as the product. Make the model bigger, the answers get better, the demos get more impressive, the valuations go up.

But agentic work is not bottlenecked on model intelligence anymore. It is bottlenecked on everything around the model:

- **Discovery.** When agent A needs help, how does it find agent B? Today's answer is _"a human wired them together in a JSON file."_ That doesn't scale.
- **Trust.** When agent A asks agent B to do something risky, how does B know A is allowed? How does A know B is who it claims to be? How does either prove the exchange happened? Today's answer is _"both parties run inside the same trusted process."_ That also doesn't scale.
- **Accountability.** When something goes wrong — a bad output, a leaked secret, a wasted budget — who is responsible? What is the evidence chain? Today's answer is _"check the chat transcript."_ That is not evidence.
- **Coordination at runtime.** When the right model for an early phase of work is different from the right model for the later phase, who decides? How is the handoff packet structured? How are costs governed?

These are not model problems. They are systems problems. They are the agentic problems.

---

## The category mistake

The most common framing error in 2026 is to call any LLM wrapper "agentic" because it can call a tool. Tool-calling is necessary but not sufficient.

A system is meaningfully agentic when it can answer **all** of the following without a human in the loop:

- _Who am I asking to do this work?_
- _Can they actually do it?_
- _Are they allowed to do it right now?_
- _What is the receipt going to look like when they are done?_

If the answers come from a human at runtime, you have a sophisticated copilot. You do not have an agent.

---

## What this implies

The next decade of progress in AI will be **less** about model architecture and **more** about the protocols, registries, and accountability layers that turn isolated models into coordinated agents. The model layer is becoming a commodity faster than people realize. The coordination layer is wide open.

This is why ZéNí exists, and this is why we are positioned where we are.

---

**Next →** [The Agentic Web](AGENTIC_WEB.md) — why the web's existing coordination primitives don't fit, and what the right ones look like.
