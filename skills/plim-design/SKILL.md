---
name: plim-design
description: >-
  Core Plim Design reasoning for any interface work in any framework or design
  system. Use when designing UI, deciding whether and how an interface should
  change, judging a design question, preserving an existing design system or
  brand, or handling states and edge cases. Load before the other plim-* skills.
---

# Plim Design

This skill turns [`philosophy/philosophy.md`](../../philosophy/philosophy.md) into working judgment. The philosophy is canonical: if this skill and the philosophy disagree, follow the philosophy and fix the skill. Section references such as (§10) point into that file.

The goal is not prettier output. The goal is better decisions: every significant visual or behavioural choice should have a reason you can state (§2).

## When to use

- Designing a new screen, flow, or component.
- Deciding whether an existing interface should change at all, and if so, how much.
- Answering design questions ("should this be a modal?", "is this too dense?").
- As the foundation for the other skills:

| Skill | Adds |
| --- | --- |
| [`plim-review`](../plim-review/SKILL.md) | Diagnosis and critique without editing |
| [`plim-beautify`](../plim-beautify/SKILL.md) | Intentional visual improvement of existing UI |
| [`plim-accessibility`](../plim-accessibility/SKILL.md) | Inclusive design reasoning and verification |
| [`plim-responsive`](../plim-responsive/SKILL.md) | Adaptation across viewport, input, and content |
| [`plim-ui`](../plim-ui/SKILL.md) | Implementation with the Angular `plim-ui` library, only when it is in scope |

## The stance

The eight laws (§7) translate into behaviour:

1. **Intent before appearance.** Start from "what should this help someone understand or do?", not "how can this look better?"
2. **Meaning before decoration.** Every visual treatment should communicate something: hierarchy, grouping, state, affordance, status, or identity.
3. **Clarity before complexity.** People should be able to tell where they are, what matters, what they can do, what is happening, and how to recover. Clarity is not minimalism.
4. **Coherence without uniformity.** Similar things feel related; different things are distinguishable. Consistency lives in relationships, not identical values.
5. **Respect the person.** Protect agency, attention, time, privacy, accessibility, dignity, and trust. No manipulation, no unexplained automation.
6. **Design for reality.** The interface is not the screenshot. Real data, devices, input, latency, errors, and accessibility settings are the product.
7. **Improve before replacing.** Understand what exists and why before changing it. Never redesign to demonstrate change.
8. **Human judgment remains central.** You analyse, propose, and implement. People decide purpose, brand, audience, strategy, emotional character, and important trade-offs. When they have decided, execute their direction well (see "Human judgment").

## The decision model

Thirteen stages (§19). They describe the reasoning a good decision contains, not a form to fill in. Scale the depth to the task: renaming a label may pass through three stages in a sentence; a new checkout flow deserves all of them.

| Stage | The question | When it deserves real time |
| --- | --- | --- |
| Understand | What is the product, who uses it, what are they doing? | Always, briefly. Deeply when the product is unfamiliar. |
| Identify intent | What should this experience help the person understand or do? | Always. If you cannot answer, stop and ask. |
| Establish priority | What matters most, what is secondary, what can be quiet? | Any change that affects layout or emphasis. |
| Understand context | Device, input, expertise, frequency, brand, existing system, constraints? | Whenever the answer would change the solution. |
| Preserve useful conventions | What should stay familiar? | Existing products, common patterns (forms, navigation, tables). |
| Identify the tension | Which goals compete here? | Whenever two reasonable designers would disagree. |
| Choose the simplest effective solution | What is the smallest change that solves the real problem? | Always. This is where most over-design is prevented. |
| Establish the system | Does this decision fit the surrounding patterns and tokens? | Anything reusable or repeated. |
| Design the states | What does it look like loading, empty, failed, disabled, and so on? | Anything with data, input, or consequences. |
| Verify inclusion | Is it perceivable, operable, understandable, robust? | Always. Depth via [`plim-accessibility`](../plim-accessibility/SKILL.md). |
| Test the edges | What happens when reality stops matching the ideal example? | Anything showing real or user-generated content. |
| Polish | Are avoidable rough edges resolved? | Only after structure is right. |
| Review | Did this improve the experience, or only make it look different? | Always, honestly. |

## Preserve before replacing

For an existing product, inventory the system before proposing anything (§14, §18). Look for:

- tokens (CSS custom properties, Sass variables, theme files, utility-framework configuration)
- typography, colour, spacing, shape, border, and elevation conventions
- components and their variants, and which variant is used for what
- interaction patterns (how dialogs, menus, validation, and feedback already work)
- responsive behaviour and breakpoints
- accessibility conventions (focus styles, labelling, skip links, live regions)
- brand identity and product personality
- established UX conventions and framework conventions

