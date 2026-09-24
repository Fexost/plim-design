# E10 · Illustration app: one justified departure, one unnecessary one

**Skills to load:** plim-design, plim-review, plim-accessibility

## Given to the agent

**Brief:** "Review the canvas and export screens of our drawing app before launch."

**Context:**

- A tablet illustration app for professional illustrators, used for hours a day with a stylus. The brand is built on "the canvas is everything".
- Canvas screen: instead of a toolbar, a press-and-hold with the stylus opens a radial tool menu around the stylus tip. It was prototyped with 20 illustrators: after first use, tool switching took about 40% less time than with a toolbar, and people kept their eyes on the drawing. A one-time hint appears the first time the canvas opens. The same tools are also reachable from a collapsible side panel and by keyboard shortcuts with a hardware keyboard.
- Export screen: the date field for a watermark uses a custom rotating-dial picker designed "to match the brand". In a test, 6 of 10 participants hesitated or asked how to enter a date, and screen reader users couldn't operate it. Nothing else in the app uses dials.
- The rest of the app follows platform conventions.

## Withheld

**Expected outcome:** Targeted improvement (replace the date picker; keep the radial menu).

**Required behaviours**

- Keeps the radial menu, with reasons: evidence it does the task better for daily experts, it is taught where it first appears, and there are recognisable alternatives. Classified as None, intentional. — `plim-design`, "Familiarity and identity" (Deviate for identity; Innovation or novelty); `plim-review`, "Classify findings" (Intent)
- Reports the dial picker as an unnecessary learning cost (Important), and as an accessibility requirement failure (not operable with a screen reader). — `plim-design`, "Familiarity and identity" (Remove unnecessary learning cost); `plim-accessibility`, "Requirements, recommendations, and human judgment"
- Directs brand character for the date field through appearance (colour, type, shape) on a familiar or native pattern, not through behaviour. — `plim-design`, "Recognisable behaviour, distinctive character"
- Uses evidence, not "it's standard" or "it's unusual", to decide both. — `plim-design`, "Design intelligence" (Novelty vs value)

**Disqualifying behaviours**

- Recommending a conventional toolbar in place of the radial menu because it is standard. — `plim-design`, "Familiarity and identity"
- Keeping the dial picker because it is on-brand. — same section
- Edits code (this is a review). — `plim-review`, "When to use"
