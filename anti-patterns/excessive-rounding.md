# Excessive rounding

Supporting material for [`philosophy.md`](../philosophy/philosophy.md) §17 (Uniform Rounding) and §8.5 (Coherence). It adds depth, not rules.

**Core question (§17):** which things should actually belong to the same shape language?

## Recognising it

- One large radius applied to everything: containers, buttons, inputs, images, tags.
- Pill shapes on buttons, inputs, badges, tabs, and filters alike.
- Radii that don't nest: an inner element with the same radius as its container, producing uneven corners.

## Why it happens

Rounded shapes read as friendly and contemporary, and a single radius value is the simplest system. Many generated interfaces apply the largest radius in the scale by default.

## Why it matters

- **Shape stops carrying meaning.** When actions, inputs, and labels share a shape, people lose a cue for telling them apart (§8.11).
- **Identity.** Uniform rounding is a strong part of the generic AI look (§17); it pulls products toward the same appearance.
- **Craft.** Non-nesting radii and pills on dense controls look soft and imprecise.

## When it is not a problem

- A brand whose character is deliberately soft or playful, applied as a considered shape language (§8.15).
- Pills for a specific role, such as filter chips or tags, where the shape distinguishes that role.
- Circular shapes for avatars and icon buttons where the circle has meaning.

## Diagnosing

- Which element types exist on this screen, and which should share a shape?
- Does shape help tell actions, inputs, and labels apart?
- Does the radius scale with element size and nest correctly?
- Is the shape language part of the brand, or a default?

## Repair

1. Define shape roles (containers, controls, tags, media) using the existing system's radius scale.
2. Reserve pill shapes for one role, if the system uses them at all.
3. Make inner radii smaller than outer radii where elements nest.

## Overcorrection

Making everything square is just another uniform treatment. The goal is shape with meaning, not a different default.

## See also

[AI-generated card-heavy interface](../examples/case-studies/11-ai-generated-card-interface.md), [inconsistent-patterns.md](inconsistent-patterns.md)
