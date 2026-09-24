# Beautiful but inaccessible interface

**Skills:** plim-accessibility, plim-review · **Stress test:** Scenario G

## Context

A boutique hotel booking site with an admired visual design: pale grey text on off-white, hairline borders, focus outlines removed, an icon-only navigation, and a full-screen background video behind the booking form.

## Existing problem

Guests using screen readers, keyboards, or older phones struggle to book. Complaints include "can't read the dates" and "the form doesn't work with the keyboard".

## What the agent notices

- The aesthetic intent is calm, light, and luxurious. That intent is legitimate and part of the brand.
- Body text and date labels fall below readable contrast. Input borders are nearly invisible.
- With focus outlines removed, keyboard users can't see where they are. The date picker is a custom widget with no keyboard support.
- Icon-only navigation has no accessible names.
- The video behind the form reduces legibility, never stops, and has no reduced-motion handling.

## Relevant Plim principles

Inclusion (§8.10, §22), Respect the person (Law 5), Semantic honesty (§8.11), Restraint ↔ Expression (§9).

## Tension

**Restraint ↔ Expression**, and aesthetics against access. The brand wants lightness; guests need to read and operate the form.

## Decision

Inclusion wins, and the calm, light intent is preserved through different means.

## Implementation direction

- Darken body and label text to readable contrast while keeping it warm grey; keep lightness through generous line height and restrained weight rather than pale colour.
- Strengthen input boundaries enough to meet non-text contrast, using the same hairline style with a darker tone.
- Design a focus indicator in the brand language, such as a thin offset ring in the accent tone, and restore it everywhere.
- Replace the custom date picker with an accessible pattern (native input or a well-tested accessible component), styled to match.
- Give navigation icons accessible names and visible labels on larger screens.
- Place the booking form on a solid panel over the video; pause the video by default under reduced motion and provide a pause control.

## Expected result

The site still feels calm and luxurious. Guests can read it, operate it by keyboard and screen reader, and book without friction. The visual quality most people noticed survives; the barriers are gone.
