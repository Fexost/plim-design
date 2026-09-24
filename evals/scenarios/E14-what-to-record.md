# E14 · Writing the record: decision-worthy events only

**Skills to load:** plim-design, plim-beautify, plim-accessibility

## Given to the agent

**Brief:** "Polish the onboarding screens of our budgeting app, and fix whatever you find."

**Context:**

- A consumer budgeting app with a documented token set and no decision record yet. The repository has no ADRs or design documents.
- Observations you can verify: two typos; inconsistent spacing between onboarding steps (the tokens define it); the progress indicator isn't announced to screen readers; the illustrations on each step have no alternative text, and are decorative.

**Answers to likely questions:**

- If the agent asks about the product's character: "Friendly but serious about money; not cute."
- Partway through, the product owner adds: "Also, we've decided the onboarding will use the illustrated mascot on every step from now on. That's final."
- If the agent asks whether to keep a decision record: "Yes, please."

## Withheld

**Expected outcome:** Polish only, plus executing the product owner's decision (the mascot on every step).

**Required behaviours**

- Fixes the typos, spacing, announcement, and decorative marking, and treats the missing announcement as a requirement. — `plim-beautify`, "Decide the outcome"; `plim-accessibility`, "Dynamic content and states"
- Creates a `DESIGN-DECISIONS.md` at the product root, says so and why, and writes one Decision entry for the mascot, naming the product owner. It may also add a Foundation or Convention entry if it established one. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "Where it lives", "When to write"
- Treats "friendly but serious about money; not cute" as context for its work, and records it only if the product owner confirms it as a decision. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "Who writes what"

**Disqualifying behaviours**

- Entries for the typos, the spacing fix, the accessibility fixes, or a summary of the session. — [`decision-records.md`](../../skills/plim-design/decision-records.md), "When to write"
- Recording its own preferences as decisions. — same file, "Who writes what"
- Resisting or diluting the mascot decision. — `plim-design`, "Human judgment"
