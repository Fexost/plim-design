# "Make this premium"

**Skills:** plim-beautify · **Stress test:** Scenario E · **Outcome:** targeted improvement, plus an expression proposal for the founder

## Context

A B2B invoicing product for small accounting firms. The founder says: "We're raising prices. Make the app look premium." The goal behind the adjective is legitimate: customers should feel the product is worth more, at a glance as well as in use. The product has a logo and a single brand blue, but no documented identity beyond that. Its invoices, which accountants send to their own clients, use a plain default template.

## What the agent notices

- "Premium" is an adjective, not a decision, so it needs interpreting against evidence: the audience (accountants and their clients), the price rise, and the founder's goal.
- **Important, accidental.** Three button styles are used for the same kind of action.
- **Important, accidental.** The invoice editor is crowded: figures are unaligned and the total doesn't stand out.
- **Important, accidental.** Loading screens are blank and error messages are generic.
- **Polish, accidental.** Spacing departs from the product's own scale in several places.
- **Important, identity gap.** Nothing about the product, or the invoices it produces, looks particular to it. For a price rise, that gap has a real consequence: the product doesn't look like what it's about to cost.

## Principles and tension

Premium as considered, coherent, precise, trustworthy, polished, appropriate (§21). Craft (§8.16), Confidence (§8.13), Character (§8.15), Beauty as an outcome (§3).

**Restraint ↔ Expression.** Craft alone won't change how the product reads at a glance. Borrowed luxury signals could undermine trust with this audience.

## Alternatives considered

- **Luxury restyle** (dark mode, gold accents, glass, oversized type). Rejected for this audience: these signal consumer luxury, and accountants are more likely to read them as style over substance. For a different product and audience, a similar direction could be right.
- **Craft only.** Rejected as the whole answer: it fixes real findings but leaves the identity gap, which is the part the founder's goal depends on.
- **Craft plus a deliberate identity.** Chosen. The identity direction is a brand decision, so the agent proposes it and the founder decides.

## Decision

For this product, fix the craft findings, and present two or three identity directions for the founder to choose from. The options might include a more distinctive typeface for headings and figures, a considered secondary colour for brand moments, and a designed invoice template, since invoices are the surface clients actually see. The agent states its reading of "premium" in one sentence and asks the founder to confirm.

## Trade-off accepted

The first release looks refined rather than dramatically different. Its visible identity arrives with the founder's chosen direction instead of the agent's guess.

## Implementation direction

- Unify action hierarchy into one primary, one secondary, and one low-emphasis style.
- In the invoice editor, align figures on tabular numerals, right-align amounts, group line items against totals, and make the total the focal point.
- Replace blank loading with structural placeholders; write specific, recoverable error messages.
- Refine typography by role and bring spacing back to the existing scale.
- Add details that signal care: saved-state confirmation, undo for deleting line items.
- Once the founder chooses, apply the identity direction through the theme, including the invoice template, and verify contrast.

## Expected result

The product feels more expensive in the way its customers value (exact, dependable, finished), and it now looks like a particular product rather than a template. The founder chose its character.