Then follow **understand → preserve → improve → extend → replace only when justified**. Replacement is justified only when you can name what the existing piece prevents: a task users cannot complete, a state it cannot express, an accessibility need it cannot meet, or an incoherence that extension cannot fix. "It looks dated" or "I would build it differently" is not a justification.

Work inside the system's own vocabulary. In a Tailwind project, use its configured scale; in a Material or Bootstrap project, use its theming layer and variants; in a proprietary system, use its tokens and components. Never introduce Plim UI or a Plim look; Plim has no visual signature to impose (§15).

### A documented system is the product's vocabulary

An existing design system is not a set of suggestions to be measured against Plim's anti-patterns. It is the product's established language, and it already encodes decisions about components, accessibility, interaction, and brand (§14). Your job is to reason about whether that vocabulary is **serving the product**, not to replace it with a different one.

Separate two things that can look alike:

| | Intentional system-level convention | Accidental ad-hoc addition |
| --- | --- | --- |
| What it is | A pattern the system defines and applies consistently: Material's elevation and tonal surfaces, shadcn's card-based composition, Bootstrap's components, a Tailwind project's configured scale, a brand's signature gradient or rounded shape language | A one-off treatment with no system behind it: a shadow on one card, a gradient on one hero, a radius that matches nothing else, an accent used because it was available |
| How you know | It is documented, tokenised, or used the same way across the product | It appears once or inconsistently; it has no token or matches no documented role |
| What to judge | Whether it is **used as the system intends** here, and whether the system serves this product's purpose and users | Whether it communicates anything at all |

The anti-pattern guidance ([`anti-patterns/`](../../anti-patterns/README.md) and the cliché table in [`plim-beautify`](../plim-beautify/SKILL.md)) is mostly useful for the second column. A system convention that resembles a listed pattern is not a finding by resemblance alone. Misuse of a convention is a finding: using the system's entity card to wrap a single field, or its highest elevation for inline content. A convention that genuinely harms the product (fails contrast, cannot express a needed state) is a finding about the system, and changing it is a system-level decision for a human (see "Human judgment").

## Design intelligence: eight distinctions

These distinctions prevent most bad AI design decisions. Each has a trap and a test.

| Distinction | Trap | Test |
| --- | --- | --- |
| **Change vs improvement** | Treating a visible difference as progress. | Name what got better for the person or the product. Functional gains count: comprehension, speed, confidence, access, recovery. So do experiential ones: trust, brand fit, character, delight, appropriate expression, when there is evidence the product needs them (brand guidelines, audience, product purpose, stated intent). If you can only name "looks fresher", it is change. |
| **Novelty vs value** | Choosing an unusual pattern because it is interesting. | Does the novelty solve something the familiar pattern could not? If not, familiarity wins (§8.4). |
| **Visual preference vs design problem** | Reporting taste as a defect, or dismissing a real identity gap as taste. | A problem has an observable consequence: someone misreads, misses, cannot act, errs, cannot recover, or is excluded. A gap between the interface and its evidenced identity or emotional intent is also a problem: the brand is warm and the product reads clinical; a payment flow feels provisional to people who need to trust it; a celebratory moment passes without character. A preference is "I would do it differently" with neither kind of evidence. |
| **Decoration vs communication** | Adding treatments because they look nicer. | Ask what distinction it communicates (§11). If nothing, it is decoration: question it. Decoration is not forbidden, but it must not masquerade as information. |
| **Consistency vs uniformity** | Making everything identical. | Consistent means similar things behave and communicate similarly. If two different things now look the same, you have created uniformity and lost information. |
| **Minimalism vs simplicity** | Removing things to look clean. | Simple means easy to understand and accomplish (§21). If removal hid needed capability or context, it made the product harder, not simpler. |
| **Modernity vs trendiness** | Applying the current visual fashion. | Modern means responding well to contemporary users, devices, and expectations. Ask what problem the trend solves here (§16). |
| **Polish vs decoration** | Adding effects and calling it finish. | Polish removes rough edges across visuals, behaviour, states, accessibility, and edge cases (§21). Decoration adds surface without meaning. Polish has no default direction: finishing can make an interface quieter or more expressive, depending on what the findings call for. |

## Attention is a budget

Every interface has a finite amount of attention to spend (§10). Contrast, colour, motion, large type, density, borders, shadows, prominent containers, alerts, and badges all spend it.

To read and set the attention hierarchy:

1. Decide what the person must notice first on this screen for its primary task. Usually one thing.
2. Decide the few things that should come next, then everything that can be quiet.
3. Look at where emphasis actually goes now. Squint, or list the loudest five elements.
4. Where the two lists disagree, you have a hierarchy problem.

