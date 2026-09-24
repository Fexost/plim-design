# E08 · Three greenfield briefs: foundations from evidence

**Skills to load:** plim-design

Run the three briefs in **separate fresh sessions**, then grade them together.

## Given to the agent

**Brief (same wording each time):** "We're starting a new product. Propose its design foundations: typography, spacing and density, colour roles, shape, elevation, and motion, with a reason for each."

**Context A:** A regional savings bank's app for existing customers, many over 60. Tasks: check balances, move money between own accounts, pay bills. Brand: a 120-year-old institution with a heritage serif logotype and deep green. Trust and calm matter; mistakes with money are costly.

**Context B:** A three-day electronic music festival's app for 18–30-year-olds. Tasks: lineup, personal schedule, maps, clashes, push alerts for set changes. Used outdoors, at night, often one-handed in crowds. Brand: not yet defined; the organisers want it "to feel like the festival".

**Context C:** A hospital ward's handover tool for nurses, on wall screens and tablets, used at shift change for 20–30 patients at once, often interrupted. No brand beyond the hospital's logo; the hospital has an accessibility policy requiring WCAG 2.2 AA.

## Withheld

**Expected outcome:** Three rationales, each derived from its own evidence.

**Required behaviours**

- The three sets of foundations differ materially, and each difference traces to evidence in its brief (audience, task, environment, brand). — `plim-design`, "Greenfield failure modes" (the bank, festival, and hospital test)
- Density is chosen per context: likely focused for the bank's money movement, dense and scannable for the handover list, glanceable and large-target for the festival outdoors. Any choice is acceptable if it is reasoned from the brief. — `plim-design`, "Choosing density"
- For B, where brand is undefined, the agent asks or proposes two or three directions with reasons, rather than filling the gap with a neutral default. — `plim-design`, "Start from evidence" (brand is a human decision)
- For A, uses the existing brand assets and treats familiarity as dominant for money movement. — `plim-design`, "Familiarity and identity"
- Resolves at least one tension explicitly per brief and says which side leads and why. — `plim-design`, "Resolve the tensions explicitly"
- Builds only the scales and roles the current decisions need. — `plim-design`, "Avoid premature proliferation"
- Records each rationale as a Foundation entry, or proposes to. — [`decision-records.md`](../../skills/plim-design/decision-records.md)

**Disqualifying behaviours**

- Near-identical foundations across the three (for example, the same neutral palette, radius, spacing scale, and card layout with only the brand colour swapped). — `plim-design`, "Greenfield failure modes"
- Describing any set as "the Plim style" or a Plim default. — `plim-design`, "When there is no system to preserve"
- A full token and component library before any screen exists. — `plim-design`, "Avoid premature proliferation"
- Inventing a brand for B and presenting it as decided. — `plim-design`, "Human judgment"
