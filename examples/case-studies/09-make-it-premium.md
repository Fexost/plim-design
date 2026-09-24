# "Make this premium"

**Skills:** plim-beautify · **Stress test:** Scenario E

## Context

A B2B invoicing product for small accounting firms. The founder says: "We're raising prices. Make the app look premium."

## Existing problem

The app is serviceable but uneven: mismatched spacing, three button styles for the same kind of action, a crowded invoice editor, blank loading screens, and generic error messages.

## What the agent notices

- The instinctive "premium" moves (dark mode, gold accents, gradients, glass, oversized type) would signal a luxury consumer brand, not a trustworthy financial tool. They might even reduce trust.
- For accountants, premium is more likely to mean precision, reliability, and care: exact alignment of figures, predictable behaviour, clear states, no rough edges.
- The rough edges are specific and fixable.

## Relevant Plim principles

Definition of premium: considered, coherent, precise, trustworthy, polished, appropriate (§21). Craft (§8.16), Confidence (§8.13), Coherence (§8.5), Beauty as an outcome (§3).

## Tension

**Restraint ↔ Expression.** Some added expression may help the product feel more valued, but it must not undermine trust.

## Decision

State the interpretation to the founder: "premium" here means precision and confidence. Invest in craft and states, not decoration. Offer a small, deliberate expression upgrade (typography refinement, a more considered brand accent) as a separate, optional decision for them to make.

## Implementation direction

- Unify action hierarchy to one primary, one secondary, and one low-emphasis style.
- In the invoice editor, align figures on tabular numerals, right-align amounts, tighten the grouping of line items against totals, and make the total the clear focal point.
- Replace blank loading with structural placeholders; write specific, recoverable error messages.
- Refine typography: fewer sizes and weights, used by role; consistent spacing rhythm from the existing scale.
- Add small interaction details that signal care, such as saved-state confirmation and undo for deleting line items.

## Expected result

The product feels more expensive in the way accountants value: exact, calm, and dependable. The founder has a clear choice about any further brand expression rather than a surprise restyle.
