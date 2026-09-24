# Tailwind application

**Skills:** plim-design, plim-beautify · **Stress test:** Scenario C · **Outcome:** targeted improvement plus polish

## Context

A React and Tailwind analytics product. The Tailwind theme defines brand colours, a spacing scale, radii, and font families. Over time, components have accumulated arbitrary values (`p-[13px]`, `text-[15px]`, `rounded-[18px]`) and one-off colour shades. The user asks: "Make the UI more consistent and polished."

## What the agent notices

- A system already exists in the Tailwind theme. The inconsistency comes from code bypassing it, not from a missing system.
- **Polish, accidental.** Arbitrary values cluster: most `p-[13px]` and `p-[14px]` instances are attempts at the same relationship. Similar components have visibly different spacing and radii.
- **Polish, accidental.** Three near-identical greys map to two real roles (secondary and tertiary text).
- **Intent unknown.** A few arbitrary values sit around icons and may be deliberate optical adjustments. They are checked before anything changes.
- **Critical, accidental; accessibility requirement.** Custom components have no visible focus style. It's hidden behind a polish request, and it's the most important finding.

## Principles and tension

Improve before replacing (Law 7), Coherence without uniformity (Law 4), Craft (§8.16), Inclusion (§8.10).

**Consistency ↔ Context.** Converging on the theme is the goal, but mechanically flattening every value would erase deliberate exceptions.

## Alternatives considered

- **Adopt a component library or new design system.** Rejected: the existing theme is sound and the user asked for consistency, not replacement.
- **Change theme values to match the one-offs.** Rejected: a theme change restyles every component that uses it (a wide blast radius) to accommodate code that is simply off-scale.
- **Find-and-replace all arbitrary values.** Rejected: it would remove the intentional optical adjustments.

## Decision

For this product, converge usages on the existing theme, add a semantic theme entry only where a real role is missing, and fix focus as a requirement. Existing theme values stay unchanged, which keeps the blast radius to the components that were off-scale.

## Trade-off accepted

A handful of documented exceptions remain. The sweep takes longer than a mechanical replace.

## Implementation direction

- Inventory arbitrary values and group them by intended relationship. Map each group to the nearest theme value; keep and document an exception where the difference is intentional.
- Add a semantic theme entry for the missing text role, then use it everywhere the three greys appeared.
- Define shared hover and focus treatments from the theme's colours, apply them to all interactive components, and verify focus contrast.
- Leave components that already follow the theme alone.

## Expected result

The product looks the same at a glance and more precise on inspection. Future work stays consistent because values come from the theme again. Keyboard users can see where they are.
