# Highly branded application

**Skills:** plim-design, plim-beautify, plim-accessibility · **Stress test:** Scenario H · **Outcome:** targeted improvement

## Context

A music festival app with a loud, documented brand: saturated magenta and yellow, a condensed display typeface, angled section edges, and playful motion. Ticket-buyer surveys say people choose this festival partly for its energy. The user asks to "improve the UX of the ticket and lineup screens".

## What the agent notices

- **None, intentional.** The brand is an asset, applied consistently from a brand kit, and its purpose (energy, recognisability) is served. It is not a finding.
- **Critical, intentional pairing; accessibility requirement.** Set times are yellow text on magenta and fail text contrast. The palette is intentional; this particular pairing excludes people with low vision from essential information.
- **Important, accidental; accessibility requirement.** Selected stage filters differ from unselected ones by colour alone.
- **Important.** The display face is used at many sizes for dense information. The typeface is intentional, but at small sizes in dense lists its purpose isn't served, so this use doesn't count as intentional under the evidence test.
- **Important, accidental.** On the ticket screen, "Buy" competes with three continuously animated promotional banners. Continuous animation without a pause control also fails a requirement.

## Principles and tension

Character (§8.15), Identity without imposition (§15), attention as a resource (§10), Inclusion (§8.10).

**Restraint ↔ Expression.** Here expression is part of the product's value; unfocused expression is hurting the purchase task.

## Alternatives considered

- **A neutral "clean-up"** (calmer palette, standard type, no angles). Rejected: it removes what users chose the festival for, and none of the findings require it.
- **Change the palette to fix contrast.** Rejected: the pairing fails, not the palette. Dark text on a lighter brand tint passes within the existing colours.
- **Remove motion.** Rejected: motion is part of the character. Only the continuous banner animation needs changing.
- **Leave everything.** Rejected: there is a Critical requirement failure.

## Decision

For this app, keep the expression and aim it. Brand intensity stays and, in places, grows: headliner reveals and transitions can carry more of the brand, because dense information no longer has to. Information and purchasing get clarity.

The number of promotional banners is a commercial decision. The agent recommends one focal promotion and asks the marketing owner.

## Trade-off accepted

The display face appears less in dense lists. Banners animate once, or on request, instead of continuously.

## Implementation direction

- Use the display face for artist names at a few sizes by role (headliner, main stage, other), and the brand kit's text face for times and details.
- Fix set-time contrast with dark text on a lighter brand tint.
- Make selected filters unmistakable through shape and fill as well as colour.
- Give "Buy" the clear focal point. Give animated banners a pause control or play them once. Apply the promotion count the marketing owner chooses.
- Keep playful motion for transitions and celebratory moments; reduce it under reduced-motion preferences (a recommendation the brand owner may decline).

## Expected result

The app still feels unmistakably like the festival, and in its big moments more so. The lineup scans quickly, filter states are clear, and buying a ticket no longer fights the decoration.
