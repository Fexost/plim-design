# Mobile checkout

**Skills:** plim-design, plim-responsive, plim-accessibility · **Outcome:** structural intervention (narrow layouts)

## Context

An e-commerce checkout, mostly used on phones, in three steps: shipping, payment, review. Mobile abandonment is much higher than desktop. The desktop layout and the brand's visual language are not in question.

## What the agent notices

- **Important, accidental.** The desktop two-column layout collapses into one long page with the order summary first, pushing the form below the fold. "Place order" sits at the very bottom. The layout shrank; it didn't adapt.
- **Important, accidental; accessibility requirement.** Personal-data fields lack autocomplete attributes, which the input-purpose requirement covers. Generic text inputs also bring up the wrong keyboards (an improvement, not a requirement).
- **Important, accidental.** A failed payment clears the card fields, so people are punished for a system error.
- **Polish or Important, depending on data.** Validation fires on every keystroke. Error text is present, so the requirement is met; the timing is an above-floor improvement.

## Principles and tension

Adaptability (§8.9), Confidence (§8.13), Agency (§8.3), Design for reality (Law 6).

**Simplicity ↔ Capability.** Hiding the order summary simplifies the screen but removes the confidence of knowing what you're paying for.

## Alternatives considered

- **Hide the summary on mobile.** Rejected: people lose track of what they are paying.
- **Add a separate summary step.** Rejected: it adds a step to the flow that is already losing people.
- **A sticky total at the top.** Considered; it competes with the form on short screens. A collapsed summary with the total, plus the total beside "Place order", keeps the information without the competition.

## Decision

For this checkout, recompose the narrow layout around the task, keep the total always visible, and make failure recoverable. Wider layouts stay as they are.

## Trade-off accepted

The itemised summary is one tap away on phones rather than always visible.

## Implementation direction

- On narrow screens, put the form first, with a collapsed summary showing the total and an expand control.
- Use correct input types and autocomplete tokens (email, telephone, postal code, card number).
- Validate on blur and on submit; on submit, summarise errors and move focus to the first one.
- On payment failure, keep entered data, explain what happened in plain language, and offer a retry or another method.
- Keep "Place order" reachable, with the total beside it, and a loading state that prevents double submission.
- Check thumb reach, zoomed text, and landscape height.

## Expected result

Checkout on a phone feels short and trustworthy. People know what they're paying, type less, and recover from errors without starting over.
