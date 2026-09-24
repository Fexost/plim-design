# Legacy Bootstrap interface

**Skills:** plim-review, plim-beautify · **Outcome:** targeted improvement, staged

## Context

An internal logistics admin built on Bootstrap years ago, customised through Sass variables. It has hundreds of screens maintained by a small team, and staff know it well. Warehouse staff increasingly use it on tablets. The user asks: "It looks dated. Can you modernise it?"

## What the agent notices

- "Dated" is an adjective, not a decision, so it needs interpreting. Evidence points to three meanings here: an inconsistent visual language, noisy alerts, and poor behaviour on warehouse tablets.
- **None, intentional.** Bootstrap and its Sass theme are a real system. Staff familiarity with the layout is an asset.
- **Polish, accidental.** Local overrides fight the theme: pages mix `.card`, panel-style wrappers, and bare tables, and form labels sit in inconsistent positions.
- **Important, accidental.** Alerts appear for trivial messages, so real warnings get ignored.
- **Important, accidental.** Tablet layouts clip tables and use small targets on the warehouse screens.

## Principles and tension

Improve before replacing (Law 7), Modern as appropriate response rather than trend (§21), Familiarity (§8.4), Adaptability (§8.9), Human judgment (Law 8).

**Innovation ↔ Familiarity.** Staff efficiency depends on familiarity; the user wants the product to feel current, which is a legitimate goal.

## Alternatives considered

- **Migrate to a new framework or component library.** Rejected as an agent-initiated move: it's enormous and risky, it would break staff familiarity, and nothing found requires it. If the user explicitly wants a redesign, that's their decision (see [case 16](16-explicit-redesign-request.md)).
- **Restyle screen by screen.** Rejected: hundreds of local changes would create a new inconsistency.
- **Refresh through the Sass theme.** Chosen. It is a small edit with a very wide blast radius, since every screen changes at once, so it's staged and reviewed.

## Decision

For this product, modernise through the existing theme, incrementally, targeting the problems that affect work. First, confirm with the user what "modern" should achieve, which visual direction they want the refreshed theme to take, and whether tablets are a priority.

## Trade-off accepted

The product won't look like a new product. In exchange, it refreshes coherently without retraining staff.

## Implementation direction

- Adjust the Sass theme (typography scale, colour, border and radius values) in the direction the user confirms. Review the change on a representative set of screens and states before rollout, because it affects all of them.
- Remove local overrides that fight the theme, starting with the most-used screens.
- Standardise form label placement and validation messaging.
- Reserve alerts for things that need attention; use inline confirmation for routine success.
- Improve tablet layouts on the warehouse screens: larger targets, and tables that prioritise the columns used on the floor.
- Ship in stages that can be reviewed and reverted.

## Expected result

The application feels coherent and current, works on warehouse tablets, and staff can still find everything where it was. No framework migration was needed.
