# Explicit redesign request

**Skills:** plim-design, plim-review, plim-accessibility · **Outcome:** redesign (human-directed)

## Context

A scheduling product for clinics. Receptionists use it all day to manage appointments, mostly by keyboard. It has about 140 screens and a shared component library, which also powers a patient booking widget embedded on clinics' own websites. It meets WCAG 2.2 AA, including a keyboard-driven calendar.

The head of product writes: "We're repositioning upmarket and rebranding next quarter. I want a full redesign of the web app: new navigation, new layout, new visual language. Not a refresh."

## What the agent notices

- An audit finds a usable product with a few Important findings and no Critical ones. Left to itself, the agent would recommend targeted improvements; it would not have initiated a redesign. Compare [case 07](07-legacy-bootstrap.md), where "modernise" was an adjective and the agent kept the existing system.
- Here, a human has explicitly decided. The repositioning and rebrand are the justification. Law 7 governs what the agent initiates, not this decision.
- The agent raises its concerns once, specifically:
  - **Blast radius.** The shared component library also drives the patient booking widget. Is the widget in scope, and on what timeline?
  - **Familiarity.** Receptionists will need to relearn navigation. The agent recommends an opt-in preview period, keeping existing keyboard shortcuts, and keeping domain terminology unless the rebrand changes it.
  - **Accessibility (requirement).** The new design must keep the product's current conformance, including full keyboard operation of the calendar. This constrains how the new calendar is built, not how it looks.
  - **Technical constraint.** The calendar is custom and costly to rebuild; the schedule should account for it.
  - **Sequencing.** A staged rollout by area or a single launch? That's the head of product's call.

## Principles and tension

Human judgment (Law 8), Coherence (§8.5), Familiarity (§8.4), Inclusion (§8.10), Design for reality (Law 6).

**Innovation ↔ Familiarity.** The human chose innovation. The agent's contribution is carrying forward what users depend on, as recommendations, and making the new system coherent.

## Alternatives considered

- **A theme refresh presented as a redesign.** This is the agent's preference. It says so once, and doesn't pursue it. Delivering it anyway would silently substitute the agent's judgment for the human's.
- **Redesign screen by screen without a new system.** Rejected: 140 screens would drift apart.
- **System-first redesign:** new foundations and components from the new brand, then navigation and layouts, then screens. Chosen, sequenced as the head of product decides.

## Decision

Redesign in full, as directed. The head of product decides the widget scope and the rollout sequencing.

## Trade-off accepted

The redesign costs more time and more retraining than a refresh would. The head of product accepted that knowingly.

## Implementation direction

- Define the new foundations (type, colour roles, spacing, shape, elevation, motion) from the new brand, and rebuild the shared components on them, with all states and keyboard behaviour.
- Design new navigation and layouts for the core receptionist tasks first: day view, booking, rescheduling, check-in.
- Carry forward what the audit found users depend on, presented as recommendations: keyboard shortcuts, calendar density, domain terms.
- Verify every rebuilt component and flow against the current conformance level before it replaces the old one.
- Document the new system so other teams, and the widget if in scope, can adopt it.

## Expected result

A genuinely new product that fits the upmarket brand, built on a coherent new system. It is at least as accessible as before, and receptionists keep the shortcuts and density they rely on. The agent carried out the decision it was given, not a smaller one it preferred.
