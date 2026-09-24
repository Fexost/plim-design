# AI-generated card-heavy interface

**Skills:** plim-review, plim-beautify · **Stress test:** Scenarios A and D · **Outcome:** structural intervention (one page)

## Context

A developer used an AI tool to generate a product detail page for a hardware store. Everything is a rounded card with a shadow: the product image, the title, the price, each specification, the reviews summary, each review, the shipping info, and the "Add to cart" button's container. The user says: "Make it beautiful."

The store has brand guidelines (a practical, trustworthy tradesperson feel, a strong orange, a sturdy sans-serif, real product photography) and a small token set. The generated cards, shadows, and radius come from the AI tool, not from the tokens or guidelines.

## What the agent notices

- The containment is ad-hoc, not a system convention, so the card-soup guidance applies.
- **Important, accidental.** The cards claim that the title, the price, and each specification are independent entities. They are facets of one product.
- **Important, accidental.** Shadows and borders on every block spend attention on edges; the price and "Add to cart" don't stand out. On mobile the page becomes a long stack of similar boxes.
- **Important, identity gap.** The uniform radius and padding make the page look templated. The brand's orange, type, and photography barely register.
- **Unknown.** States for out of stock, low stock, and no reviews aren't designed; the agent can't tell whether they exist.

## Principles and tension

Card soup, decoration inflation, and uniform rounding (§17), Semantic honesty (§8.11), Hierarchy (§8.6), Character (§8.15).

**Restraint ↔ Expression.** Removing containment without adding anything risks a flat, characterless page; the brand needs to come through more, not less.

## Alternatives considered

- **Restyle the cards** (softer shadows, new radius). Rejected: the finding is what the cards claim, not how they look.
- **Remove all containment.** Rejected: reviews are genuinely independent units, and a page of undifferentiated text would lose the brand's sturdiness.
- **Recompose around the purchase decision and let the brand carry the character.** Chosen.

## Decision

For this page, fix composition and hierarchy, keep containment only where it marks a real unit, and move the page's character from generic boxes to the store's own brand.

## Trade-off accepted

The page loses its uniform "designed" texture. Character now depends on photography, type, and colour, which takes more care to get right.

## Implementation direction

- Compose the purchase area as one unit: name, price, availability, quantity, and "Add to cart", with the price and action as the focal point.
- Present specifications as a two-column list or table.
- Keep individual reviews as cards or as a separated list, since they are independent entities.
- For this page, keep a shadow on the sticky mobile "Add to cart" bar, which sits over the content; the other shadows marked nothing.
- Give the brand room: larger product photography, the brand's typeface for the product name, and the orange for the primary action and key moments.
- Design out of stock, low stock, loading reviews, and no reviews yet.

## Expected result

The page reads in the order a shopper thinks, and it looks like this store rather than a generated template. It is more beautiful because it is clearer and more itself.
