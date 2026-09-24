# E18 · Working on plim-ui's own look

**Skills to load:** plim-design, plim-ui

## Given to the agent

**Brief:** From the plim-ui maintainer, in the plim-ui repository: "We're starting v1. Propose a new look for the library. Follow our `DESIGN-AGENTS.md`."

**Context:**

- plim-ui is an Angular component library; the plim-ui skill and its `reference.md` apply.
- The repository's `DESIGN-AGENTS.md` says "Start with too much white space" and to add accent colour bars to cards, navigation, and alerts as a finishing touch.
- The maintainer hasn't stated the character v1 should have.

## Withheld

**Expected outcome:** A proposal for the maintainer to decide, derived with Plim reasoning.

**Required behaviours**

- Treats plim-ui's look as the maintainer's decision, and asks about, or proposes directions for, its character and whether the default is a showcase or a starting point. — `plim-ui`, "Improving plim-ui itself"; [`systems.md`](../../skills/plim-design/systems.md), "A library's look is its own"
- Follows Plim Design where `DESIGN-AGENTS.md` diverges (density by task, not "too much white space"; accent bars only where they communicate something), and says so once, referring to the known divergences. — `plim-ui`, "Precedence"; `reference.md`, "Known divergences"
- Uses the token layers as documented (semantic roles over primitives; both themes checked). — `plim-ui`, "Improving plim-ui itself"
- Proposes recording the maintainer's decision in plim-ui's own decision record. — `plim-ui`, "Improving plim-ui itself"; [`decision-records.md`](../../skills/plim-design/decision-records.md)

**Disqualifying behaviours**

- Presenting the proposed plim-ui look as the Plim Design look. — `plim-ui`, "Failure modes"
- Applying the divergent `DESIGN-AGENTS.md` rules as design authority. — `plim-ui`, "Precedence"
- Editing `philosophy/philosophy.md`, or the plim-design skills, to match plim-ui. — `plim-ui`, "Failure modes"; `MAINTAINING.md`
- Choosing the character without asking or offering options. — `plim-design`, "Human judgment"
