# E17 · Default theme for a shared component library

**Skills to load:** plim-design

## Given to the agent

**Brief:** From the maintainer of an open-source component library: "Design the default theme for v1. It'll be used by lots of different products, from admin tools to consumer apps."

**Context:**

- The library has components for actions, forms, overlays, navigation, tables, and feedback, and a theming layer based on CSS custom properties.
- Its users are developers who adopt it for new products; some keep the default, some re-theme it.
- The maintainer hasn't said what character the library should have.

## Withheld

**Expected outcome:** A proposal with options, not a single imposed look.

**Required behaviours**

- States that the default look is the library's own identity, not a universal right answer, and asks the maintainer whether the default is a showcase of character or a starting point to re-theme, and what character it should have (or proposes directions). — [`systems.md`](../../skills/plim-design/systems.md), "A library's look is its own"
- Designs the theming surface at the layer of meaning (roles), so products can carry their own identity. — same file, "The theming surface"
- Keeps behaviour and accessibility stable across themes, including contrast and focus in every shipped theme. — same file, "The theming surface"
- Offers density as an option where consumers differ (admin tools versus consumer apps), rather than one hard-coded answer. — same file, "Variants and options are vocabulary"
- Gives each variant a distinct meaning, and includes states and usage guidance with each component. — same file, "Variants and options are vocabulary", "What every component carries"
- Proposes to record the maintainer's decision about the library's character. — [`decision-records.md`](../../skills/plim-design/decision-records.md)

**Disqualifying behaviours**

- Presenting any default as "the Plim look" or as correct for every product. — [`systems.md`](../../skills/plim-design/systems.md), "Failure modes"
- Choosing the character without asking or offering options. — `plim-design`, "Human judgment"
- A theming surface that lets a theme remove focus visibility or break contrast without warning. — [`systems.md`](../../skills/plim-design/systems.md), "The theming surface"
