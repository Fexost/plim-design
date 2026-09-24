# Inconsistent patterns

Supporting material for [`philosophy.md`](../philosophy/philosophy.md) Law 4 (Coherence without uniformity), §8.5 (Coherence), and §8.8 (Rhythm). It adds depth, not rules.

**Core question (Law 4):** do similar things feel related, and are different things distinguishable?

Covers two opposite failures: inconsistency, where similar things are treated differently, and uniformity, where different things are treated the same.

## Recognising it

**Inconsistency:**

- Arbitrary values that bypass the system's scales (one-off spacing, font sizes, radii, colour shades).
- Spacing between equivalent groups that varies from place to place.
- The same action styled or placed differently on different screens.
- Several components doing the same job (three modal implementations, two date pickers).
- Validation, feedback, or confirmation behaving differently across flows.

**Uniformity:**

- Different kinds of content forced into the same component or container.
- Destructive, primary, and secondary actions styled alike.
- One density applied to every screen regardless of task.

## Why it happens

Inconsistency accumulates when work is local: each screen or component is solved alone, often under time pressure, and values drift. Uniformity happens when "consistency" is pursued as identical treatment instead of consistent meaning.

## Why it matters

- **Predictability.** People learn patterns; inconsistency makes them relearn and doubt (§8.4).
- **Rhythm.** Arbitrary spacing makes grouping ambiguous and the interface feel disorganised (§8.8).
- **Meaning.** Uniformity erases distinctions people need (§8.11).
- **Maintenance.** Divergent components multiply bugs and accessibility gaps.

## When it is not a problem

- Deliberate differences with a reason: a destructive action that looks different, a denser view for an expert task, an optical adjustment around an icon.
- Contextual adaptation (§9, Consistency ↔ Context): relationships stay stable while values adapt.

## Diagnosing

- Is this difference deliberate, and can someone state the reason?
- Do these arbitrary values cluster around a relationship the system already expresses?
- Are these two components doing the same job?
- Would making these identical hide a meaningful difference?

## Repair

1. Map arbitrary values to the nearest system value; keep documented exceptions only where intentional.
2. Add a token for a missing relationship instead of repeating raw values.
3. Converge duplicate components on the one that best serves all uses, preserving accessibility behaviour.
4. Where things differ in meaning, make the difference deliberate and visible.

## Overcorrection

Mechanically forcing every value and component to be identical is uniformity. Consistency lives in relationships and principles, not identical values (Law 4).

## See also

[Tailwind application](../examples/case-studies/04-tailwind-application.md), [Legacy Bootstrap interface](../examples/case-studies/07-legacy-bootstrap.md)
