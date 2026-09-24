# "Make this modern"

**Skills:** plim-beautify, plim-responsive · **Outcome:** structural intervention

## Context

A public library's catalogue and account site. A board member says it "doesn't look modern". The audience is broad: older patrons, students, people on shared public computers and cheap phones. The board's concern is legitimate: a public institution whose site looks unmaintained loses trust and visibility.

## What the agent notices

- "Modern" is an adjective to interpret. The evidence points to two meanings here: behaving well on contemporary devices, and looking cared-for.
- **Critical, accidental.** Search results don't work on phones, and phones are a primary device for part of the audience.
- **Critical, accidental; requirement.** Text is small and doesn't reflow at high zoom; table-based layouts force horizontal scrolling.
- **Important, accidental.** A mega-menu of 60 links, and renewing a loan takes five steps.
- **Important, identity gap.** The visual language looks unmaintained, which is the board member's observation and matches patron feedback.
- The tasks that matter most are search, reserve, and renew.

## Principles and tension

Modern as appropriate response to contemporary users and contexts (§21), Against trend-driven design (§16), Purpose (§8.1), Adaptability (§8.9), Inclusion (§8.10).

**Innovation ↔ Familiarity.** Long-time patrons know the current site; the board wants a visible renewal.

## Alternatives considered

- **Trend-led restyle** (glassy hero, bento grid, big gradient headings, animation). Rejected for this audience: it adds weight on low-end devices and shared computers, doesn't fix the tasks, and is tied to a moment.
- **Fix behaviour only, keep the look.** Rejected: it ignores a legitimate identity finding. The board is right that appearance matters here.
- **Restructure around the core tasks, with a visual refresh in the library's own identity.** Chosen.

## Decision

For this site, modernise the experience around the three core tasks, and refresh the visual language as part of the same work. The agent proposes this interpretation to the requester, and offers visual directions drawn from the library's existing identity (its logo, signage, and printed materials) for the board to choose from.

## Trade-off accepted

Patrons have to relearn navigation. Familiar labels and a short "what's changed" note soften it.

## Implementation direction

- Make search the focal point of the home page; group the 60 links into a small number of clear sections.
- Rebuild search results to adapt on narrow screens: title, author, availability, and a reserve action per result, with filters in a disclosure panel.
- Reduce renewal to one step from the account page, with clear confirmation.
- Raise base text size, fix reflow, and apply the chosen visual direction through a small set of shared styles.
- Keep pages light for slow connections and shared computers.

## Expected result

The site looks current and behaves like a current site: readable, fast, usable on a phone, quick for everyday tasks, and recognisably the library's.
