# Beautiful but inaccessible interface

**Skills:** plim-accessibility, plim-review · **Outcome:** targeted improvement

## Context

A boutique hotel booking site with an admired visual design: pale grey text on off-white, hairline borders, focus outlines removed, icon-only navigation, and a full-screen background video behind the booking form. The brand owner describes the intent as calm, light, and luxurious. Guests using screen readers, keyboards, or older phones struggle to book; complaints include "can't read the dates" and "the form doesn't work with the keyboard".

## What the agent notices

The aesthetic intent is legitimate and part of the brand. Several of its executions fail accessibility requirements, which makes them Critical findings even though they are intentional.

- **Critical, intentional; requirement.** Body text and date labels fall below text contrast; input borders fall below non-text contrast.
- **Critical, intentional; requirement.** Focus outlines were removed, so keyboard users can't see where they are.
- **Critical, accidental; requirement.** The custom date picker can't be operated by keyboard.
- **Critical, accidental; requirement.** Navigation icons have no accessible names.
- **Important, intentional; requirement.** The background video plays continuously with no way to pause it, and it reduces the form's legibility.
- **Recommendations, above the floor:** visible navigation labels, and pausing the video under reduced-motion preferences. The brand owner may decline these.

## Principles and tension

Inclusion (§8.10, §22), Respect the person (Law 5), Semantic honesty (§8.11).

**Restraint ↔ Expression,** and aesthetic intent against access. The requirements constrain how lightness is achieved, not whether the site may be light.

## Alternatives considered

The agent offers the brand owner accessible options rather than one fix:

- **Text:** a warm grey darkened to pass contrast, keeping lightness through line height and weight; or pale grey kept for large display text (which has a lower threshold) with darker body text; or a slightly deeper background that lets the grey stay softer.
- **Focus:** a thin offset ring in the accent tone, or an underline-and-tint treatment in the brand's hairline style.
- **Video:** the form on a solid panel over the video, or the video moved beside the form.
- **Rejected: a generic accessible restyle** (darker, heavier, boxier). It would meet the requirements and discard the brand for no reason.

## Decision

For this site, the requirements hold, and the calm, light intent is kept through the option the brand owner chooses in each case.

If the brand owner rejected every text option and insisted on the original pale body text, the agent would still implement everything else, leave the body text colour unimplemented, and record it as an open decision: which requirement it fails, who it excludes, and the options offered. The agent would not ship it as though it passed.

## Trade-off accepted

Text is somewhat darker than the original, and a focus indicator is visible where there was none. Most of the airy quality is kept.

## Implementation direction

- Apply the chosen text and border treatments, verified against contrast in every state.
- Restore focus everywhere in the chosen treatment.
- Replace the date picker with an accessible pattern (native input or a well-tested accessible component), styled to match.
- Give navigation icons accessible names, plus visible labels on larger screens if the brand owner accepts the recommendation.
- Add a pause control to the video; pause it by default under reduced motion if accepted.

## Expected result

The site still feels calm and luxurious. Guests can read it, operate it by keyboard and screen reader, and book without friction. The visual quality most people noticed survives; the barriers are gone.
