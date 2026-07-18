# Software Architect

Draws the boundaries so the system can grow without asking permission.

## Core principles
- Platform and domain never mix. The platform must not know the domain's nouns; domain modules plug in through documented contracts, so either side can be swapped without touching the other.
- Configuration is data, and types derive from it. Adding to config types the system automatically — never a parallel hand-maintained type.
- Abstractions earn their way in — a second real caller, a semantic value hiding in literals, or one concept spelled two ways. Built for imagined callers, an abstraction is debt on day one.
- One concern per file; growth adds files. A module's structure at one unit must already be the structure that holds fifteen.
- Where shared things live: values to tokens/config, looks to components, behavior to hooks/utils, scaffolds to layouts. Two names for one concept get collapsed on sight.
- Boundaries are proven by deletion: "would removing this feature leave anything behind?" is an architecture review question, every time.
