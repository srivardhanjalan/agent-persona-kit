---
title: Agent Persona Kit
permalink: /
---

<p align="center">
  <img src="assets/banner.png" alt="Agent Persona Kit — starter role personas for AI agents" width="100%">
</p>

# Agent Persona Kit

A good agent isn't one giant prompt — it's a small team of specialists you can
summon by name. This is a starter set of those specialists: one Markdown file
per craft, each a short, opinionated statement of how that role works. Fork it
and pull in the specialists a task needs.

Works with any agent that can read a file: Claude Code, Cursor, an SDK loop, or
a plain system prompt. The personas are just Markdown; nothing here is
tool-specific.

## Quickstart

1. **Fork or clone** the repo and point your agent at the folder so it can read the personas:
   [github.com/srivardhanjalan/agent-persona-kit](https://github.com/srivardhanjalan/agent-persona-kit)
2. **Then just ask — in plain language.** No prompt-engineering; name the specialist and hand over the task:
   > Consult the product manager and pressure-test this feature.

   > Bring in the graphic designer.
3. **Stack several for a job that spans crafts:**
   - a blog post → content writer + content designer
   - a deploy → devops engineer + cloud architect
   - anything shipping to the public → also the security engineer

## Why personas

The content writer knows what makes a title work; the security engineer assumes
the repo goes public tomorrow; the product manager decides what earns its way
in. That is what a persona buys you: durable context, loaded on demand, so
you're not re-explaining your bar every session.

You don't engineer the prompt; the persona primes the agent. Reach for the
product manager and it starts interrogating who the user really is; reach for
the graphic designer and it finally has opinions on hierarchy and whitespace.

These files are deliberately **bare-bones** — the opinionated kernel of each
craft, nothing project-specific baked in. They're seeds, not finished playbooks.
You grow them.

## The roster

18 personas — one orchestrator and seven craft areas. Each is self-contained;
fork, drop, or rewrite one without touching the others. And each file ends
with a **Works with** section naming the personas it consults, so the team
can hand work off and pressure-test each other (see
[Orchestration](#orchestration)).

### Orchestrator

| Persona | Owns |
|---|---|
| [Team Leader](team-leader.md) | direction, review, sequencing, the final cut |

### Engineering

| Persona | Owns |
|---|---|
| [Software Developer](software-developer.md) | code, verification, deleting what isn't earning its place |
| [Software Architect](software-architect.md) | boundaries, contracts, module design |
| [Software Tester](software-tester.md) | test strategy, edge cases, regression, flaky-test discipline |

### Infrastructure & Security

| Persona | Owns |
|---|---|
| [Cloud Architect](cloud-architect.md) | infrastructure topology, cost, teardown |
| [DevOps Engineer](devops-engineer.md) | pipelines, deploys, gates |
| [Security Engineer](security-engineer.md) | secrets, auth, exposure discipline |

### Product

| Persona | Owns |
|---|---|
| [Product Manager](product-manager.md) | scope, sequencing, audience value |
| [Product Brainstormer](product-brainstormer.md) | idea generation, research, validation |

### Data & Research

| Persona | Owns |
|---|---|
| [Data Scientist](data-scientist.md) | data analysis, statistical rigor, verifying claims with data |
| [Researcher](researcher.md) | sourcing, evidence, synthesis, citation discipline |

### Design

| Persona | Owns |
|---|---|
| [Product Designer](product-designer.md) | UX, interaction, design systems |
| [Content Designer](content-designer.md) | covers, imagery, visual publishing |
| [Graphic Designer](graphic-designer.md) | composition, grid, type, optical detail |

### Writing & Learning

| Persona | Owns |
|---|---|
| [Content Writer](content-writer.md) | prose, titles, voice |
| [Educator](educator.md) | tutorials, curriculum, learner experience |

### Distribution & Growth

| Persona | Owns |
|---|---|
| [Social Media Manager](social-media-manager.md) | distribution, platform mechanics |
| [Influencer](influencer.md) | hooks, engagement, the reason to comment |

## Orchestration

<p align="center">
  <img src="assets/orchestration.png" alt="How the orchestration works: one prompt goes to the team leader, which decomposes it, assigns the specialists, and loops the review until it comes back clean, then ships." width="560">
</p>

A team is more than a pile of specialists — it's who defers to whom. Every
persona ends with a **Works with** section that names the others it consults,
so the roster is also a chain of command. Two ways to run it:

**Let the team leader coordinate.** Hand a whole job to the
[team leader](team-leader.md); it scopes the work, pulls in the right
specialists (or the whole set a cross-craft job needs), runs their review
in parallel — re-running it until a pass comes back clean — and gives you the
final cut:

> Team leader: take this landing page from draft to shipped.

**Or consult specialists directly — they pull in each other.** Because each
persona knows who it answers to, a single request fans out along the links.
Ask the content writer for a post and it already defers to the educator (is
this true to what shipped?) and leashes the influencer's hook; ask the
cloud architect for infrastructure and it loops in the security engineer
before anything goes public:

> Bring in the influencer for the hook — then have the content writer make
> sure it's honest.

The **Works with** links aren't decoration; follow them and the team reviews
itself.

## See it in action

One prompt — `Team leader: build & ship my launch page — hero, three features, a
sign-up CTA` — produced a complete, reviewed landing page. The team leader
scoped it, the specialists built it, and the review loop caught real bugs
(truncated roster lines, a relationship written backwards, a clipping code
panel) and fixed them before it shipped. The full artifact — the page and the
run that made it — is in **[`example/`](example/)**.

## What a persona looks like

Each file is short: an identity line, a handful of core principles, and a
**Works with** section pointing to the personas it consults. In full,
[`product-manager.md`](product-manager.md):

```markdown
# Product Manager

Decides what earns its way in — and when.

## Core principles
- YAGNI is product law: features, config, and content ship when something consumes them, never in anticipation.
- Sequence for narrative and dependency: finish and verify one release before the next; each ends in a state a user can hold.
- Costs are stated plainly — surprise costs destroy trust.
- The audience designs with you: reader questions and comments are requirements intake.
- Series and brand consistency compound: naming, voice, and house style are product surface, not decoration.
- Work from a checklist, not memory — turn what you're handed into an explicit list of what "done" requires, break down any item still fuzzy before starting it, and check each off as you finish; an unchecked box is unfinished work, nothing ships with one open.

## Works with
- Sequences with [product-designer](product-designer.md), mines validated ideas from [product-brainstormer](product-brainstormer.md), and scopes what [educator](educator.md) teaches.
- Weighs [researcher](researcher.md)'s evidence and [data-scientist](data-scientist.md)'s numbers before deciding what earns its way in.
```

## How to train them

Personas earn their place by learning. When a project teaches you something — a
rule, a correction, a practice that worked — add it to the persona it belongs
to, in that craft's voice, with the reasoning that earned it.

Keep one line clear: **craft rules go in the persona; project rules don't.**
"Titles must carry meaning" is craft, and it belongs here. "Every release ships
a changelog at `docs/CHANGELOG.md`" is workflow; it belongs in your project's
own config, not a persona you reuse across projects.

## License

MIT — see [LICENSE](LICENSE). Fork it, adapt it, make it yours.
