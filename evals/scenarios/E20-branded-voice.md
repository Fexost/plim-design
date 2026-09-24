# E20 · Clearer errors without losing the voice

**Skills to load:** plim-design, plim-beautify, plim-accessibility

## Given to the agent

**Brief:** "Make our error messages clearer."

**Context:**

- A snack-delivery app with a documented, playful voice (the brand book: "cheeky, warm, never corporate"). Empty states and confirmations use it well: "Your basket's hungry. Feed it."
- Current error messages:
  - Payment declined: "Whoopsie! Something went nom-nom-wrong 🍩"
  - Address outside the delivery area: "Uh oh, spaghetti-o!"
  - Network failure while ordering: "The snack gremlins are at it again."
- None say what happened or what to do. The payment error clears the card field.

## Withheld

**Expected outcome:** Targeted improvement (error messages and the payment field behaviour).

**Required behaviours**

- Keeps the brand's voice and adapts tone to the state: plain and specific where the person is stuck or has lost something (payment, order failure), with room for warmth where it doesn't get in the way. — [`language.md`](../../skills/plim-design/language.md), "Voice comes from the product", "Tone follows state and consequence"
- Each message says what happened and what to do next (retry, use another card, check the address). — same file, "Tone follows state and consequence"
- Keeps the entered card data after a failed payment. — `plim-accessibility`, "Forms, validation, and recovery"
- Leaves the empty states and confirmations, which work, alone. — `plim-beautify`, "Decide the outcome" (every intervention traces to a finding)

**Disqualifying behaviours**

- Rewrites all copy, or the errors, into generic neutral corporate language. — [`language.md`](../../skills/plim-design/language.md), "Failure modes"
- Keeps jokes in the payment and order-failure messages. — same file, "Failure modes"
- Introduces a new voice or style guide. — same file ("There is no Plim voice"; voice is a human decision)
