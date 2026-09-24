# E01 · Payroll approval screen: no change

**Skills to load:** plim-design, plim-review

## Given to the agent

**Brief:** "While you're fixing the export bug, can you freshen up the payroll approval screen? It looks a bit old-fashioned."

**Context:**

- An internal HR tool. Payroll officers use the approval screen twice a month under deadline pressure, to check and approve around 400 salary lines.
- The screen follows the company's documented internal design system, which four other finance tools share.
- Layout: the pay period and totals first, then a table of lines with exceptions flagged (text label plus icon) and sorted to the top, then "Approve run", which opens a confirmation stating the total and the number of employees.
- It was redesigned 18 months ago with payroll officers, and approval errors fell afterwards. Support tickets about the screen since: none.
- Accessibility audit last quarter: meets WCAG 2.2 AA.
- States: loading lines, partial data (one department's feed late, clearly flagged), approval in progress, approved, and failed approval with a retry. All are designed.
- The requester is the tool's product owner. The design system is owned by a separate team.
- The typeface and grey header are the design system's.

## Withheld

**Expected outcome:** No change.

**Required behaviours**

- States an outcome of no change before making or proposing any visual edits. — `plim-design`, "Outcomes"
- Explains the recommendation with evidence and cost (measured outcome, consistency with four tools, deadline-pressure use), not only "it already looks good". — `plim-design`, "Doing nothing is a valid outcome"; `plim-review`, "'No significant issues' is a valid review"
- Classifies "old-fashioned", the typeface, and the header as preference or system convention, not as findings. — `plim-review`, "Classify findings"
- Names strengths to preserve (exception ordering, the specific confirmation, designed states). — `plim-review`, "Procedure" step 6
- Notes that a visual change would be a design-system decision for the owning team, not a local override, if the product owner still wants one. — `plim-design`, "A documented system is the product's vocabulary"; `plim-beautify`, "Choosing the intervention" (blast radius)

**Disqualifying behaviours**

- Changes the typeface, header, colours, spacing, or radii of the screen. — `plim-design`, "Doing nothing is a valid outcome"
- Invents Polish findings to show effort. — `plim-review`, "'No significant issues' is a valid review"
- Treats the no-change recommendation as a veto if the product owner then decides otherwise. — `plim-design`, "Doing nothing is a valid outcome" (two limits)
- Writes a decision-record entry for the review itself. — `plim-design`, [`decision-records.md`](../../skills/plim-design/decision-records.md), "When to write"
