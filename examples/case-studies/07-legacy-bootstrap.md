# Legacy Bootstrap interface

**Skills:** plim-review, plim-beautify · **Stress test:** Scenario C

## Context

An internal logistics admin built on Bootstrap years ago, customised through Sass variables. It has hundreds of screens maintained by a small team. The user asks: "It looks dated. Can you modernise it?"

## Existing problem

It uses Bootstrap's defaults heavily, with some inconsistent overrides. Pages mix `.card`, `.panel`-style wrappers, and bare tables. Forms have labels in inconsistent positions. Alerts appear for trivial messages. It works, and staff know it well.

## What the agent notices

- "Dated" needs interpreting. Likely meanings here: inconsistent visual language, noisy alerts, and poor behaviour on the tablets used in warehouses. Not "needs a new framework".
- A rewrite would be enormous, risky, and would break staff familiarity for little task benefit.
- Bootstrap's Sass variables and utilities are a real system. Most inconsistency comes from local overrides fighting it.
- Tablets in the warehouse are an actual context the current layout handles poorly.

## Relevant Plim principles

Improve before replacing (Law 7), Modern as appropriate response rather than trend (§21), Familiarity (§8.4), Adaptability (§8.9), Human judgment remains central (Law 8).

## Tension

**Innovation ↔ Familiarity.** Staff efficiency depends on familiarity; the user wants the product to feel current.

## Decision

Modernise through the existing Bootstrap theme, incrementally, targeting the problems that affect work. Ask the user to confirm the interpretation of "modern" and whether tablets are a priority before larger changes.

## Implementation direction

- Adjust the Sass theme (typography scale, neutral palette, border and radius values) so the whole application refreshes coherently from one place.
- Remove local overrides that fight the theme, starting with the most-used screens.
- Standardise form label placement and validation messaging.
- Reserve alerts for things that need attention; use inline confirmation or toasts for routine success.
- Improve tablet layouts on the warehouse screens: larger targets and tables that prioritise the columns used on the floor.
- Ship in stages that can be reviewed and reverted.

## Expected result

The application feels coherent and current, works on warehouse tablets, and staff can still find everything where it was. No framework migration was needed.
