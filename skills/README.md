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
| [plim-design](plim-design/SKILL.md) | Any design decision; foundation for the rest | Decision model, eight distinctions, tensions, attention, semantic honesty, the canonical state model, automation and agency, familiarity and identity, edges, system inventory, greenfield foundations and density, the outcome scale and "no change", explaining decisions; product decision records in [`decision-records.md`](plim-design/decision-records.md), shared systems and libraries in [`systems.md`](plim-design/systems.md), interface language in [`language.md`](plim-design/language.md) |
| [plim-review](plim-review/SKILL.md) | Critique without editing | Review lenses, finding classification, evidence discipline; working with partial evidence, code-only review, scoping, and decision owners in [`evidence.md`](plim-review/evidence.md) |
| [plim-beautify](plim-beautify/SKILL.md) | Improving existing UI | Request interpretation (premium, modern), beautification sequence, intervention ladder, cliché catalogue |
| [plim-accessibility](plim-accessibility/SKILL.md) | Inclusive design and verification | How accessibility shapes decisions, conflict resolution, verification |
| [plim-responsive](plim-responsive/SKILL.md) | Adaptation across contexts | Context dimensions, adaptation strategies, surface-specific reasoning |
| [plim-ui](plim-ui/SKILL.md) | Angular projects using plim-ui, and work on plim-ui itself | Precedence, concept mapping; versioned facts in [`reference.md`](plim-ui/reference.md), update process in [`MAINTAINING.md`](plim-ui/MAINTAINING.md) |

Each concept is defined once, in the skill that owns it; other skills refer to it. Typical combinations:

- **"Improve this screen"** → plim-design + plim-beautify (which uses plim-review, plim-accessibility, plim-responsive at its steps)
- **"What's wrong with this?"** → plim-design + plim-review
- **"Build this in our plim-ui app"** → plim-design + plim-ui

## Framework independence

All skills except `plim-ui` are framework-agnostic. They work inside whatever stack and design system a product uses ([`plim-design`](plim-design/SKILL.md), "Preserve before replacing"); [`integrations/`](../integrations/) only signposts that.

## Installing

Install from GitHub with the Agent Skills CLI.

```bash
npx skills add Fexost/plim-design
```

Global install: `npx skills add Fexost/plim-design -g`. One skill: `npx skills add Fexost/plim-design --skill plim-design`. If you install any specialist skill, also install `plim-design`. See the [repository README](../README.md).

The CLI copies each `skills/<name>/` directory. Links between those directories work when the skills are installed together. Links to `philosophy/` resolve in this repository; the canonical file is also at <https://github.com/Fexost/plim-design/blob/v1.0.0/philosophy/philosophy.md>.
