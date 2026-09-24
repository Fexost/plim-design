# Dense enterprise table

**Skills:** plim-design, plim-responsive, plim-accessibility · **Outcome:** targeted improvement

## Context

An insurance claims tool built on an internal component library with a data-table component. Adjusters work all day in a table of claims with 14 columns (ID, claimant, policy, status, amount, dates, assignee, region, flags). They sort, filter, and compare rows constantly. The user asks: "This table looks overwhelming. Make it cleaner."

## What the agent notices

- **None, intentional.** The density is deliberate and serves its purpose: adjusters are experts with high frequency of use, and they compare 30 or more rows at once. "Overwhelming" doesn't come from the number of rows.
- **Important, accidental.** The noise comes from borders on every cell, bold text in five columns, and no alignment discipline (amounts left-aligned, dates in mixed formats).
- **Important, accidental.** On laptop widths the last columns are clipped with no scroll cue, and the identifying column scrolls away, so users lose track of the row.
- **Important, accidental; accessibility requirements.** Status is a coloured dot alone, and sort state isn't exposed to assistive technology. The faint sort arrow is also hard to see.

## Principles and tension

Appropriate complexity (§8.12), Clarity (§8.2: "a dense interface can be clear"), Inclusion (§8.10), Design for reality (Law 6).

**Density ↔ Breathing room.** "Cleaner" invites more padding or cards, which would halve the visible rows and slow the work the table exists for.

## Alternatives considered

- **Convert rows to cards.** Rejected: it breaks column comparison, which is the core task.
- **Increase row padding for everyone.** Rejected as the default, because it costs visible rows. Offered instead as a per-user density setting.
- **Hide low-use columns by default.** Rejected: adjusters use them, and hiding them is the adjusters' call. Column visibility is offered instead.
- **Add horizontal scrolling only.** Rejected on its own: rows lose their identity as they scroll.

## Decision

For this table, the density stays. Noise, alignment, and orientation are fixed in the places the findings identify, using the existing table component.

## Trade-off accepted

Lighter separation between cells makes individual columns slightly less boxed in; right-alignment and consistent formats compensate. A density setting adds one control to the toolbar.

## Implementation direction

- Reduce separation to what the structure needs, such as row rules or zebra striping, whichever the component library supports. Keep a clear header.
- Limit bold text to the claim ID; right-align amounts with tabular numerals; standardise the date format.
- Pin the ID and claimant columns; allow horizontal scroll for the rest, with a visible cue that more columns exist.
- Offer column visibility and a saved compact or comfortable density setting.
- Give status a text label beside the dot. Sortable headers expose and show their sort state.
- Keyboard: headers operable as buttons, visible focus on rows or cells, filters reachable before the table.
- States: loading without collapsing the layout, "no claims match these filters" with a clear-filters action, and partial failure when one data source is unavailable.

## Expected result

The same amount of information scans faster. Nothing adjusters rely on was removed; the table looks deliberate rather than crowded.
