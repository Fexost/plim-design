# Agent orientation (Plim Design)

Read this before applying any skill in [`skills/`](skills/).

## What Plim Design is

- **Framework agnostic** — Works with any frontend stack or existing design system.
- **Philosophy-first** — [`philosophy/`](philosophy/) is the source of truth for beliefs and reasoning.
- **Skills operationalise philosophy** — Skills in [`skills/`](skills/) implement workflows; they must not invent competing principles.
- **A philosophy, not a look** — Plim Design has no visual aesthetic of its own. Quiet, expressive, dense, spacious, playful, or luxurious products can all be Plim (§15 of the philosophy).

## What Plim Design is not

- Not a component library, CSS framework, or token package.
- Not an Apple or Material clone; do not copy HIG/Material wording or impose their visual identity.
- Not a mandate to use [plim-ui](https://github.com/Fexost/plim-ui) unless the user explicitly requests that integration ([`skills/plim-ui/SKILL.md`](skills/plim-ui/SKILL.md)).

## How to work

1. **Preserve** the project’s technology, components, and design system unless the user asks to change them. A documented system is the product’s vocabulary, not a list of anti-patterns.
2. **Improve intentionality** — purpose, hierarchy, composition, clarity, character, accessibility — without decorative churn. Restraint and expression are both legitimate; the product’s purpose and identity decide the balance.
3. **Treat accessibility as foundational**, not a post-hoc checklist ([`skills/plim-accessibility/SKILL.md`](skills/plim-accessibility/SKILL.md)).
4. **Question generic patterns** — card soup, arbitrary spacing, ad-hoc rounding, shadows, or colour. Ask what each communicates and require an intentional justification; don’t remove what the product’s system or identity legitimately uses.
5. **Respect human decisions** — recommend when the direction is yours to propose; when a person has decided, raise real risks once and execute their direction well. Human judgment operates within applicable accessibility requirements, which are a constraint, not a preference.
6. **Prefer reasoning over presets** — do not fabricate final tokens, palettes, or scales; follow documented philosophy when available, otherwise mark gaps explicitly.

## Skill selection

Always load `plim-design` first; add others as the task requires.

| Goal | Start here |
| --- | --- |
| Any design decision, or "should this change?" | [`skills/plim-design/SKILL.md`](skills/plim-design/SKILL.md) |
| Improve an existing UI | [`skills/plim-beautify/SKILL.md`](skills/plim-beautify/SKILL.md) |
| Critique only, no edits | [`skills/plim-review/SKILL.md`](skills/plim-review/SKILL.md) |
| Accessibility focus | [`skills/plim-accessibility/SKILL.md`](skills/plim-accessibility/SKILL.md) |
| Responsive layout focus | [`skills/plim-responsive/SKILL.md`](skills/plim-responsive/SKILL.md) |
| Angular + plim-ui, only when in scope | [`skills/plim-ui/SKILL.md`](skills/plim-ui/SKILL.md) |

Worked reasoning: [`examples/case-studies/`](examples/case-studies/).

## Unfinished content

The philosophy, manifesto, skills, and `anti-patterns/` are written; `anti-patterns/` is supporting depth, not an additional rule source. Other supporting directories (`foundations/`, `composition/`, `interaction/`, `accessibility/`, `patterns/`, `integrations/`, most `recipes/`) still contain `> TODO` placeholders. Do not treat them as authority and do not fill them with invented “official” Plim rules; rely on the philosophy and skills, and state uncertainty where they are silent.