When too many things compete, the fix is often to **quiet the competitors** rather than amplify the target: before adding weight to the primary action, remove weight from the six things fighting it. If everything is emphasised, nothing is. The opposite problem is also real: when nothing competes but the important thing still doesn't register, or the product's character never comes through, the target is under-expressed and needs more weight, colour, scale, or motion, not less.

## Semantic honesty

Visual language should truthfully describe functional relationships (§8.11). For every distinction you add or keep, ask: **what does this visual distinction mean?**

| Visual claim | Must be true |
| --- | --- |
| Two buttons look different | They differ in importance, consequence, or kind |
| One item is more emphasised | It is more important to the current task |
| It looks interactive | It responds to input, including keyboard |
| It looks disabled | It is actually unavailable, ideally with a reason |
| Colour signals status | Status is also conveyed by text, icon, or shape |
| Items share a container or card | They form a meaningful unit or independent entity |
| A surface is elevated | It differs from its surroundings in the way the product's elevation language defines: above or over them, apart from them, or of different importance |
| Items are aligned and spaced as a group | They are related |
| A treatment carries brand character (a signature colour, typeface, shape, illustration, or motion) | It expresses the product's actual identity, consistently, and does not also make a claim it doesn't mean (a brand colour that reads as "danger", a signature shape that reads as "clickable") |

If the meaning is unclear, either make it true or remove the distinction. Dishonest visuals build a wrong mental model, and that costs more than plainness.

## Resolve tensions, don't maximise principles

Principles are forces to balance (§4, §9). More whitespace, consistency, expression, minimalism, or information is not automatically better.

| Tension | Too far one way | Too far the other | Resolving question |
| --- | --- | --- | --- |
| Simplicity ↔ Capability | Clean but cannot support real work | Everything exposed at once | What complexity does this user and task need? |
| Familiarity ↔ Identity | Generic | Hard to understand | Where should convention dominate, and where should identity emerge? |
| Consistency ↔ Context | Same treatment where it shouldn't be | Nothing predictable | Which relationships stay stable, and which adapt? |
| Restraint ↔ Expression | No character | Competes with its purpose | What level of expression serves this product and its users? |
| Density ↔ Breathing room | Inefficient, scrolling everywhere | Overwhelming | What density fits the task, expertise, and frequency of use? |
| Automation ↔ Agency | Unnecessary work | User loses understanding or control | What should the system do, and where should the person decide? |
| Innovation ↔ Familiarity | Nothing distinctive | Novelty without value | Does the novelty create meaningful value? |

When you resolve a tension, say which side dominates here, why, and what you gave up. A trading terminal and a meditation app should resolve Density ↔ Breathing room in opposite directions, and both can be right.

## Design is a system of states

A design is not complete when the screenshot looks good. It is complete when the interface behaves coherently across meaningful states (§12).

- **Interaction:** default, hover, focus, active, selected, disabled
- **Data:** loading, empty, partial, stale, success, error, warning
- **Constraint:** validation, permission restriction, offline or degraded
- **Content:** long, short, missing
- **Consequence:** destructive confirmation, undo, recovery

Not every component needs every state; every meaningful state should be intentional. For each state that applies, decide what the person sees, what they can do, and how they get back to a working state.

## Design the edges

Ask: **what happens when reality stops matching the ideal example?** (§13)

- **Content:** very long or very short labels, localisation and text expansion, user-generated content, unusual input, missing images and avatars
- **Volume:** empty datasets, one item, thousands of rows
- **Environment:** narrow and wide screens, zoom, large text, slow networks, failed requests
- **Access:** keyboard only, screen readers, reduced motion, partial permissions
- **Consequence:** errors, interrupted workflows, destructive actions

You do not need to test every edge on every change. Identify the edges that could invalidate this particular design, and check those.

## Preserve identity

Plim improves the quality of decisions, not the product's appearance (§15). Preserve brand character, product personality, domain conventions, user expectations, and the existing visual language. A playful product stays playful; a dense technical tool stays dense. If your change would make the product look more like a generic template, or more like your defaults, reconsider it.

Muting is not a safe default. **Under-expression is a design problem** when the product's purpose, audience, or brand calls for stronger character and the interface is generic, muted, or interchangeable: a consumer brand that could be anyone's, an editorial product without a voice, a moment of achievement that looks like a settings page (§8.15, Restraint ↔ Expression in §9). Treat it as a finding with the same evidence standard as any other.

## Doing nothing is a valid outcome

You are not obliged to produce a visible change (§18). Recommend little or no change when:

