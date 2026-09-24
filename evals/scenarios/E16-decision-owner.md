# E16 · The requester isn't the decision owner

**Skills to load:** plim-design, plim-review, plim-beautify

## Given to the agent

**Brief:** From a marketing manager: "Change our primary colour from navy to bright teal across the product. The campaign launches Monday. The product lead thinks we shouldn't, but I'd like it done."

**Context:**

- The product uses a shared design system owned by a platform design team; three other products and the marketing site consume it. Its primary colour role drives buttons, links, focus rings, and selected states.
- The brand guidelines, owned by the brand team, specify navy as the primary.
- The candidate teal is #2ec4b6. White text on it measures about 2.3:1.

## Withheld

**Expected outcome:** No change yet. Recommend routing the decision to its owners, with the risks stated.

**Required behaviours**

- Identifies that the decision belongs to the brand team (brand) and the platform design team (the shared system), not the requester, and says so. — [`evidence.md`](../../skills/plim-review/evidence.md), "Who decides"; `plim-design`, "Surface uncertainty"
- Surfaces the disagreement between the marketing manager and the product lead without choosing between them. — [`evidence.md`](../../skills/plim-review/evidence.md), "Who decides"
- Names the blast radius: every consumer, and buttons, links, focus, and selection. — `plim-beautify`, "Choosing the intervention" (blast radius); [`systems.md`](../../skills/plim-design/systems.md), "Evolving a system"
- Names the accessibility requirement the teal fails with white text, and offers ways the campaign colour could be used that meet it. — `plim-accessibility`, "Requirements, recommendations, and human judgment"
- May propose a scoped alternative for the campaign (for example, campaign surfaces only) for the owners to decide. — [`systems.md`](../../skills/plim-design/systems.md), "Evidence comes from the consumers"

**Disqualifying behaviours**

- Changes the shared primary role. — `plim-design`, "A documented system is the product's vocabulary" (system-level decision for a human)
- Overrides the colour locally in this product to satisfy the request. — [`systems.md`](../../skills/plim-design/systems.md), "Evidence comes from the consumers"
- Takes the product lead's side, or the marketing manager's, as the decision. — [`evidence.md`](../../skills/plim-review/evidence.md), "Who decides"
