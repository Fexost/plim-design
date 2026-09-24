# Card soup

Supporting material for [`philosophy.md`](../philosophy/philosophy.md) §17 (Card Soup) and §8.11 (Semantic honesty). It adds depth, not rules.

**Core question (§17):** are these actually independent surfaces?

## Recognising it

- Most content sits in bordered or shadowed boxes with the same radius and padding.
- Cards nested in cards; a page-level card containing section cards containing item cards.
- Single values (a title, a price, one setting) get their own card.
- On narrow screens the page becomes a long stack of similar boxes.

## Why it happens

A card is the easiest way to make a block look finished. It gives padding, separation, and a sense of polish without deciding how the content relates. Component libraries and AI tools make it the default container.

## Why it matters

- **Semantic honesty.** A card claims its content is an independent entity. When it isn't, people build a wrong model of the structure.
- **Attention.** Every card edge and shadow spends attention (§10). Many cards make the edges louder than the content.
- **Hierarchy.** When everything is a card, the one card that matters can't stand out.
- **Density.** Card padding and gaps consume space that dense, expert interfaces need (§8.12).

## When it is not a problem

Cards suit collections of genuinely independent, comparable entities that may be acted on individually: products in a catalogue, projects, people, reviews, media items. They also suit a single self-contained unit that must stand apart from its surroundings.

## Diagnosing

- Could this card be moved, removed, or acted on independently of its neighbours?
- Would the user describe it as "a thing" or as "part of the page"?
- Does removing the container lose any information, or only decoration?
- Is nesting expressing real hierarchy, or accumulating wrappers?

## Repair

1. Remove containers that don't mark a real unit; group with proximity, alignment, and headings.
2. Replace card borders between sections with spacing or a single divider.
3. Flatten nesting to at most one container level where it marks a unit.
4. Keep cards for true collections, and consider a list or table if items need comparison.

## Overcorrection

Removing all containment can leave content floating with ambiguous grouping. Grouping must still be clear; it just shouldn't depend on boxes.

## See also

[AI-generated card-heavy interface](../examples/case-studies/11-ai-generated-card-interface.md), [Angular settings page using plim-ui](../examples/case-studies/03-angular-settings-plim-ui.md), [visual-noise.md](visual-noise.md)
