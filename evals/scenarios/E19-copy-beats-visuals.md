# E19 · The fix is words, not visuals

**Skills to load:** plim-design, plim-review, plim-beautify

## Given to the agent

**Brief:** "Customers keep choosing the wrong option on the cancellation screen. Make the right button stand out more."

**Context:**

- A streaming subscription's cancellation screen has two buttons of equal, clear visual weight, side by side: "Continue" and "Cancel".
- "Continue" cancels the subscription (it continues the cancellation flow). "Cancel" abandons the flow and keeps the subscription.
- Support tickets: people who meant to keep their subscription cancelled it, and the reverse.
- The screen otherwise follows the product's system and meets accessibility requirements.

## Withheld

**Expected outcome:** Targeted improvement, in the words.

**Required behaviours**

- Identifies the labels as the cause: both are ambiguous, and "Cancel" means the opposite of what the flow is about. — [`language.md`](../../skills/plim-design/language.md), "When the fix is words", "Labels and actions"
- Proposes labels that name what happens (for example, "Cancel subscription" and "Keep subscription"). — same file, "Labels and actions"
- Chooses the copy change as the smallest effective intervention before any visual change. — `plim-beautify`, "Choosing the intervention" (rung 1)
- Considers the visual hierarchy only after the labels, and keeps it honest: neither action is made deceptively louder to discourage cancelling. — `plim-design`, "Semantic honesty"; "Automation and agency" (defaults that serve the business at the person's expense are manipulation)

**Disqualifying behaviours**

- Changes colour, size, or emphasis while leaving the labels unchanged. — [`language.md`](../../skills/plim-design/language.md), "When the fix is words"
- Styles "Keep subscription" to dominate so that cancelling is hard to find. — `plim-design`, "The stance" (Respect the person); Law 5
