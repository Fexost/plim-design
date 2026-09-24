# E11a · Settings screen with a documented signature gradient

**Skills to load:** plim-design, plim-review, plim-beautify · **Pair:** [E11b](E11b-gradients-ad-hoc.md)

## Given to the agent

**Brief:** "Make the workspace settings screen look more professional."

**Fixtures:** [`fixtures/e11-settings/`](../fixtures/e11-settings/): `index.html`, `tokens.css`, `settings.css`, and `brand-system.md`.

**Context:** Northwind is a design-agency project tool. The brand system excerpt in `brand-system.md` is the company's published brand documentation.

## Withheld

**Expected outcome:** Targeted improvement, scoped to the destructive action. The gradient headers and pill buttons stay.

**Required behaviours**

- Reads `brand-system.md` and identifies the Aurora gradient on headers and primary actions, and the pill buttons, as documented system conventions used as intended: None, intentional. — `plim-design`, "A documented system is the product's vocabulary"
- Reports "Delete workspace" as Critical: styled as a primary (Aurora) action, which the system forbids for destructive actions, and it deletes with no confirmation. — `plim-review`, "Classify findings"; `plim-design`, "Automation and agency" (Destructive actions)
- Fixes it within the system: the danger role, and a confirmation that names what will be lost (all projects and files, for every member). Adds the danger token only because the system defines that role and the tokens lack it. — `plim-beautify`, "Choosing the intervention" (rung 6); `plim-design`, "Semantic honesty"
- Interprets "professional" against evidence and states the interpretation before changing anything. — `plim-beautify`, "First, interpret the request"

**Disqualifying behaviours**

- Removes or softens the gradient headers or pill buttons, or replaces them with a flat or square treatment. — `plim-design`, "A documented system is the product's vocabulary"
- Cites "excessive gradients" or "excessive pills" as findings. — `plim-beautify`, "Clichés" (the table targets ad-hoc additions)
- Leaves the delete action without confirmation. — `plim-design`, "Outcomes" (Critical findings override the outcome)
