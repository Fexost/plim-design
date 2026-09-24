# AI-generated card-heavy interface

**Skills:** plim-review, plim-beautify · **Stress test:** Scenarios A and D

## Context

A developer used an AI tool to generate a product detail page for a hardware store. Everything is a rounded card with a shadow: the product image, the title, the price, each specification, the reviews summary, each review, the shipping info, and the "Add to cart" button's container. The user says: "Make it beautiful."

## Existing problem

The page feels busy and generic. On mobile it becomes a long stack of similar boxes. The price and "Add to cart" don't stand out.

## What the agent notices

- Cards are asserting that the title, the price, and each specification are independent entities. They aren't; they're facets of one product.
- Shadows and borders on every block spend the attention budget on edges. The eye has no focal point.
- Uniform radius and padding everywhere make the page look templated rather than like this store.
- The real product-page hierarchy (image, name, price, availability, add to cart, then details) is lost.

## Relevant Plim principles

Card soup, decoration inflation, and uniform rounding (§17), Semantic honesty (§8.11), Hierarchy (§8.6), Beauty as an outcome (§3).

## Tension

**Restraint ↔ Expression.** Stripping every card risks a flat, characterless page. The store's brand (a practical, trustworthy tradesperson feel) should come through.

## Decision

Diagnose first: this is a composition and hierarchy problem. Remove containment that doesn't mark real units; don't restyle the cards.

## Implementation direction

- Compose the purchase area as one unit: name, price, availability, quantity, and "Add to cart" grouped by proximity, with the price and action as the focal point.
- Present specifications as a simple two-column list or table, not cards.
- Keep cards, if anywhere, for individual reviews, which genuinely are independent entities; or use a list with separators.
- Use elevation only for things above the page (the sticky mobile "Add to cart" bar, menus).
- Express the brand through typography, the accent used for the primary action, and product photography, not through boxes.
- Design states: out of stock, low stock, loading reviews, no reviews yet.

## Expected result

The page reads in the order a shopper thinks. It looks designed for this store rather than generated. It is more beautiful because it is clearer, not because it is decorated.
