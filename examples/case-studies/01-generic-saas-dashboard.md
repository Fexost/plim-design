# Generic SaaS dashboard

**Skills:** plim-review, plim-beautify · **Outcome:** structural intervention

## Context

A project-management SaaS. Team leads open the app several times a day. The user asks: "Improve the dashboard."

The home dashboard was AI-generated for an early prototype: twelve metric cards in a grid, each with a gradient icon tile, a large number, a trend pill, and a shadow, then two charts and a "Recent activity" card. The product's tokens define a colourful brand (a saturated violet and a coral) and a type scale. The gradient tiles, shadows, and card radius are not in the tokens and appear nowhere else in the product.

Users say they "never look at the dashboard"; analytics show most sessions leave it within seconds for the project list.

## What the agent notices

- **Important, accidental.** The attention hierarchy is flat: twelve equally loud numbers, each with a gradient and a coloured pill. Nothing reads first.
- **Important, accidental.** What team leads act on (overdue tasks, blocked items, today's deadlines) is buried in the activity feed. The evidence is behavioural: users bypass the page.
- **Polish, accidental.** Several metrics are redundant ("Tasks", "Total tasks", "Active tasks").
- **Important, accidental; accessibility requirement.** Trend pills show direction by green or red alone. The task doesn't depend on trends, so this isn't Critical, but it fails the use-of-colour requirement and must be fixed rather than offered as optional.
- **None, intentional.** The colourful brand is documented and serves the product. It is not a finding.
- The card treatments are ad-hoc additions, not system conventions, so the card-soup and decoration guidance applies to them.

## Principles and tension

Purpose (§8.1), Hierarchy (§8.6), attention as a resource (§10), Semantic honesty (§8.11), dashboard syndrome (§17).

**Simplicity ↔ Capability:** removing metrics risks hiding something someone uses. **Restraint ↔ Expression:** the brand is colourful, and fixing the hierarchy shouldn't drain it.

## Alternatives considered

- **Restyle the cards** (flatter, softer, new palette). Rejected: it changes the surface and leaves the finding untouched; the page would still not answer "what needs me today?"
- **Delete most metrics.** Rejected: nobody has confirmed which ones are unused.
- **Keep the grid and reorder it by importance.** Viable but weak: twelve containers of equal weight still compete.
- **Lead with what needs action, keep a few metrics.** Chosen.

## Decision

For this dashboard, the problem is information architecture and hierarchy, not styling, and the fix spans the whole page, so the outcome is a structural intervention scoped to this screen. The page's job is "what needs my attention today?"; it leads with that.

## Trade-off accepted

Some metrics move one click away to a reports page. The user confirms which stay. Brand colour appears in fewer places, but more strongly in the places that call for action.

## Implementation direction

- Put a "Needs attention" list first: overdue, blocked, due today, each linking to the item.
- Keep the four or five metrics that inform decisions, in a compact row. The one-off gradient tiles and shadows go, because they aren't part of the product's system and don't distinguish anything.
- Give trends text ("+12% vs last week") alongside colour.
- Use the brand violet and coral confidently on the attention list, its actions, and its urgent states, so the most colourful part of the page is the part that needs action.
- Design the empty state ("Nothing overdue.") and the loading state for the attention list.

## Expected result

The dashboard answers the team lead's first question at a glance. It isn't simply quieter: the attention list is louder than anything on the old page, and the rest steps back. The brand is still recognisable, because its colour now marks what matters.
