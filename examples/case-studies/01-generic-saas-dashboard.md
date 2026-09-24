# Generic SaaS dashboard

**Skills:** plim-review, plim-beautify · **Stress test:** Scenario A

## Context

A project-management SaaS. The home dashboard was AI-generated: twelve metric cards in a grid, each with a gradient icon tile, a large number, a trend pill, and a shadow. Below are two charts and a "Recent activity" card. Users are team leads who open the app several times a day.

## Existing problem

Users say they "never look at the dashboard" and go straight to their project list.

## What the agent notices

- The attention hierarchy is flat: twelve equally loud numbers, each with a gradient and a coloured pill. Nothing reads first.
- Several metrics are redundant ("Tasks", "Total tasks", "Active tasks") and have no obvious action attached.
- The things team leads actually act on (overdue tasks, blocked items, today's deadlines) are buried in the activity feed.
- Every card has the same radius, shadow, and padding, so the one card that matters looks like the eleven that don't.
- Trend pills are green or red with no text alternative.

## Relevant Plim principles

Purpose (§8.1), Hierarchy (§8.6), attention as a resource (§10), Semantic honesty (§8.11), dashboard syndrome and card soup (§17).

## Tension

**Simplicity ↔ Capability.** Removing metrics risks hiding information someone uses. **Restraint ↔ Expression.** The product has a colourful brand that shouldn't be flattened into grey.

## Decision

Treat this as an information architecture and hierarchy problem, not a styling one. The screen's job is "what needs my attention today?" Lead with that, demote the vanity metrics, and keep the brand colour for things that need action.

## Implementation direction

- Replace the metric grid's lead position with a "Needs attention" list: overdue, blocked, due today, each linking to the item.
- Keep four or five metrics that inform decisions, in a compact row without individual cards, gradients, or shadows. Move the rest to a reports page rather than deleting them, and ask the user to confirm which ones matter.
- Trend indicators get text ("+12% vs last week") alongside colour.
- Use the brand accent for the attention list's actions and the primary state, not for every icon tile.
- Design the empty state ("Nothing overdue. Good work.") and the loading state for the attention list.

## Expected result

The dashboard answers the team lead's first question at a glance. It is quieter overall, yet the important items are more visible than before. The brand is still recognisable because its colour now marks meaning rather than filling every surface.
