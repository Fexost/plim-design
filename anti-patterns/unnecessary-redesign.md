# Unnecessary redesign

Supporting material for [`philosophy.md`](../philosophy/philosophy.md) Law 7 (Improve before replacing), §17 (Unnecessary Redesign), and §18 (Distinguish change from improvement). It adds depth, not rules.

**Core question (§17):** what meaningful improvement justifies this change?

## Recognising it

- A working component, pattern, layout, or design system replaced with a different one.
- Proposed changes justified by "cleaner", "more modern", or "better practice" without a named problem.
- A restyle that touches every screen in response to a request about one issue.
- Migration to a new framework or component library suggested as the fix for a visual complaint.
- Large diffs where the before and after are equally functional.

## Why it happens

Visible change looks like progress and effort. An agent's own defaults feel like improvements because they are familiar to it. Redesign is also easier than understanding why an existing system is the way it is.

## Why it matters

- **Familiarity.** Existing users lose learned patterns and efficiency (§8.4).
- **Preserved knowledge.** Existing systems encode decisions about accessibility, edge cases, brand, and constraints (§14) that a replacement may silently drop.
- **Risk and reviewability.** Large changes are harder to review and reverse (§18, Preserve human control).
- **Identity.** Replacing the product's visual language with the agent's defaults erases character (§15).

## When it is not a problem

Replacement is justified when you can name what the existing piece prevents: a task people cannot complete, a state it cannot express, an accessibility need it cannot meet, or an incoherence extension cannot fix. A user's explicit decision to redesign is also legitimate; the reasoning then shifts to doing it well.

## Diagnosing

- What specific problem does the current design cause, and for whom?
- Could extending or adjusting the existing system solve it?
- What would be lost: learned behaviour, accessibility, edge-case handling, brand?
- Is the proposed alternative better, or only different (§18)?

## Repair

1. Name the problem and its consequence before proposing anything.
2. Try the smallest intervention that addresses it, within the existing system.
3. If replacement is still justified, make it incremental, reviewable, and reversible, and state what is preserved.
4. Consider that the right outcome may be no change.

## Overcorrection

Refusing all change preserves real problems. Improve before replacing does not mean never replacing; it means replacement must be earned.

## See also

[Legacy Bootstrap interface](../examples/case-studies/07-legacy-bootstrap.md), [Polish only](../examples/case-studies/12-little-or-no-change.md)
