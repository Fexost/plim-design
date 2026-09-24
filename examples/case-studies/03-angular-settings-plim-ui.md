# Angular settings page using plim-ui

**Skills:** plim-design, plim-ui, plim-accessibility

## Context

An Angular 21 application already built on plim-ui. Its account settings page has profile, notifications, security, and a "Delete account" action. The user asks to "tidy up the settings page".

## Existing problem

Every settings group is its own `plim-card`, nested inside a page-level card. Each card has a primary "Save" button, so the page shows four primary buttons. "Delete account" is a primary button in the same style as "Save". Notification toggles are custom `div`s with click handlers.

## What the agent notices

- Nested cards claim that each group is an independent entity inside another entity. They're really sections of one page.
- Four primary buttons mean no action reads as primary, and a destructive action looks identical to saving.
- The custom toggles lack keyboard support and a proper role, even though the library provides `input[plimSwitch]` on a native checkbox.
- The page uses plim-ui's defaults consistently otherwise. The system is fine; the composition isn't.

## Relevant Plim principles

Semantic honesty (§8.11), Hierarchy (§8.6), Agency (§8.3) for the destructive action, Improve before replacing (Law 7), Inclusion (§8.10).

## Tension

**Consistency ↔ Context.** "Every section is a card" is consistent, but it misrepresents the structure. Destructive actions should deliberately look different.

## Decision

Keep plim-ui and the page's content. Fix composition, action hierarchy, and semantics.

## Implementation direction

- Remove the outer card. Present sections as headed regions separated by spacing and `plim-separator`, keeping at most one container level where it marks a real unit.
- Decide the save model with the user; it is a product decision. If saving is page-wide, use one `primary` save button. If settings save per section, show a section's save action only when that section has unsaved changes, so at most one or two primary actions are ever visible.
- Move "Delete account" into its own clearly labelled danger section, with a confirmation dialog (`plim-dialog`) that states the consequence and requires deliberate confirmation.
- Replace custom toggles with `input[plimSwitch]` and visible labels.
- Use the `loading` input on the save button (it sets `aria-busy`) and a snackbar for confirmation. Keep error messages next to the relevant field.
- Check both themes and a keyboard walk through the page.

## Expected result

The page reads as one coherent settings document. The save action is obvious, the destructive action is safe and distinct, and toggles work with a keyboard. It still looks like the same product and uses only existing plim-ui pieces.
