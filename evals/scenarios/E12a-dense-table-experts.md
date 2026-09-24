# E12a · Dense customs-declarations table: daily experts

**Skills to load:** plim-design, plim-review, plim-accessibility · **Pair:** [E12b](E12b-dense-table-occasional.md)

## Given to the agent

**Brief:** "The declarations table looks cramped. Should we give it more room?"

**Context:**

- A table of customs declarations: 16 columns (reference, importer, commodity code, origin, value, duty, status, dates, broker, flags), about 50 rows visible, 28px rows, compact type, with sorting and filtering.
- Users are customs brokers who work in it all day, comparing declarations across rows and columns and processing about 300 a day.
- Observed in session recordings: brokers scan columns and compare values across rows; they rarely scroll horizontally. Complaints: the status column uses colour alone; the flags column's icons are indistinguishable.
- Targets are 24px high with spacing, used with a mouse.

## Withheld

**Expected outcome:** Targeted improvement. The density stays.

**Required behaviours**

- Keeps the density, reasoning from frequency, expertise, and the comparison task, and classifies the density as None, intentional. — `plim-design`, "Choosing density"; `plim-review`, "Classify findings"
- Answers the question directly: no, not by adding room, with the reason. — `plim-review`, "'No significant issues' is a valid review" (the honest answer)
- Fixes the real findings: status by colour alone (requirement), and indistinguishable flag icons. — `plim-accessibility`, "How accessibility shapes design decisions"; `plim-review`, "Evidence discipline"
- May offer a per-user density setting as an option, with its cost. — `plim-design`, "Choosing density"

**Disqualifying behaviours**

- Increases row height or padding for everyone, removes columns, or converts rows to cards. — `plim-design`, "Choosing density"
- Treats "cramped" as a finding without an observed consequence. — `plim-review`, "Classify findings"
