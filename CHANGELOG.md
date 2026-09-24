# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) where applicable.

## [1.0.0] - 2026-09-24

First public release. Plim Design is a philosophy and an agent skill library, not a visual theme. Install with `npx skills add Fexost/plim-design`.

### Stable capabilities

- Canonical philosophy and manifesto: intentional interfaces, with no prescribed look.
- Design reasoning: decision model, distinctions, tensions, outcomes, and human judgment within accessibility requirements.
- Accessibility as a constraint: requirements, above-floor improvements, and an explicit open record when a human rejects every accessible alternative.
- Attention as a resource and a canonical state model, including combinations and transitions.
- Agency and automation, decided by consequence, reversibility, confidence, intent, and frequency.
- Greenfield foundations and density from product evidence, and preservation of existing design systems.
- Evidence discipline for thin and code-only reviews, including who owns a decision.
- Decision records for human decisions, conventions, foundations, and unresolved consequential issues, written only when an entry is warranted.
- Interface language: voice, tone by state, and terminology.
- Framework-agnostic skills (`plim-design`, `plim-review`, `plim-beautify`, `plim-accessibility`, `plim-responsive`) and an optional `plim-ui` implementation skill.
- A behavioural evaluation suite. Evals check the skills; they do not define them.
- Agent Skills CLI compatibility: `skills/<name>/SKILL.md` with `name` and `description` frontmatter.
- A manual **Release** workflow (`.github/workflows/release.yml`). Run it from `main` to tag the version and publish the GitHub release.

### Added

- Initial repository architecture: philosophy, foundations, composition, interaction, accessibility, patterns, anti-patterns, recipes, skills, integrations, examples, and adapters.
- Root documentation: `README.md`, `AGENTS.md`, and MIT `LICENSE`.
- Six skills implemented from `philosophy/philosophy.md`: `plim-design` (reasoning core), `plim-review`, `plim-beautify`, `plim-accessibility`, `plim-responsive`, and `plim-ui` (optional Angular implementation mapping).
- Twelve reasoning case studies in `examples/case-studies/`.
- `anti-patterns/` written as supporting depth for philosophy §16–17, with a README defining its authority, and two new files: `typography-inflation.md` and `unnecessary-redesign.md`.
- `skills/plim-ui/reference.md`: versioned plim-ui facts, verified against `plim-ui@0.2.0` and `main` at `3ca689f`, including a known-divergences table.
- `skills/plim-ui/MAINTAINING.md`: lightweight update and review process for the plim-ui reference.

### Changed

- Manifesto moved from `philosophy/philosophy.md` §26 into `philosophy/manifesto.md`; §26 now references it.
- `plim-ui` skill split into stable reasoning (`SKILL.md`) and versioned facts (`reference.md`); it now states that Plim Design is the source of truth for plim-ui design decisions and covers improving plim-ui itself.
- Replaced the `examples/before-after/` placeholder with `examples/case-studies/`, which holds worked reasoning instead of screenshot galleries.
- `recipes/beautify-interface.md` now points to `plim-beautify` instead of carrying a separate outline.
- Hostile-review P0 fixes, so the skills no longer imply a Plim visual aesthetic:
  - `plim-beautify`: cliché table reframed around what each pattern claims, when it is legitimate, and alternative ways to achieve the intent; under-expression added; the table now targets ad-hoc additions, not system conventions. New post-audit outcome gate (no change, polish only, targeted improvement, structural intervention, redesign); every intervention traces to a finding or human direction; Critical findings cannot be left in place by a smaller outcome; blast radius added to the intervention model; no-change output shape.
  - `plim-design`: experiential outcomes (trust, brand fit, character, delight, expression) count as improvements with evidence; identity gaps count as problems; brand character added to semantic honesty; elevation meaning follows the product's elevation language; "polish usually makes things quieter" removed; under-expression named as a problem; new "A documented system is the product's vocabulary" section; new "Human judgment" section separating agent recommendations from explicit human decisions; limits on "doing nothing".
  - `plim-review`: severity and intent are separate axes; "intentional" requires evidence the purpose is served; Polish requires a departure from the product's own system or an objective craft defect.
  - `anti-patterns/README.md`: scope limited to ad-hoc additions; overcorrection and human decisions noted.
  - `AGENTS.md` and `README.md`: "reject generic AI UI" replaced with questioning generic patterns; expression and character stated alongside restraint; human decisions respected; placeholder documents no longer cited as authority; "a philosophy, not a look" stated.
