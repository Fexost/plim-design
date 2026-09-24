# Tailwind application

**Skills:** plim-design, plim-beautify · **Stress test:** Scenario C

## Context

A React and Tailwind analytics product. The Tailwind theme defines brand colours, a spacing scale, and font families. Over time, components have accumulated arbitrary values (`p-[13px]`, `text-[15px]`, `rounded-[18px]`) and many one-off colour shades. The user asks: "Make the UI more consistent and polished."

## Existing problem

Similar components have visibly different spacing and radii. Three near-identical greys are used for secondary text. Hover and focus styles vary per component; some have none.

## What the agent notices

- A system already exists in the Tailwind theme. The inconsistency comes from code bypassing it, not from a missing system.
- Arbitrary values cluster: most `p-[13px]` and `p-[14px]` instances are attempts at the same relationship.
- The three greys map to two real roles (secondary and tertiary text).
- Focus styles are missing on custom components, a Critical finding hidden behind a polish request.

## Relevant Plim principles

Improve before replacing (Law 7), Coherence without uniformity (Law 4), Craft (§8.16), Inclusion (§8.10).

## Tension

**Consistency ↔ Context.** Some arbitrary values may be deliberate, for example an optical adjustment around an icon. Don't flatten everything mechanically.

## Decision

Converge on the existing Tailwind theme. Don't introduce a new design system, component library, or visual style.

## Implementation direction

- Inventory arbitrary values and group them by intended relationship. Map each group to the nearest theme value; keep a documented exception only where the difference is intentional.
- Where the theme genuinely lacks a role (a secondary-text colour), add a semantic theme entry rather than another raw shade, then use it everywhere.
- Define shared hover and focus treatments using the theme's colours and apply them to all interactive components; verify focus contrast.
- Leave components that already follow the theme alone.

## Expected result

The product looks the same at a glance but calmer and more precise on inspection. Future work stays consistent because values come from the theme again. Keyboard users can finally see where they are.
