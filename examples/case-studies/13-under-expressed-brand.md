# Under-expressed brand

**Skills:** plim-design, plim-review, plim-beautify, plim-accessibility · **Outcome:** targeted improvement (identity)

## Context

An outdoor-adventure cooperative's member app, used to browse and book guided trips. The co-op's brand is documented and distinctive: a rugged display typeface, a deep forest green and a signal orange, hand-drawn trail-map illustration, and a warm, direct voice. Its website and printed trip guides use all of it.

The app was built quickly on shadcn/ui with the default theme: neutral greys, the default font and radius, no illustration, and generic copy. It is usable, accessible, and internally coherent. The co-op's brand lead asks: "The app doesn't feel like us. Can you help?" A member survey says the app "could be any booking app" and "feels like a bank".

## What the agent notices

- **None.** Usability, states, and accessibility are sound. No Critical findings.
- **Important, identity gap.** The evidence is concrete: documented brand guidelines, the survey, and a visible mismatch with the co-op's other surfaces. The app is under-expressed for its purpose, which is partly to make members feel part of the co-op.
- shadcn is the app's system. Its theming variables (colours, radius, font) are the intended way to carry a brand, so identity can come through the system rather than around it.
- Not every screen carries identity equally. Trip pages, booking confirmation, onboarding, and empty states are where members meet the brand. Payment and account settings are where they need plain confidence.

## Principles and tension

Character (§8.15), Identity without imposition (§15), Familiarity ↔ Identity and Restraint ↔ Expression (§9), Semantic honesty for brand treatments.

**Restraint ↔ Expression**, resolved towards expression for this product, because the evidence says the restraint was accidental rather than chosen.

## Alternatives considered

- **No change, because the app works.** Rejected: an evidenced identity gap is a real finding, and usability is not the only outcome that matters here.
- **Generic "vibrant" additions** (gradients, blobs, glass). Rejected: they aren't the co-op's language and would replace one generic look with another.
- **A full custom redesign.** Rejected as agent-initiated: the components and flows work. Theming and targeted composition can close the gap.
- **The brand at full intensity everywhere.** Rejected: payment and settings benefit from clarity, so intensity varies by moment.
- **Theme the system in the brand's language, and give the brand room at the moments that carry identity.** Chosen, with the brand lead reviewing directions before rollout.

## Decision

For this app, adding character is the improvement. The agent proposes two directions built from the co-op's own assets, which differ in how far illustration and the display face are pushed. The brand lead chooses.

## Trade-off accepted

Some screens carry more visual weight than before. The theme change has a wide blast radius, because every component restyles, so it is checked across all screens and states before release.

## Implementation direction

- Set the shadcn theme variables from the brand: colour roles from the forest green and orange, the brand typeface for headings, a radius that suits the brand's sturdier shapes.
- Give trip pages room for photography, trail-map illustration, and the display face.
- Make booking confirmation a moment, with the brand's voice, illustration, and, if the brand lead wants it, a brief celebratory transition.
- Write empty states and onboarding in the co-op's voice.
- Keep payment and account screens in the themed system, without added illustration.
- Accessibility requirements: signal orange doesn't pass text contrast on white, so it's used for large display text, non-text elements that pass 3:1, or a darker text shade. Illustrations that carry no information are marked decorative. Reducing the confirmation motion under reduced-motion preferences is recommended.

## Expected result

Members recognise the co-op in the app as they do in its guides. Booking is as clear as before, and the moments that matter feel like the organisation they joined.
