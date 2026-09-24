# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html) where applicable.

## [Unreleased]

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
