---
name: plim-ui
description: >-
  Implement Plim Design decisions with the Angular plim-ui component library,
  or improve plim-ui itself using Plim Design. Use only when the project already
  uses plim-ui, the user explicitly asks to use it, or the work is on the
  plim-ui repository. Covers precedence, component selection, composition,
  tokens, variants, states, accessibility, responsive behaviour, and theming.
  Never use it to replace an existing component system.
---

# Plim UI integration

> **Plim UI implements Plim Design principles, but Plim Design does not require Plim UI.**

This is an implementation skill. The reasoning comes from [`plim-design`](../plim-design/SKILL.md) and the other skills; this skill explains how those decisions are expressed with [plim-ui](https://github.com/Fexost/plim-ui), an accessibility-first Angular library built on native HTML, Angular CDK primitives, and `--plim-*` design tokens.

Decide what the interface needs first. Then choose how plim-ui expresses it.

## When to use

- An Angular project already depends on plim-ui.
- The user explicitly asks to build with or adopt plim-ui.
- The work is on the plim-ui repository itself: its components, tokens, or docs.

Do not use this skill to migrate a project from Angular Material, PrimeNG, Bootstrap, Tailwind components, or a proprietary library, and do not suggest plim-ui as an improvement unless asked. If a project mixes plim-ui with another system, preserve both and keep each area coherent.

## Versioned facts

Component names, inputs, and tokens are in [`reference.md`](reference.md), which records the plim-ui version and commit it was verified against. Before relying on a detail:

- compare the installed version with the one recorded in `reference.md`
- if they differ, confirm the detail in the installed public API or styles, and tell the user about any mismatch
- never invent an input or token; if something you need doesn't exist, say so

## Precedence

| Question | Source of truth |
| --- | --- |
| Design decisions: hierarchy, density, emphasis, colour roles, shape, elevation, motion, states | Plim Design: [`philosophy.md`](../../philosophy/philosophy.md) and the skills |
| What plim-ui currently implements | The plim-ui code at the installed version |
| Architecture and code conventions inside plim-ui | plim-ui's `AGENTS.md` |
| plim-ui's local visual guidance | plim-ui's `DESIGN-AGENTS.md`, applied where it agrees with Plim Design |

Where `DESIGN-AGENTS.md` and Plim Design diverge, follow the Plim Design reasoning for the decision, say that you did and why, and check the known divergences in `reference.md`. Do not edit the philosophy or `DESIGN-AGENTS.md` to reconcile them unless the user asks.

## Mapping Plim concepts to plim-ui

Concept-level mapping; exact names are in `reference.md`.

| Plim concept | How plim-ui expresses it |
| --- | --- |
| **Semantic honesty** | Controls are directives on native elements (buttons, inputs, selects, tables). Use each on the correct native element; never put click handlers on styled non-interactive elements. |
| **Action hierarchy** | Button variants (primary, secondary, text). Usually one primary action per context; variant reflects importance and consequence, not decoration. |
| **Attention budget** | Semantic text roles (default, muted, subtle) let you quiet supporting content instead of amplifying headings. Badge and snackbar variants carry status; reserve them for statuses that matter. |
| **Containment** | The card component for genuinely independent units. Group related content with spacing, headings, and separators instead. |
| **Elevation as meaning** | Semantic elevation roles (raised, overlay, modal) and surface roles. The library is predominantly flat; use elevation for things that sit above the page. |
| **Density** | Density tokens, including compact values for tables and lists. Choose density by task, expertise, and frequency of use. |
| **States** | Built-in disabled and loading states on buttons; spinner, progress bar, and skeleton (check the version) for loading; snackbar for transient feedback; form field for label and hint. Empty and error states are composed in the page from these pieces. |
| **Inclusion** | Native semantics first, focus-ring tokens, reduced-motion support in components, and CDK-backed overlays that handle focus and keyboard behaviour. Don't add ARIA over native semantics that already work. |
| **Continuity** | Duration and easing tokens for any custom transition; keep motion explanatory. |
| **Adaptability** | Sidebar push and overlay modes, header and toolbar slots. Page layout and breakpoints are the application's responsibility; apply [`plim-responsive`](../plim-responsive/SKILL.md). |
| **Coherence** | Spacing, type, radius, and colour-role scales. Use them instead of raw values. |

## Tokens and theming

Tokens are layered: primitives feed semantic roles, which feed component tokens.

- In application code, use semantic and component tokens, not primitives.
- Theme at the semantic layer to express the product's brand.
- Add a token rather than hard-coding a value when the system lacks one.
- Check every change in both light and dark themes.

plim-ui's default look is the library's own identity. It is **not** the Plim Design aesthetic, because Plim Design has none. A product built with plim-ui can, and often should, re-theme it to carry its own character (§15).

## Choosing how to build something

Prefer the earliest option that works:

1. An existing component or directive used as documented.
2. Composition of existing components through their slots.
3. Customisation through tokens and theme roles.
4. An application component that composes plim-ui primitives and follows its conventions.
5. A new pattern, raised with the user and possibly proposed upstream.

If you need deep style overrides of component internals, the component may be the wrong choice, or a token may be missing.

## Improving plim-ui itself

When Plim Design is used to improve the library, its tokens, or its docs:

- **Review before changing.** Run [`plim-review`](../plim-review/SKILL.md) on the component or docs page, classify findings, and record what already works.
- **Treat tokens as a system.** A token change affects every consumer. State what relationship it changes, check both themes and all components that use it, and prefer changing semantic roles over primitives.
- **Defaults serve many products.** Library defaults should be restrained enough to be re-themed and dense or spacious enough for the range of tasks the component serves. Where a single default can't serve both, prefer a documented option (such as a compact density) over one hard-coded answer.
- **Keep public APIs small**, following plim-ui's `AGENTS.md`. Add a variant or input only when it expresses a real distinction.
- **States and docs together.** A component change includes its states, its accessibility behaviour, and its docs page.
- **Log divergences.** If plim-ui guidance and Plim Design disagree on a decision, add or update the entry in `reference.md` rather than editing either document.
- **After a release**, update `reference.md` using [`MAINTAINING.md`](MAINTAINING.md).

## Failure modes

- Treating plim-ui as mandatory for Plim Design, or migrating another system to it unasked.
- Using plim-ui's defaults as a product's brand without asking whether the product has its own.
- Wrapping everything in cards.
- Hand-building dialogs, menus, or tooltips that the library already provides accessibly.
- Hard-coded colours, spacing, or radii where tokens exist.
- Inventing inputs or tokens, or relying on `reference.md` without checking the installed version.
- Changing the philosophy or `DESIGN-AGENTS.md` to make a divergence disappear.

## Completion criteria

- Decisions were made with Plim Design reasoning first; plim-ui only expresses them.
- Components are used on the correct native elements with inputs that exist in the installed version.
- Variants and tokens reflect meaning (importance, state, elevation), not decoration.
- States use the library's loading, disabled, and feedback facilities consistently.
- Both themes and keyboard behaviour have been checked.
- Nothing outside the requested scope was migrated to plim-ui.
- Any divergence from plim-ui's own guidance was stated, and logged if it was new.

See [`examples/case-studies/03-angular-settings-plim-ui.md`](../../examples/case-studies/03-angular-settings-plim-ui.md).
