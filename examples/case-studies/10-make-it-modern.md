# "Make this modern"

**Skills:** plim-beautify, plim-responsive · **Stress test:** Scenario F

## Context

A public library's catalogue and account site. A board member says it "doesn't look modern". The audience is broad: older patrons, students, people on shared public computers and cheap phones.

## Existing problem

The site uses dated table-based layouts, tiny text, a mega-menu of 60 links, and a search results page that doesn't work on phones. Renewing a loan takes five steps.

## What the agent notices

- A trend-driven response (glassy hero, bento grid, big gradient headings, animations) would add weight on low-end devices and do nothing about the real problems.
- Plausible meanings of "modern" here: works on phones, readable text, simpler navigation, faster common tasks, better accessibility.
- The tasks that matter are search, reserve, and renew.

## Relevant Plim principles

Modern as appropriate response to contemporary users and contexts (§21), Against trend-driven design (§16), Purpose (§8.1), Adaptability (§8.9), Inclusion (§8.10).

## Tension

**Innovation ↔ Familiarity.** Long-time patrons know the current site; the board wants visible renewal.

## Decision

Clarify with the requester what "modern" should achieve, proposing the interpretation above. Modernise the experience around the three core tasks, with a visual refresh that follows from better structure rather than leading it.

## Implementation direction

- Make search the focal point of the home page; group the 60 links into a small number of clear sections.
- Rebuild search results to adapt on narrow screens: title, author, availability, and a reserve action per result, with filters in a disclosure panel.
- Reduce renewal to one step from the account page, with clear confirmation.
- Raise base text size and contrast; refresh typography and spacing coherently.
- Keep pages light for slow connections and shared computers.

## Expected result

The site looks current because it behaves like a current site: readable, fast, usable on a phone, and quick for everyday tasks. It isn't wearing this year's trend, so it won't look dated next year.
