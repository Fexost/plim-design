# Angular settings page using plim-ui

**Skills:** plim-design, plim-ui, plim-accessibility · **Outcome:** targeted improvement

## Context

An Angular 21 application already built on plim-ui. Its account settings page has profile, notifications, security, and a "Delete account" action. The user asks to "tidy up the settings page".

## What the agent notices

- **Important, accidental.** Every settings group is its own `plim-card`, nested inside a page-level card. The library's card is for independent units; these are sections of one page. The finding is the misuse of a system component, not the existence of cards.
- **Important, accidental.** Each card has a primary "Save" button, so four primary actions compete and none reads as primary.
- **Critical, accidental.** "Delete account" has the same primary style as "Save" and runs without confirmation, so a mis-click can destroy an account.
- **Critical, accidental; accessibility requirement.** Notification toggles are custom `div`s with click handlers: no keyboard operation and no role. The library provides `input[plimSwitch]` on a native checkbox.
- **None, intentional.** The rest of the page uses plim-ui consistently. The system is fine; the composition isn't.

## Principles and tension

Semantic honesty (§8.11), Hierarchy (§8.6), Agency (§8.3), Improve before replacing (Law 7), Inclusion (§8.10).

**Consistency ↔ Context.** "Every section is a card" is consistent, but it misstates the structure. On this page, deleting the account has a different consequence from saving, so it needs a different treatment.

## Alternatives considered

- **Un-nest the cards but keep one per section.** Viable. It's the right answer if each section saves independently; see the save model below.
- **Move sections into tabs.** Rejected: it changes navigation, which nobody asked for, and hides settings people scan for.
- **Restyle the cards.** Rejected: the problem is what the cards claim, not how they look.

## Decision

For this page, keep plim-ui and the content. Fix composition, action hierarchy, the destructive action, and the toggles' semantics.

## Trade-off accepted

The page loses its boxed look. The save model is a product decision, so the agent asks rather than chooses.

## Implementation direction

- Remove the outer card. Present sections as headed regions separated by spacing and `plim-separator`, or keep one card per section if sections save independently.
- Ask the user about the save model. If saving is page-wide, use one `primary` save button. If settings save per section, show a section's save action only when that section has unsaved changes.
- Move "Delete account" into its own clearly labelled section, with a confirmation dialog (`plim-dialog`) that states the consequence and requires deliberate confirmation.
- Replace custom toggles with `input[plimSwitch]` and visible labels.
- Use the button's `loading` input and a snackbar for confirmation; keep error messages next to their fields.
- Check both themes and a keyboard walk through the page.

## Expected result

The page reads as one coherent settings document. The save action is obvious, deleting is safe and distinct, and toggles work with a keyboard. It still looks like the same product and uses only existing plim-ui pieces.
