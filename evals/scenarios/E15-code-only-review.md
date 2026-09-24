# E15 · Code-only review with no brand evidence

**Skills to load:** plim-design, plim-review, plim-accessibility

## Given to the agent

**Brief:** "Review our app's UI. We don't have designers. Here's the repo."

**Context:** Only the code is available: no screenshots, brand guidelines, research, or analytics. From the code:

- A `theme.ts` defines a grey palette, one blue (`primary`), a 4px spacing base, and 6px radius. About 90% of the components use these values; `Button`, `Input`, `Card`, and `Table` use them throughout.
- The `ReportsPage` component uses raw values found nowhere else: `#7c3aed` purple, a 20px radius, and `box-shadow: 0 20px 40px`.
- `button:focus { outline: none; }` is in the global stylesheet, with no replacement focus style.
- The `ProjectList` component has branches for loading and error but none for an empty list.
- The app has 60 routes.

## Withheld

**Expected outcome:** Targeted improvement, recommended.

**Required behaviours**

- States the assumptions it reviews against and that the hierarchy is inferred from code, not seen. — [`evidence.md`](../../skills/plim-review/evidence.md), "When evidence is thin", "Reviewing from code alone"
- Reports the removed focus outline as Critical (or at least an accessibility requirement failure), with full severity, despite the thin evidence. — same file, "Observable consequences still stand"; `plim-review`, "Classify findings"
- Treats the `theme.ts` values as a provisional convention by frequency and token use, and the `ReportsPage` values as likely ad hoc, with intent Unknown. — same file, "Convention or ad hoc"
- Reports the missing empty state for `ProjectList`. — same file, "States"
- Treats any identity question (is the plain grey look chosen?) as a question for the team, not an Important finding. — same file, "An identity gap without evidence is a question"
- States coverage: which of the 60 routes or which shared components it reviewed, and what it could not assess (rendered contrast, screen reader behaviour). — same file, "Scoping a large product"; `plim-review`, "Completion criteria"

**Disqualifying behaviours**

- Invents user research, personas, or analytics. — [`evidence.md`](../../skills/plim-review/evidence.md), "Don't invent evidence"
- Files "the app looks generic" or "lacks brand character" as an Important finding. — same file
- Recommends a new visual identity, or a new component library. — `plim-design`, "Preserve before replacing"
- Edits code (this is a review). — `plim-review`, "When to use"
