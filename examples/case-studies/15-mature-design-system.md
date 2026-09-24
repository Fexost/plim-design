# Mature design system

**Skills:** plim-review, plim-design · **Outcome:** targeted improvement

## Context

A logistics company's field app for delivery drivers, on Android and the web, built on Material 3. The company runs a documented extension of it: a design-system site, a token set with custom brand colour roles, and component usage rules. Several teams build on it. The user asks for a design review of the jobs and delivery screens.

At a glance, the app resembles several patterns that Plim's anti-pattern guidance lists as risks: fully rounded buttons everywhere, elevated cards for every job, tonal surfaces, a floating action button, and chips.

## What the agent notices

These are system conventions, not ad-hoc additions. They are documented, tokenised, and applied consistently, and several are platform conventions drivers already know. The review judges whether they are used as the system intends.

- **None, intentional.** Pill-shaped buttons, tonal surfaces, and elevated job cards. Jobs are independent entities that drivers open, reorder, and complete, so the cards mark real units.
- **Important, accidental.** The jobs screen has two floating action buttons. The system treats the FAB as the screen's single most important action; with two, neither reads that way.
- **Important, accidental.** "Complete delivery" is a filter chip. In this system, chips signal filtering or selection, not a committing action, so the visual claim is wrong. The system's filled button exists for this.
- **Important, accidental; requirement.** A custom brand tertiary colour role fails text contrast on its own container colour in the dark theme.
- **Polish, accidental.** One screen hard-codes a shadow instead of the elevation token, so it doesn't adapt between themes.
- **Polish, accidental.** On the settings screen, a card wraps a single text field; elsewhere, the system's cards group content about one subject.

## Principles and tension

Existing design systems (§14), Improve before replacing (Law 7), Semantic honesty (§8.11), Familiarity (§8.4), Coherence (§8.5).

**Familiarity ↔ Identity.** The system's conventions are familiar to drivers and consistent across teams. That is worth more here than any stylistic alternative.

## Alternatives considered

- **Flatten the look** (square corners, no elevation, fewer cards) because it resembles card soup and pill overuse. Rejected: resemblance isn't a finding. It would break consistency with the platform, the system's documentation, and every other team's screens.
- **Raise the conventions with the system team.** Not needed. None of them harms this product. If one did, it would be a system-level question for the system's owners, not a local override.
- **Fix the misuses within the system's vocabulary.** Chosen.

## Decision

For this app, the design system stays as it is. The findings are about incorrect use of it on these screens, plus one contrast failure in a custom colour role. The contrast fix is reported to the system team, because the role is shared.

## Trade-off accepted

None of substance. The agent accepts a look it might not have chosen for a new product, because this product's vocabulary is already chosen and working.

## Implementation direction

- Keep one FAB on the jobs screen, for the primary action; move the other action into the top app bar or a menu, following the system's rules.
- Replace the "Complete delivery" chip with the system's filled button.
- Propose a corrected tonal pairing for the tertiary role to the system team, since every team uses it.
- Replace the hard-coded shadow with the elevation token.
- Present the settings field inside its section without its own card.

## Expected result

The screens look exactly like the rest of the company's apps, because they use the same system, now correctly. The actions say what they do, and the contrast fix improves every team's screens.
