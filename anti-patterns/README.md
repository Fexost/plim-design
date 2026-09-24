# Anti-patterns

Deeper supporting material on the failure modes described in [`philosophy.md`](../philosophy/philosophy.md) §16 (Against trend-driven design) and §17 (Common AI interface failure modes).

## Authority

- **The philosophy is canonical.** These files explain its failure modes in more depth; they do not add rules.
- **Nothing here is forbidden** (§16). Every pattern has legitimate uses, and each file says when. The question is always **what does this accomplish?**
- **The operational summary** lives in the cliché table of [`plim-beautify`](../skills/plim-beautify/SKILL.md). Agents use that table while working, and come here when they need to recognise a pattern with confidence, explain it, or avoid overcorrecting.

- **Ad-hoc additions, not system conventions.** These files are most useful for one-off treatments with no system behind them. A documented convention of the product's design system (Material elevation, shadcn cards, Bootstrap components, a Tailwind scale, a brand's signature shapes or gradients) is the product's vocabulary. Resembling a pattern here doesn't make it a problem; judge whether it is used as the system intends (see [`plim-design`](../skills/plim-design/SKILL.md), "A documented system is the product's vocabulary").
- **Overcorrection is a failure too.** Removing expression, colour, elevation, or motion that the product's identity calls for is not a repair. Under-expression is covered in the `plim-beautify` table.
- **Human decisions come first.** If a person has explicitly chosen a pattern listed here, these files inform how to execute it well, not whether to resist it.

If a file here seems to contradict the philosophy or a skill, the philosophy wins and the file should be fixed.

## Shape of each file

| Section | Purpose |
| --- | --- |
| Core question | The question from the philosophy that tests for the pattern |
| Recognising it | Observable signals, in code and on screen |
| Why it happens | The reasoning shortcut behind it, especially in AI-generated UI |
| Why it matters | The consequence for people, tied to principles |
| When it is not a problem | Legitimate uses, so the pattern isn't removed by reflex |
| Diagnosing | Questions that separate the problem from a valid choice |
| Repair | Directions, smallest effective change first |
| Overcorrection | The opposite failure to avoid |

## Files

| File | Covers | Philosophy |
| --- | --- | --- |
| [generic-ui.md](generic-ui.md) | The root causes: signal substitution, trend substitution, screenshot optimisation, dashboard syndrome, aesthetic presets | §16, §17 |
| [card-soup.md](card-soup.md) | Card soup, excessive containers | §17, §8.11 |
| [excessive-decoration.md](excessive-decoration.md) | Shadows, glass, blobs, decorative icons, decorative and meaningless motion | §17, Law 2, §8.14 |
| [excessive-rounding.md](excessive-rounding.md) | Uniform rounding, pills everywhere | §17 |
| [excessive-colour.md](excessive-colour.md) | Accent overload, gradients, colour-only meaning | §17, §10 |
| [typography-inflation.md](typography-inflation.md) | Giant headings, size as the only hierarchy tool | §17, §8.6 |
| [visual-noise.md](visual-noise.md) | Borders, badges, competing signals, random asymmetry | §10, §8.7 |
| [inconsistent-patterns.md](inconsistent-patterns.md) | Arbitrary values, divergent components, and the opposite failure, uniformity | Law 4, §8.5 |
| [unnecessary-redesign.md](unnecessary-redesign.md) | Replacing what works | Law 7, §17, §18 |
