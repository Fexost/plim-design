# Examples

Worked reasoning, not before/after galleries. The case studies are a reasoning test suite: they show how Plim Design behaves when purpose, existing systems, accessibility, expression, and human decisions interact.

Each case makes its reasoning visible in roughly the same order, using only the sections it needs:

```text
Context → What the agent notices (findings with severity and intent)
→ Principles and tension → Alternatives considered → Decision (outcome)
→ Trade-off accepted → Implementation direction → Expected result
```

Decisions in a case are scoped to that case. They are examples of reasoning, not rules: "for this interface, X was appropriate because…" never means "Plim says X". Across the collection, outcomes run in both directions: some cases quiet an interface, and others strengthen its expression.

Load only the case that resembles the task at hand.

## Case studies

| Case | Demonstrates | Outcome | Skills |
| --- | --- | --- | --- |
| [Generic SaaS dashboard](case-studies/01-generic-saas-dashboard.md) | Hierarchy and IA before styling; brand colour concentrated where action is | Structural intervention | review, beautify |
| [Dense enterprise table](case-studies/02-dense-enterprise-table.md) | Keeping necessary density; responsive tables | Targeted improvement | design, responsive, accessibility |
| [Angular settings page using plim-ui](case-studies/03-angular-settings-plim-ui.md) | Misuse of a system component, not the component itself | Targeted improvement | design, plim-ui, accessibility |
| [Tailwind application](case-studies/04-tailwind-application.md) | Converging on an existing system; blast radius; a Critical finding inside a polish request | Targeted improvement plus polish | design, beautify |
| [Highly branded application](case-studies/05-highly-branded-application.md) | Aiming and strengthening expression; intentional but failing | Targeted improvement | design, beautify, accessibility |
| [Mobile checkout](case-studies/06-mobile-checkout.md) | Adapting rather than shrinking; recovery | Structural intervention | design, responsive, accessibility |
| [Legacy Bootstrap interface](case-studies/07-legacy-bootstrap.md) | Interpreting "modernise"; agent does not initiate a redesign | Targeted improvement, staged | review, beautify |
| [Beautiful but inaccessible interface](case-studies/08-beautiful-but-inaccessible.md) | Requirements versus recommendations; accessible options for the human to choose | Targeted improvement | accessibility, review |
| ["Make this premium"](case-studies/09-make-it-premium.md) | Premium as craft and identity; the founder chooses the expression | Targeted improvement | beautify |
| ["Make this modern"](case-studies/10-make-it-modern.md) | Modern as contemporary usefulness, with a legitimate visual refresh | Structural intervention | beautify, responsive |
| [AI-generated card-heavy interface](case-studies/11-ai-generated-card-interface.md) | Ad-hoc card soup; character moved from boxes to brand | Structural intervention | review, beautify |
| [Polish only: a plain tool that works](case-studies/12-little-or-no-change.md) | Restraint that is the product's identity; character left to the user | Polish only | review |
| [Under-expressed brand](case-studies/13-under-expressed-brand.md) | Adding character as the improvement | Targeted improvement | design, review, beautify, accessibility |
| [Human-chosen bold direction](case-studies/14-human-chosen-bold-direction.md) | Executing a human's direction without taming it | Execute a human direction | design, responsive, accessibility |
| [Mature design system](case-studies/15-mature-design-system.md) | Conventions that resemble anti-patterns; judging use, not resemblance | Targeted improvement | review, design |
| [Explicit redesign request](case-studies/16-explicit-redesign-request.md) | Human-chosen redesign versus agent-initiated redesign | Execute a human direction (a redesign) | design, review, accessibility |
| [Genuine no change](case-studies/17-genuine-no-change.md) | Why no intervention is justified, with evidence and cost | No change | review, design |

## Reference interfaces

[`reference-interfaces/`](reference-interfaces/) is reserved for annotated real-world references.

> TODO: Curate reference interfaces. They must be annotated with reasoning and must not be presented as the Plim visual identity.
