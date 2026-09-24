# E05 · Energy-trading dashboard on a mature system

**Skills to load:** plim-design, plim-review, plim-accessibility

## Given to the agent

**Brief:** "Review the positions screen. Be honest; we suspect it's got the usual AI-dashboard problems."

**Context:**

- An energy-trading firm's internal platform, built on a documented in-house design system with a public documentation site, tokens, and usage rules. Twelve teams use it.
- The system defines: KPI tiles (bordered, same size, a large figure and a delta) for the top of monitoring screens; dense data grids with zebra striping and borders; status pills with text labels; elevation only for overlays.
- The positions screen has, in order: six KPI tiles, a positions grid, and a news panel.
- Observations:
  - The six tiles follow the system's KPI tile rules exactly. Traders use them to check exposure at a glance.
  - One tile shows "Total positions" and another "Positions count", with the same figure.
  - A "Close all positions" action is styled as a status pill in the grid toolbar.
  - The news panel uses a hard-coded shadow not in the tokens.
  - The grid's negative P&L is shown in red text only.

## Withheld

**Expected outcome:** Targeted improvement.

**Required behaviours**

- Identifies the tiles, grid borders, zebra striping, and pills as documented system conventions, and judges their use rather than their resemblance to dashboard or card anti-patterns. — `plim-design`, "A documented system is the product's vocabulary"; `plim-review`, "Classify findings" (last paragraph)
- Reports the duplicated tile as a finding (Polish or Important, with reason). — `plim-review`, "Evidence discipline"
- Reports "Close all positions" as a pill misused for a consequential action: at least Important, and connects it to consequence (a batch, possibly irreversible action). — `plim-design`, "Semantic honesty"; "Automation and agency"
- Reports red-only P&L as an accessibility requirement failure. — `plim-accessibility`, "How accessibility shapes design decisions" (Colour)
- Reports the hard-coded shadow as Polish against the system. — `plim-review`, "Classify findings" (Polish)
- Recommends one outcome from the canonical scale and lists the requirement failure there. — `plim-review`, "Report shape"

**Disqualifying behaviours**

- Reports "dashboard syndrome", "card soup", or "too many borders" as findings about the system's conventions. — `plim-design`, "A documented system is the product's vocabulary"
- Recommends flattening, removing the tiles, or reducing density. — `plim-review`, "Failure modes"
- Edits code (this is a review). — `plim-review`, "When to use"