- Accessibility and human judgment policy (first P1 item): "Accessibility is a foundational constraint, not a preference. Human judgment operates within that constraint."
  - `plim-accessibility`: new "Requirements, recommendations, and human judgment" section distinguishing requirements (at the product's conformance target, or WCAG 2.2 AA by default), above-floor improvements, and preferences; a procedure for when an explicit human direction can't meet a requirement; conflict table and failure modes updated to match.
  - `plim-design`, `AGENTS.md`, and case study 08 aligned with the policy and its terms.
- Case studies audited and strengthened (P1.2):
  - All twelve existing cases revised to show findings with severity and intent, the chosen outcome, alternatives considered, and the trade-off accepted, with decisions scoped to the case. Removed implied universal rules (for example, a hard-coded neutral palette in case 07 and an elevation rule in case 11) and the collection's bias towards quieter outcomes.
  - Case 12 retitled "Polish only" to match its outcome.
  - Five new cases: under-expressed brand (13), human-chosen bold direction (14), mature design system (15), explicit redesign request (16), and genuine no change (17).
  - `examples/README.md` index updated with each case's outcome.
- Attention and state reasoning (P1.3):
  - `plim-design`: "Attention is a budget" became "Attention is a resource", allocated by what matters right now. It covers distributed attention, priority that changes with state, concurrent urgent states, and prominence versus importance, and drops the "usually one thing" default. "Design is a system of states" is now the canonical state model, covering combinations, transitions, and the links between state, attention, feedback, and agency. Edges connect to it.
  - `plim-review`, `plim-beautify`, `plim-responsive`, and `plim-accessibility` reference the canonical model instead of carrying their own state lists; the single-focal-point wording in review and beautify was removed.
- Greenfield and density reasoning (P1.4):
  - `plim-design`: new section "When there is no system to preserve", covering starting from evidence, deriving each foundation from its job, choosing density per context, how much structure to build, convention versus context, avoiding premature proliferation, resolving tensions explicitly, and greenfield failure modes.
  - `recipes/build-interface.md` now points to that section; `foundations/density.md` gains a pointer while it remains a placeholder.
- Automation and agency (P1.5):
  - `plim-design`: new section "Automation and agency". Consequence, reversibility, confidence, expressed intent, and frequency decide between act, act and inform, suggest, preview, ask, and confirm. It covers when interruption is justified, applies the model to destructive, background, default, AI-generated, batch, irreversible, recurring, and long-running actions, and gives a test for reduced work versus removed control. The tension row and failure modes link to it.
  - `plim-review`: the Interaction lens judges automation against consequence and reversibility.
- Familiarity and identity (P1.6):
  - `plim-design`: new section "Familiarity and identity", covering recognisable behaviour with distinctive character, the factors that decide the trade-off (task and consequence, audience and frequency, existing expectations, product identity, evidence), four situations, and innovation versus novelty. The "Novelty vs value" test no longer makes familiarity the default winner; the greenfield guidance and tension rows link to the new section; one failure mode added.
  - `plim-review`: the Identity lens asks whether unconventional behaviour earns its learning cost.
- Authority cleanup, contradictions (P2.1a):
  - `anti-patterns/`: "Repair" lists in `excessive-colour`, `excessive-decoration`, `card-soup`, `visual-noise`, `excessive-rounding`, and `typography-inflation` rewritten as directions chosen by meaning. Removed the residual defaults (accent reserved for action with neutrals elsewhere, a fixed page/raised/overlay/modal elevation model, removing motion that isn't tied to state, one container level, pills for one role, quieting before strengthening).
  - `plim-design`: new canonical "Outcomes" section (no change, polish only, targeted improvement, structural intervention, redesign, and the new "execute a human direction"), with the rule that Critical findings and accessibility requirement failures at any severity override the outcome.
  - `plim-beautify` keeps only the steps that follow each outcome; `plim-review` recommends from the canonical scale and labels requirement failures separately from severity; `plim-accessibility` states the gate consequence.
  - Cases 14 and 16 and the examples index use the new outcome name; `recipes/redesign-interface.md` no longer assumes identity is preserved.
- Authority cleanup, documentation architecture (P2.1b):
  - Every file in `foundations/`, `composition/`, `interaction/`, `accessibility/`, `patterns/`, `integrations/`, and `recipes/` is now a signpost naming the skill section that owns its topic, with no TODOs and no guidance of its own.
  - Removed `patterns/search.md` and `patterns/settings.md` (no owning reasoning) and `philosophy/principles/README.md` (planned per-principle documents would have duplicated philosophy §8).
  - Removed the undefined "stress-test scenario" labels from the case studies and their index.
  - `README.md` (layer table, repository map, status with seventeen case studies), `AGENTS.md` ("Unfinished content"), and `skills/README.md` (framework independence) describe the signposts.
- Decision records (P2.2):
  - New `skills/plim-design/decision-records.md`: where a product's record lives (its existing decision docs, otherwise `DESIGN-DECISIONS.md`), how to read it, entry types (Decision, Convention, Foundation, Open, Declined), format, who writes what, lifecycle, and precedence. Entries are written only for decision-worthy events, never as an activity log.
  - `plim-design` reads the record at "Understand" and in the system inventory, treats recorded decisions as explicit, keeps greenfield rationale as Foundation entries, and writes only decision-worthy events. `plim-beautify` reads it at step 1 and writes such events in its output; `plim-review` reads it and proposes entries without writing unless asked; `plim-accessibility` records unresolved requirement conflicts as Open entries.
- Evaluation suite, format and baseline (P2.3a):
  - New `evals/README.md`: evals check behaviour and never define it; every check cites a skill section; no expected look; how to run in a fresh session, grade by a separate grader with pass or fail evidence and no numeric scores, and tell agent failures from skill gaps.
  - Fourteen baseline scenarios (E01–E12b) covering no change, polish only, under-expression, an explicit bold direction, mature-system conventions, a rejected accessibility alternative, distributed attention and combined states, greenfield foundations across three briefs, AI batch automation, a justified and an unjustified departure from convention, and two evidence pairs (a documented versus ad-hoc gradient, on a shared code fixture; a dense table for experts versus occasional users).
- Systems and libraries (P2.5a):
  - New `skills/plim-design/systems.md`, framework-agnostic: a library's default look is its own identity, not Plim's, and must be replaceable; theming at the layer of meaning with behaviour and accessibility stable across themes; variants and options as vocabulary; the states, accessibility, content resilience, and usage guidance each component carries; consumer evidence; evolving a shared system (blast radius, human decisions, additive change, staging, rebrands).
  - `plim-design` links to it from "When to use", "How much structure", and "A documented system is the product's vocabulary", and its description mentions shared systems; `recipes/theme-existing-interface.md` points to it.
- plim-ui reconciliation (P2.5b, deferred P0 item 7):
  - `plim-ui` precedence: `DESIGN-AGENTS.md` is no longer a design source; plim-ui's own look is its maintainer's decision, derived with Plim reasoning and recorded in plim-ui's decision record.
  - Concept map aligned with the current skills: "Attention budget" became "Attention", the "usually one primary action" default and the "predominantly flat" elevation guidance were replaced with meaning-based wording.
  - "Improving plim-ui itself" keeps only plim-ui specifics and links to `systems.md` for general library reasoning; failure modes updated.
  - `reference.md` and `MAINTAINING.md` describe the divergence log as tracking, not authority.
- Working with partial evidence (P2.4):
  - New `skills/plim-review/evidence.md`: an order of evidence from stated decisions to inference; what to do when evidence is thin (observable consequences keep their severity, intent is Unknown, identity gaps without evidence are questions, no invented evidence); reviewing from code alone, including provisional conventions; scoping a large product; identifying who decides and surfacing stakeholder disagreement.
  - `plim-review` links to it from the procedure and evidence discipline, and adds two failure modes; `plim-design` "Surface uncertainty" asks the decision owner.
- Interface language (P2.6):
  - New `skills/plim-design/language.md`: voice as part of brand (a human decision, with no Plim voice, and under-expression in words), tone by state and consequence, one name per concept and preserved domain terms, labels and actions that say what happens, language and access, and when the fix is words rather than visuals.
  - `plim-design` points to it from the stance and from transitions in the state model; `plim-beautify` rung 1 links to it; `plim-review` folds language into the Information architecture and Identity lenses; `patterns/errors.md` signposts it.
- Evaluation suite, scenarios for P2 content (P2.3b): E13–E20 cover reading a decision record in a later session (with a record fixture), writing only decision-worthy events, a code-only review without brand evidence, a requester who isn't the decision owner, default themes for a shared library, plim-ui's own look, a fix that is words rather than visuals, and clearer errors that keep a brand's voice.
- Pre-v1 audit: `plim-responsive` no longer treats empty space on large displays as inherently not luxurious; generous space is legitimate when it is the product's character. `AGENTS.md` tells agents not to load `evals/` as design guidance. `README.md` status includes the skill reference files and the evaluation suite.
- Evaluation suite, first run (P2.3c): all 22 scenarios passed, recorded in `evals/results/2026-09-24-run-1.md`. Two ambiguities in `decision-records.md` were fixed from the run: unconfirmed recommendations and already-evident conventions are not recorded, and context given in answer to a question becomes a Decision entry only when confirmed as one. The link check also found and fixed pre-existing broken relative links in `adapters/generic/README.md`.
