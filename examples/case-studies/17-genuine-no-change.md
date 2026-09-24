# Genuine no change

**Skills:** plim-review, plim-design · **Outcome:** no change

## Context

A hospital's ward app has a medication administration screen. Nurses use it at the bedside to record doses, on wall-mounted and handheld devices, often gloved and often interrupted. While on another task, the IT project manager asks: "That screen looks old. Can you give it a refresh while you're in there?"

The request is optional ("while you're in there"), so the direction is the agent's to recommend.

## What the agent notices

- **Purpose and hierarchy.** The patient identity band reads first, then due medications with time, dose, and route, then the record action. That order matches the task and the hospital's safety checks.
- **Evidence the design works.** The screen was redesigned two years ago with nurses and usability-tested. Medication-error reporting since then shows no incidents attributed to the interface.
- **System.** It follows the hospital's clinical design system, and nurses move between several ward apps that share the same patterns.
- **Accessibility.** Requirements are met: contrast in day and night modes, keyboard and scanner operation, and large targets that work with gloves.
- **States.** Overdue, held, refused, partial dose, and an offline queue with clear sync status are all designed.
- **Findings.** No Critical, Important, or Polish findings. The agent checked for rough edges against the system and for craft defects, and found none worth a change.
- **Preferences, set aside.** The typeface looks dated to the agent (it is the clinical system's typeface), and the grey header is plain (a system convention).
- **Cost of change.** In a safety-critical, interrupted task, visual change risks slips from altered habits. Changes to this screen also need clinical safety sign-off, and a local refresh would break consistency with the other ward apps.

## Principles and tension

Doing nothing is valid (§18), Improve before replacing (Law 7), Familiarity (§8.4), Respect the person (Law 5), Distinguish change from improvement (§18).

## Alternatives considered

- **A light refresh** (typeface, colours, spacing). Rejected: it would have a real cost (risk, retraining, sign-off, inconsistency) and no evidenced improvement.
- **Polish something, to show effort.** Rejected: there was nothing that met the Polish standard, and inventing findings would be its own failure.
- **No change.** Chosen.

## Decision

For this screen, recommend no change, and explain why in terms of evidence and cost, not only "it's already good".

The recommendation is not a veto. If the project manager, with this information, still decides the screen should change, the right route is through the clinical design system team, so every ward app changes together and goes through safety sign-off.

## Trade-off accepted

The screen keeps a look some people find dated. That appearance has no measured cost; changing it would have several.

## What would change the answer

- Incident or observation data pointing at the interface.
- New devices or a new clinical workflow.
- An update to the clinical design system, applied to all ward apps together.
- A new accessibility or regulatory requirement.

## Report

- **Outcome:** no change.
- **Strengths to preserve:** hierarchy aligned with safety checks, complete states, glove-friendly targets, consistency across ward apps.
- **Preferences set aside:** typeface and header plainness.
- **Critical findings:** none.
- **Revisit when:** any of the conditions above occur.

## Expected result

A safe screen stays safe. The project manager gets a reasoned recommendation they can act on, not a visual change nobody needed.
