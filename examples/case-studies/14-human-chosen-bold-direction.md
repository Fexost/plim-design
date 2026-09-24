# Human-chosen bold direction

**Skills:** plim-design, plim-responsive, plim-accessibility · **Outcome:** execute the chosen direction

## Context

A contemporary art museum is building a microsite for an exhibition about protest posters. The design lead gives an explicit brief: oversized condensed type that fills the viewport, a black and acid-green palette, heavy 3px black rules, zero corner radius, an intentionally off-grid collage layout, and an image trail that follows the cursor. "It should feel like a wall of flyposting, not a museum website."

Left to itself, the agent would not have chosen this direction. That is not a finding.

## What the agent notices

- This is an explicit human decision about aesthetic direction and emotional character, grounded in the exhibition's subject. It is legitimate.
- Most of it is accessible as specified: acid green on black has very high contrast, and heavy rules and zero radius have no accessibility consequence.
- A few details affect requirements or robustness, and the agent raises each once:
  - **Reflow (requirement).** Viewport-filling type can clip at 320 CSS px and at high zoom. Fluid sizing keeps the scale while fitting the width.
  - **Reading and focus order (requirement).** The collage layout must not scramble the reading order for keyboard and screen reader users. The source order follows the intended reading sequence; the collage is achieved through placement.
  - **Cursor trail.** It's pointer-only decoration, so no information can live only there. Disabling it under reduced-motion preferences is recommended; its cost on low-end phones is a technical note.
  - **Scope question.** Does the direction extend to the ticket purchase flow? The design lead answers: yes, except the third-party payment embed, which keeps its own styling.

## Principles and tension

Human judgment (Law 8), Character (§8.15), Identity without imposition (§15), Inclusion (§8.10), Adaptability (§8.9).

**Restraint ↔ Expression.** The human resolved it, towards expression. The agent's job is to execute that resolution well.

## What the agent does not do

- Soften the palette, add rounding, or add whitespace "for breathing room".
- Propose a "calmer" variant of the direction after the decision is made.
- Treat the collage or the oversized type as anti-patterns. They are the brief, not ad-hoc additions.
- Collapse the collage into a generic single-column stack on phones.

## Decision

For this microsite, execute the brief as given, and solve the requirement points inside its language.

## Trade-off accepted

The cursor trail costs some performance on low-end devices; the design lead accepts it. Fluid type is slightly smaller at the narrowest widths than a fixed viewport-width size would be.

## Implementation direction

- Fluid type with a floor and a ceiling, so headlines fill the viewport at every width without clipping or overlapping.
- A collage grid on wide screens and a re-composed, still off-grid, collage on narrow screens, with source order matching the reading order.
- Focus indicators designed in the direction: a thick acid-green outline with a black offset, visible on every surface.
- Hover and active states that use the same hard, high-contrast language.
- States for sold-out sessions, loading ticket availability, and failed requests, in the same voice.
- A cursor trail that runs only for fine pointers, doesn't block interaction, and is disabled under reduced motion.

## Expected result

The site feels like a wall of flyposting, as the design lead intended. People can read it at any zoom, use it by keyboard and screen reader, and buy tickets. Nothing was quietly tamed.
