# Excessive decoration

Supporting material for [`philosophy.md`](../philosophy/philosophy.md) §17 (Decoration Inflation), Law 2 (Meaning before decoration), and §8.14 (Continuity). It adds depth, not rules.

**Core question (§17):** what meaning does each treatment communicate?

Covers shadows, glassmorphism, background blobs and shapes, decorative icons, and motion that doesn't explain change.

## Recognising it

- Shadows on most surfaces, without a rule for what a shadow means in this product.
- Translucent, blurred panels over busy or variable backgrounds.
- Blobs, orbs, and abstract shapes behind content.
- An icon beside every heading, label, and list item.
- Floating, pulsing, or parallax effects; hover animations on non-interactive elements; long entrance animations.

## Why it happens

Each treatment makes a single element look richer in isolation. Added together, they become the fastest route to "looks designed" without deciding what anything means. Motion in particular impresses in demos.

## Why it matters

- **Meaning.** Treatments without meaning dilute those that carry it (Law 2, §11): if everything has a shadow, elevation can't signal a dialog.
- **Legibility.** Glass and background shapes reduce text contrast, often variably, which is an inclusion problem (§8.10).
- **Attention.** Motion is the strongest attention signal; decorative motion pulls attention from the task and can cause vestibular discomfort.
- **Performance and robustness.** Blur and animation cost more on low-end devices.

## When it is not a problem

- Shadows that follow the product's elevation language: things that sit above the page (menus, dialogs, popovers, sticky or dragged items), or whatever else the system defines elevation to mean, such as tactility or importance.
- Translucency where seeing what's behind matters, with contrast verified.
- Illustration and imagery that express brand character (§8.15) or explain something.
- Icons that aid recognition and scanning, such as in navigation or toolbars.
- Motion that explains what changed, where something came from or went, or what needs attention (§8.14).
- Expressive brands where decoration is part of the identity, provided it doesn't compete with tasks.

## Diagnosing

For each treatment: what distinction or meaning does it communicate (§11)? If removed, what would the user lose? Does it still read, and still move acceptably, with reduced motion, low contrast settings, and a slow device?

## Repair

1. State what elevation means in this product (layering, separation, importance, tactility) and apply it by that meaning. Where the system has an elevation scale, use it; where it has none, define only the levels the product actually needs.
2. Keep translucency where seeing what's behind matters, with contrast verified on the worst background; otherwise consider tinted or opaque surfaces.
3. Keep background shapes that belong to the brand's visual language; replace arbitrary ones with brand imagery that has a role, a colour field, or nothing.
4. Keep icons where they aid recognition or carry the product's illustrative voice; let text stand alone where the label is clear.
5. Keep motion that explains change or carries the product's character at meaningful moments; question motion that does neither. Honour reduced motion, and give continuous motion a way to pause (a requirement for motion longer than five seconds).

## Overcorrection

Removing all depth and motion can make layers and state changes harder to follow. Keep the treatments that explain structure and change.

## See also

[Beautiful but inaccessible interface](../examples/case-studies/08-beautiful-but-inaccessible.md), [Highly branded application](../examples/case-studies/05-highly-branded-application.md)
