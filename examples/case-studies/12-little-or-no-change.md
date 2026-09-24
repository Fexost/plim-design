# Polish only: a plain tool that works

**Skills:** plim-review · **Outcome:** polish only

## Context

A command-line-style developer tool with a web dashboard: monospaced type, a near-monochrome palette, dense lists, no illustrations, keyboard shortcuts for everything. The user asks: "Can you make this more beautiful? It feels a bit plain." The product has no brand guidelines calling for more expression, and its users are developers who praise its speed.

For a case where the right answer is no change at all, see [case 17](17-genuine-no-change.md).

## What the agent notices

- The attention hierarchy matches the task: current build status reads first, then recent runs, then configuration.
- **None, intentional.** The minimalism is deliberate and its purpose is served: the audience values speed, density, and keyboard control, and uses the tool heavily.
- States are thorough (running, queued, failed with logs, cancelled, empty projects), and accessibility requirements are met (visible focus, real headings, text status labels, readable contrast).
- **Under-expression check.** "Plain" could signal an identity gap. Here there is no evidence of one: no brand direction calls for more, and users don't describe the tool as generic. The discomfort is the user's taste, so it's a preference, but the user is entitled to choose more character.
- **Polish, accidental.** Spacing between list groups departs from the tool's own scale.
- **Polish, accidental.** Hover is barely distinguishable from selected, an objective state defect.

## Principles and tension

Doing nothing is valid (§18), Restraint (§8.7), Minimalism is neither good nor bad (§21), Identity without imposition (§15).

**Restraint ↔ Expression.** The user wants more character; the product's current character is its restraint.

## Alternatives considered

- **Add decoration** (gradients, cards, illustrations, larger type, animation). Rejected for this tool: each would spend attention without communicating anything, and would slow expert use.
- **No change at all.** Rejected: there are two genuine rough edges against the tool's own system.
- **Polish the two findings, and offer character as the user's choice.** Chosen.

## Decision

For this tool, fix the two polish findings and recommend no further visual change, explaining why. If the user wants more character, offer options that fit the identity: refined monospaced typography, or one considered accent for status. The user decides; if they choose one, the agent implements it well.

## Trade-off accepted

The user doesn't get the visible transformation they may have expected. They get a clear explanation and a choice instead of an unrequested restyle.

## Implementation direction

- Normalise spacing between list groups using the existing scale.
- Make hover and selected states clearly distinct without adding colour noise.
- Report the review: what works and must be preserved, the two fixes, and why no further change is recommended.

## Expected result

The tool stays fast, dense, and recognisably itself, with two rough edges removed. The decision about character stays with the user.
