# Generic UI

Supporting material for [`philosophy.md`](../philosophy/philosophy.md) §16 and §17. It adds depth, not rules.

**Core question:** does this interface feel like this product, or like a template?

Generic UI is less a single pattern than the family resemblance produced by a few reasoning shortcuts. The other files in this directory describe specific symptoms; this one describes the causes.

## Recognising it

- The screen could belong to almost any product in the category if the logo were swapped.
- A familiar kit: gradient hero, metric cards, rounded containers, pill badges, an accent colour on everything, oversized headings.
- Every page, whatever its task, has the same composition.
- The design looks finished in a static frame but has thin loading, empty, and error states.

## Why it happens

- **Signal substitution.** Visual signals associated with polished products (cards, shadows, gradients, big numbers) are applied in place of decisions about this product. They look like quality without being the result of it.
- **Trend substitution** (§17). "Modern" stands in for reasoning. The question "what problem does this solve?" is never asked.
- **Screenshot optimisation** (§17). Work is judged by a single static frame with ideal data, so states, edges, and real use go undesigned.
- **Dashboard syndrome** (§17). Every page becomes metrics and charts, because that composition reads as "product" regardless of the user's task.
- **Aesthetic presets.** Words like "premium", "modern", or "minimal" are treated as visual styles rather than outcomes. A common result is replacing useful density with empty space, or adding luxury styling without improving hierarchy.

AI tools are especially prone to these because they average over many interfaces and converge on the most common visual answer (§17).

## Why it matters

- Identity is lost (§15, §8.15): the product stops communicating its own character.
- Hierarchy suffers because the template's emphasis doesn't match this product's priorities (§8.6).
- Real use suffers because only the ideal state was designed (Law 6).

## When it is not a problem

Convention is not genericness. Familiar patterns for forms, navigation, tables, and dialogs reduce effort (§8.4), and many tools rightly look quiet and conventional. The failure is not "looking familiar"; it is decisions that weren't made for this product.

## Diagnosing

- What is this screen's primary task, and does the composition start from it?
- Which visual treatments would you keep if you had to justify each one (§11)?
- Where is this product's identity expressed: typography, colour, language, imagery, density, interaction?
- What does the screen look like empty, loading, failed, with long content, at a narrow width?
- If "premium" or "modern" was the request, what outcome was actually wanted?

## Repair

1. Restate the task and priority; rebuild the attention hierarchy around it.
2. Remove treatments that communicate nothing (see the specific files).
3. Let identity come from the product's own brand and content, not from added effects.
4. Design the states and edges that the template skipped.

## Overcorrection

Stripping everything back to grey and whitespace is also generic. The aim is intentional character, not the absence of character.

## See also

[AI-generated card-heavy interface](../examples/case-studies/11-ai-generated-card-interface.md), [Generic SaaS dashboard](../examples/case-studies/01-generic-saas-dashboard.md), ["Make this modern"](../examples/case-studies/10-make-it-modern.md)
