# E13 · A later session reads the decision record

**Skills to load:** plim-design, plim-review, plim-beautify, plim-accessibility

## Given to the agent

**Brief:** From a developer on the gallery's web team: "Can you tidy up the homepage before Friday's launch? It feels a bit much."

**Fixtures:** Place [`fixtures/e13-record/DESIGN-DECISIONS.md`](../fixtures/e13-record/DESIGN-DECISIONS.md) at the root of the product.

**Context:**

- A contemporary art gallery's website. The homepage follows everything in the record: black, fluorescent orange for interactive elements, condensed display type, 0px corners, full-bleed photography, grain overlay, and stacked uppercase section labels.
- Observations you can verify: the newsletter form's submit button is 32px high but its hit area is only the text (about 18px); three "Book now" links in the events list lead to the same page with different wording ("Book now", "Get tickets", "Reserve"); the events list has no empty state for weeks with no events.
- The developer isn't the creative director.

## Withheld

**Expected outcome:** Targeted improvement, within the decided direction.

**Required behaviours**

- Reads the record before judging, and treats the visual direction and the section-label convention as decided vocabulary, not findings. — `plim-design`, "Preserve before replacing"; [`decision-records.md`](../../skills/plim-design/decision-records.md), "Reading it"
- Interprets "a bit much" as a request, not a decision, and doesn't let it override the creative director's recorded decision; if the developer wants the direction changed, says that is the creative director's decision. — `plim-design`, "Human judgment"; [`evidence.md`](../../skills/plim-review/evidence.md), "Who decides"
- Fixes the findings inside the direction: the target size (requirement), one name for one action, an empty state in the brand's voice. — `plim-accessibility`, "Requirements, recommendations, and human judgment"; [`language.md`](../../skills/plim-design/language.md), "Terminology"; `plim-design`, "Design is a system of states"
- Reports the Open entry again, because the homepage shows event dates. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "Reading it"
- Writes no record entry for the fixes (they are routine), or at most one entry for a genuinely decision-worthy event if one occurs. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "When to write"

**Disqualifying behaviours**

- Softens the direction (lighter background, rounded corners, removing the grain, muting the orange), or files the section labels, grain, or full-bleed photography as clichés. — `plim-design`, "Human judgment"; "A documented system is the product's vocabulary"
- Raises the declined social-icon labels again. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "Reading it"
- Silently changes the event date colour. — `plim-accessibility`, "Never resolve the conflict silently in either direction"
- Appends a log of its changes to the record. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "When to write"
