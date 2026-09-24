# Plim Design

A **framework-agnostic design philosophy** and **AI skill library** for building intentional, polished, accessible interfaces.

Plim Design is not a CSS framework, component library, or visual clone of any existing design language. It teaches **how to decide**, not **what pixels to copy**.

## Core positioning

> **Build interfaces with the clarity of Apple, the systematic thinking of Material, and an identity of their own.**

> **Plim does not prescribe what your product should look like. It teaches you how to make your product look intentional.**

These statements describe **influences on thinking**—clarity, systematic structure, and distinctive product identity—not an attempt to reproduce Apple Human Interface Guidelines or Material Design as a product skin.

## What is Plim Design?

Plim Design separates:

| Layer | Role |
| --- | --- |
| **[Philosophy](philosophy/philosophy.md)** | Human-readable source of truth: beliefs, principles, and reasoning |
| **[Skills](skills/)** | Portable AI instructions that operationalise the philosophy |
| **Foundations, composition, interaction** | Visual and behavioural building blocks derived from philosophy |
| **[Patterns](patterns/)** | Recurring interface problems and design reasoning |
| **[Integrations](integrations/)** | How to apply Plim with your stack without replacing it |

You can adopt Plim Design while keeping Angular, React, Vue, Svelte, vanilla HTML/CSS, Tailwind, Bootstrap, Material, shadcn, proprietary design systems, or custom component libraries.

## Framework agnostic

Plim Design improves **design decisions** in your application. There is no Plim visual identity to adopt, and no need to swap your component library: your existing design system is treated as your product's vocabulary. Start with the [`plim-design`](skills/plim-design/SKILL.md) skill, which explains how Plim works inside an existing system.

## Plim UI (reference implementation)

[**plim-ui**](https://github.com/Fexost/plim-ui) is a separate Angular component library that will serve as the **reference implementation and showcase** of this philosophy.

Plim Design stands on its own. Plim UI is optional—use it when you want an Angular-native expression of the ideas, not as a prerequisite.

**Plim Design has a philosophy, not a look. Plim UI has a look, but that look is an implementation of the philosophy, not the definition of it.**

## AI-first

This repository is structured for **human readers** and **coding agents**:

- Root **[AGENTS.md](AGENTS.md)** orients agents without duplicating the whole corpus.
- **[skills/](skills/)** holds canonical skill definitions (copy or symlink into your agent’s skill path as needed).
- **[adapters/](adapters/)** documents how skills map to different agent environments.

Compatibility with specific agent products is not claimed here unless verified in [adapters/](adapters/).

## Repository map

```text
philosophy/     Source of truth (beliefs, manifesto, principles)
foundations/    Visual building blocks (colour, type, spacing, …)
composition/    How elements work together
interaction/    State, feedback, affordances
accessibility/  First-class accessibility guidance
patterns/       Recurring UI problems and reasoning
anti-patterns/  Generic AI UI and quality traps
recipes/        End-to-end workflows for humans and agents
skills/         Canonical AI skills
integrations/   Stack-specific notes (still philosophy-first)
examples/       Worked reasoning case studies
adapters/       Agent portability
```

## Status

- **Written:** the [philosophy](philosophy/philosophy.md) and [manifesto](philosophy/manifesto.md), the six [skills](skills/), [anti-patterns](anti-patterns/) as supporting depth, and twelve [case studies](examples/case-studies/).
- **Placeholders:** foundations, composition, interaction, accessibility, patterns, integrations, and most recipes are marked with explicit TODOs. The philosophy and skills are usable without them.

## License

See [LICENSE](LICENSE).
