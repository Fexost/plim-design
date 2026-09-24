# Mobile checkout

**Skills:** plim-design, plim-responsive, plim-accessibility

## Context

An e-commerce checkout, mostly used on phones. It works as three steps: shipping, payment, review. Abandonment on mobile is high.

## Existing problem

The desktop two-column layout collapses into one long page where the order summary comes first, pushing the form below the fold. The "Place order" button sits at the very bottom. Fields use generic text inputs, so phones show the wrong keyboards. Validation fires on every keystroke with red text. A failed payment clears the card fields.

## What the agent notices

- The layout shrank; it didn't adapt. On mobile the primary task (completing the form) should lead, with the summary available but secondary.
- Input types and autocomplete attributes would remove much of the typing.
- Validation timing creates anxiety before users have finished typing.
- Clearing data after a payment failure punishes the user for a system error.

## Relevant Plim principles

Adaptability (§8.9), Confidence (§8.13), Agency (§8.3), Respect the person (Law 5), Design for reality (Law 6).

## Tension

**Simplicity ↔ Capability.** Hiding the order summary simplifies the screen but removes the confidence of knowing what you're paying for.

## Decision

Recompose for mobile around the task, keep the summary one tap away with the total always visible, and make failure recoverable.

## Implementation direction

- On narrow screens, put the form first; show a collapsed summary with the total and an expand control.
- Use correct input types and autocomplete tokens (email, telephone, postal code, card number) so the right keyboards and autofill appear.
- Validate on blur and on submit; on submit, summarise errors and move focus to the first one.
- On payment failure, keep all entered data, explain what happened in plain language, and offer a clear retry or alternative method.
- Keep "Place order" reachable, with the total repeated beside it; show a loading state that prevents double submission.
- Check targets for thumb reach, zoomed text, and landscape height.

## Expected result

Checkout on a phone feels short and trustworthy. Users know what they're paying, type less, and recover from errors without starting over.
