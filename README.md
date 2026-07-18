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

1. **Fork or clone** the repo:
   [github.com/srivardhanjalan/agent-persona-kit](https://github.com/srivardhanjalan/agent-persona-kit)
2. **Point your agent at the persona a task needs.** For example, hand it:
   > Read `software-developer.md` and adopt it as your working standard, then implement the change.
3. **Stack several for a job that spans crafts:**
   - a blog post → content writer + content designer
   - a deploy → devops engineer + cloud architect
   - anything shipping to the public → also the security engineer

## Why personas

The content writer knows what makes a title work; the security engineer assumes
the repo goes public tomorrow; the product manager decides what earns its way
in. That is what a persona buys you: durable context, loaded on demand, so
you're not re-explaining your bar every session.

These files are deliberately **bare-bones** — the opinionated kernel of each
craft, nothing project-specific baked in. They're seeds, not finished playbooks.
You grow them.

## The roster

13 personas across four work areas. Each is self-contained — fork, drop, or
rewrite one without touching the others.

## What a persona looks like

Each file is short: an identity line and a handful of core principles. In full,
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
```

## How to train them

Personas earn their weight by learning. When a project teaches you something — a
rule, a correction, a practice that worked — add it to the persona it belongs
to, in that craft's voice, with the reasoning that earned it.

Keep one line clear: **craft rules go in the persona; project rules don't.**
"Titles must carry meaning" is craft, and it belongs here. "Every release ships
a changelog at `docs/CHANGELOG.md`" is workflow; it belongs in your project's
own config, not a persona you reuse across projects.

## License

MIT — see [LICENSE](LICENSE). Fork it, adapt it, make it yours.
