# Dense enterprise table

**Skills:** plim-design, plim-responsive, plim-accessibility · **Stress test:** Scenario B

## Context

An insurance claims tool. Adjusters work all day in a table of claims with 14 columns: ID, claimant, policy, status, amount, dates, assignee, region, flags. They sort, filter, and compare rows constantly. The user asks: "This table looks overwhelming. Make it cleaner."

## Existing problem

The table is dense, has heavy borders on every cell, uses bold text in several columns, and status is a coloured dot. On laptop widths the last columns are clipped with no scroll cue. Sorting state is unclear.

## What the agent notices

- Density is not the problem. Adjusters are experts with high frequency of use; they need to compare many rows at once.
- The noise comes from borders on every cell, bold text in too many columns, and no alignment discipline (amounts left-aligned, dates in mixed formats).
- The identifying column scrolls away horizontally, so users lose track of which row they are on.
- Status relies on colour alone, and sort direction is shown only by a faint arrow.

## Relevant Plim principles

Appropriate complexity (§8.12), Density ↔ Breathing room (§9), Clarity (§8.2: "a dense interface can be clear"), Inclusion (§8.10), Design for reality (Law 6).

## Tension

**Density ↔ Breathing room.** "Cleaner" could tempt a move to cards or generous row padding, which would cut the visible rows by half and slow the actual work.

## Decision

Keep the density. Reduce noise and improve scanning instead. Do not convert to cards, and do not simply add horizontal scrolling without keeping the row's identity visible.

## Implementation direction

- Replace cell borders with subtle row separators; keep a clear header.
- Limit bold text to the claim ID; right-align amounts with tabular numerals; standardise date format.
- Pin the ID and claimant columns; allow horizontal scroll for the rest, with a visible cue that more columns exist.
- Offer column visibility and a saved compact or comfortable density toggle, so users choose.
- Status gets a text label with the dot. Sortable headers announce sort state and show a clear direction indicator.
- Keyboard: headers operable as buttons, focus visible on rows or cells, filters reachable before the table.
- States: loading without collapsing the layout, "no claims match these filters" with a clear-filters action, and partial failure when one data source is unavailable.

## Expected result

The same amount of information feels calmer and scans faster. Nothing adjusters rely on was removed; the table looks deliberate rather than crowded.
