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
| **[Anti-patterns](anti-patterns/)** | Supporting depth on generic and low-quality patterns; adds no rules |
| **[Examples](examples/)** | Worked reasoning case studies |
| **Foundations, composition, interaction, accessibility, patterns, integrations, recipes** | Signposts by topic. Each file names the skill section that owns the topic and adds nothing to it |

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
philosophy/     Source of truth (philosophy and manifesto)
skills/         Canonical AI skills that operationalise the philosophy
anti-patterns/  Supporting depth on generic AI UI and quality traps
examples/       Worked reasoning case studies
evals/          Behavioural test scenarios; check the skills, never define them
foundations/    Signposts: colour, type, spacing, … → owning skill sections
composition/    Signposts: layout, hierarchy, grouping, …
interaction/    Signposts: states, feedback, affordances, motion
accessibility/  Signposts to plim-accessibility
patterns/       Signposts: tables, forms, errors, …
recipes/        Signposts: task → skill workflow
integrations/   Signposts: any stack, via plim-design
adapters/       Agent portability
```

## Status

- **Written:** the [philosophy](philosophy/philosophy.md) and [manifesto](philosophy/manifesto.md), the six [skills](skills/) (with reference files for decision records, shared systems, and interface language), [anti-patterns](anti-patterns/) as supporting depth, seventeen [case studies](examples/case-studies/), and a behavioural [evaluation suite](evals/).
- **Signposts:** foundations, composition, interaction, accessibility, patterns, integrations, and recipes point to the skill sections that own each topic. They hold no guidance of their own, by design, so that every concept has one source.

## License

See [LICENSE](LICENSE).