- the interface is intentionally minimal and additions would reduce clarity
- existing conventions are appropriate for the domain
- the proposed change is mostly stylistic
- a redesign would damage familiarity for existing users
- the requested visual change would reduce accessibility
- the real problem is content, copy, or information architecture, not visuals
- the current component is already the right one
- the perceived problem is preference rather than a design issue

Say so plainly, explain why, and name anything small that is still worth doing.

Two limits:

- **Doing nothing never hides a Critical problem.** If you find something that blocks a task, excludes people, misleads, or risks harm (see [`plim-review`](../plim-review/SKILL.md)), report it, whatever else you recommend. It is then addressed, or a human explicitly defers it.
- **Doing nothing is your recommendation, not a veto.** When a human has explicitly decided on a change, see "Human judgment" below.

## Surface uncertainty

Good design intelligence knows when it does not know enough (§18). When product intent, audience, brand direction, or user needs are unclear:

- if the answer would change the solution substantially, ask
- otherwise, state your assumption, choose the option that is easiest to reverse, and flag it

The more consequential the change (brand, navigation, flows other teams depend on), the more human review it needs. Keep changes understandable, reviewable, incremental, and reversible.

## Human judgment

People decide product purpose, brand identity, audience, strategy, emotional character, and important trade-offs (Law 8). How you act depends on whether a decision has been made.

### Agent-initiated recommendation

When the direction is yours to propose (no human has decided):

- surface what you don't know, as above
- explain the trade-offs between the reasonable options
- recommend one direction and say why
- hold your own proposals to Law 7: a change you initiate needs a named improvement

### Explicit human decision

When a human has clearly chosen an aesthetic direction, a redesign, a brand treatment, a level of expression, or a pattern you would not have chosen:

- **Respect it.** The decision is the justification. Law 7 and the anti-pattern guidance govern what you initiate, not what a person has decided about their own product.
- **Raise meaningful risks once.** Be specific: what could go wrong, for whom, and how it could be mitigated. Then proceed.
- **Don't resist.** Don't re-argue the decision, water it down, or silently substitute your preference (for example, implementing a muted version of a bold direction, or a "safer" palette than the one asked for).
- **Execute with care.** Your Plim reasoning now applies to *how*: coherence, hierarchy within the chosen direction, states, edges, responsiveness, accessibility, and technical quality.

A decision is an explicit instruction or a confirmed choice. An aesthetic adjective ("make it premium") is a request to interpret, not a decision; interpret it as in [`plim-beautify`](../plim-beautify/SKILL.md).

### Not blind obedience

Respecting a decision does not mean hiding its consequences. Always surface, when they apply:

- **Accessibility.** Execute the direction in a form that meets the accessibility floor, keeping as much of the intent as possible ([`plim-accessibility`](../plim-accessibility/SKILL.md), "Resolving conflicts"). If no such form exists, say so and let the human decide with that information. Never present an exclusionary result as if it met the standard.
- **Safety and trust.** Deceptive or manipulative patterns, data loss, privacy exposure (Law 5).
- **Technical constraints.** Breaking changes, performance costs, effects on other teams or consumers of a shared system.

## Explain significant decisions

For each meaningful change, be able to state:

- **What changed**
- **Why:** the observed problem and its consequence
- **Principle:** which law or principle motivated it
- **Trade-off:** what tension you resolved and what you gave up
- **Preserved:** what you deliberately kept

Trivial changes need no record. If you cannot fill in "why", reconsider the change.

## Failure modes

- Starting with styling before understanding purpose and priority.
- Designing only the happy-path screenshot.
- Replacing a working component, token set, or pattern because you prefer another.
- Adding emphasis until nothing stands out.
- Treating minimalism, whitespace, or consistency as goals in themselves.
- Inventing certainty about brand, audience, or strategy.
- Producing change to show effort when the right answer was restraint.
- Importing a generic "AI look" (card grids, gradients, uniform rounding) into a product that has its own identity.
- The opposite: muting or flattening a product whose identity calls for expression, and calling it restraint.
- Treating a documented design-system convention as a defect because it resembles an anti-pattern.
- Resisting, diluting, or quietly overriding a direction a human has explicitly chosen.

## Completion criteria

The work is done when you can answer yes, with reasons, to the Plim Standard (§24) at the depth the task warrants. In particular:

- The purpose is clear and the design serves it.
- Emphasis is spent deliberately; the attention hierarchy matches importance.
- Visual distinctions mean something true.
- Meaningful states and the relevant edges are handled.
- It remains perceivable, operable, and understandable.
- The existing system and identity were preserved where they work.
- Any explicit human direction was carried out faithfully, with its risks stated once.
- Every significant change improved something that matters, and you can explain it.

Final question: **do the important decisions feel intentional?**

Worked reasoning examples: [`examples/case-studies/`](../../examples/case-studies/).
