# E02 · Log viewer: polish only

**Skills to load:** plim-design, plim-review, plim-beautify, plim-accessibility

## Given to the agent

**Brief:** "Make the log viewer prettier."

**Context:**

- A developer tool's web log viewer: monospaced type, dark near-monochrome palette, one accent (amber) used only for warnings, dense lines, keyboard navigation (j/k, / to search).
- Its users are engineers who use it for hours during incidents and describe it as fast.
- No brand guidelines beyond the logo and the amber.
- Observations you can verify in the code:
  - The spacing between log groups uses 12px in two places and 16px elsewhere; the spacing scale defines 16px for this relationship.
  - The focused line and the hovered line use the same background, so keyboard users can't tell focus from pointer position.
  - The timestamp column truncates at 200% text size, clipping the seconds.
- Contrast, headings, and accessible names meet requirements.

## Withheld

**Expected outcome:** Polish only (or targeted improvement, if the agent treats the truncation at 200% text size as a requirement failure; either is acceptable if the reasoning is stated).

**Required behaviours**

- States the outcome and its reason before editing. — `plim-design`, "Outcomes"
- Interprets "prettier" against the product's identity before acting, and treats the restraint as intentional with its purpose served. — `plim-beautify`, "First, interpret the request"; `plim-review`, "Classify findings" (Intent)
- Fixes the three observations, each traced to a finding: the spacing inconsistency against the tool's own scale, the focus/hover collision, and the clipping. — `plim-beautify`, "Decide the outcome" (every intervention traces to a finding)
- Classifies the clipping at 200% text size as an accessibility requirement failure, and does not leave it in place. — `plim-design`, "Outcomes"; `plim-accessibility`, "Requirements, recommendations, and human judgment"
- Offers any extra character as the user's choice, in the tool's own language, rather than applying it. — `plim-design`, "Human judgment"

**Disqualifying behaviours**

- Adds decoration unconnected to a finding: gradients, cards, rounded containers, illustration, larger type, or new accent colours. — `plim-beautify`, "Clichés: ask what they communicate"
- Files "it could use more whitespace" or similar taste as Polish. — `plim-review`, "Classify findings" (taste alone is never Polish)
- Reduces density. — `plim-design`, "Choosing density"
