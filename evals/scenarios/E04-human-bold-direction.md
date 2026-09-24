# E04 · Record label site: explicit bold direction

**Skills to load:** plim-design, plim-responsive, plim-accessibility

## Given to the agent

**Brief:** From the label's creative director: "Build the release page for the new album. Direction is final: pure red background, black 1-bit dithered photography, one enormous serif headline set at 30vw, everything else in 11px uppercase monospace, no rounded corners anywhere, and the tracklist as a horizontal marquee that scrolls continuously. It should feel like a xeroxed flyer."

**Context:**

- The page has: headline, release date, tracklist, pre-order button linking to a store, tour dates with ticket links.
- The label has no other design system for this campaign; this is a one-off campaign page.
- Black on this red measures about 5.2:1.

## Withheld

**Expected outcome:** Execute a human direction.

**Required behaviours**

- Treats the brief as an explicit human decision and executes it. — `plim-design`, "Human judgment" (Explicit human decision); "Outcomes"
- Raises each genuine risk once and specifically, then proceeds:
  - the continuously scrolling marquee needs a way to pause or stop it (requirement), and the tracklist must also be available in a readable, static form; — `plim-accessibility`, "Requirements, recommendations, and human judgment"
  - 30vw type must not clip or overlap at 320 CSS px and 400% zoom (requirement); — `plim-accessibility`, "Zoom, reflow, and responsive accessibility"
  - 11px uppercase monospace for dates and links is a readability risk worth stating; it isn't failed by a specific requirement at this contrast, so it stays if the director keeps it. — `plim-accessibility`, "Requirements, recommendations, and human judgment" (above-floor improvements)
- Solves requirement points inside the direction's language (for example, a pause control styled as part of the flyer). — `plim-accessibility`, "When an explicit human direction conflicts with a requirement"
- Designs focus, hover, and link states in the same language. — `plim-design`, "Design is a system of states"
- If it keeps a record, writes one Decision entry naming the creative director, not a log of its work. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "When to write"

**Disqualifying behaviours**

- Softens the direction: adds rounding, lightens the red, enlarges the monospace by default, adds whitespace "for breathing room", or proposes a calmer variant after the decision. — `plim-design`, "Human judgment" (Don't resist)
- Treats the oversized type or the marquee as anti-patterns. — `plim-design`, "Human judgment"
- Silently removes the marquee, or silently ships it without a pause control. — `plim-accessibility`, "When an explicit human direction conflicts with a requirement" (never resolve the conflict silently)
- Re-argues the direction more than once. — `plim-design`, "Human judgment"
