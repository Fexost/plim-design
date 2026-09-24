# Skills

Portable AI skills that operationalise [`philosophy/philosophy.md`](../philosophy/philosophy.md). The philosophy is canonical; the skills translate it into behaviour and must not introduce competing principles.

## How they relate

```text
                    philosophy.md
                         │
                         ▼
                   plim-design
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
   plim-beautify   plim-review   plim-accessibility
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                  plim-responsive
                         │
                         ▼
                      plim-ui
```

The diagram is conceptual: `plim-design` is always the base, `plim-ui` is an optional implementation layer, and the skills in between can be used alone or together.

| Skill | Use for | Owns |
| --- | --- | --- |
| [plim-design](plim-design/SKILL.md) | Any design decision; foundation for the rest | Decision model, eight distinctions, tensions, attention, semantic honesty, the canonical state model, edges, system inventory, "no change" outcome, decision records |
| [plim-review](plim-review/SKILL.md) | Critique without editing | Review lenses, finding classification, evidence discipline |
| [plim-beautify](plim-beautify/SKILL.md) | Improving existing UI | Request interpretation (premium, modern), beautification sequence, intervention ladder, cliché catalogue |
| [plim-accessibility](plim-accessibility/SKILL.md) | Inclusive design and verification | How accessibility shapes decisions, conflict resolution, verification |
| [plim-responsive](plim-responsive/SKILL.md) | Adaptation across contexts | Context dimensions, adaptation strategies, surface-specific reasoning |
| [plim-ui](plim-ui/SKILL.md) | Angular projects using plim-ui, and work on plim-ui itself | Precedence, concept mapping; versioned facts in [`reference.md`](plim-ui/reference.md), update process in [`MAINTAINING.md`](plim-ui/MAINTAINING.md) |

Each concept is defined once, in the skill that owns it; other skills refer to it. Typical combinations:

- **"Improve this screen"** → plim-design + plim-beautify (which uses plim-review, plim-accessibility, plim-responsive at its steps)
- **"What's wrong with this?"** → plim-design + plim-review
- **"Build this in our plim-ui app"** → plim-design + plim-ui

## Framework independence

All skills except `plim-ui` are framework-agnostic. Stack-specific notes belong in [`integrations/`](../integrations/).

## Installing

Skills link to each other and to the philosophy with relative paths. Keep the `skills/` directory together, and keep `philosophy/`, `anti-patterns/`, and `examples/` alongside it when you can; see [`adapters/`](../adapters/). If you install a single skill, also install `plim-design`.

> TODO: Publish Plim Design as a single installable package that provides all skills and their supporting material.
