# E12b · The same table: occasional public users

**Skills to load:** plim-design, plim-review, plim-responsive, plim-accessibility · **Pair:** [E12a](E12a-dense-table-experts.md)

## Given to the agent

**Brief:** "The declarations table looks cramped. Should we give it more room?"

**Context:**

- The same table as in E12a (16 columns, about 50 rows visible, 28px rows, compact type, sorting and filtering), now in a government portal where individuals check the status of a parcel they imported.
- Users visit once or twice a year. Most have one or two declarations. They look up their own declaration by reference and want to know its status and whether duty is owed.
- Observed in session recordings: users scroll horizontally hunting for the status column; many search support for "what does status HLD mean"; on phones the table is unusable. Support contacts about the page are the portal's third highest.
- Status uses colour alone; targets are 24px high.

## Withheld

**Expected outcome:** Structural intervention (the page is recomposed around looking up one declaration).

**Required behaviours**

- Concludes that this density doesn't fit this task and audience, reasoning from frequency, expertise, and the lookup task, with the recorded evidence. — `plim-design`, "Choosing density"
- Changes the composition rather than only the padding, for example a lookup by reference leading to a detail view that shows status and duty in plain language. — `plim-responsive`, "Surfaces" (Tables: lookup of single records); `plim-design`, "Simplicity ↔ Capability" row
- Fixes status by colour alone and explains status codes in words. — `plim-accessibility`, "How accessibility shapes design decisions"
- Makes it work on phones. — `plim-responsive`, "Reasoning procedure"

**Disqualifying behaviours**

- Keeps the dense table unchanged because density is "legitimate". — `plim-design`, "Choosing density"
- Only increases row padding. — `plim-responsive`, "Failure modes" (shrinking instead of recomposing)

**Pair check:** An agent that gives E12a and E12b the same answer fails the pair.
