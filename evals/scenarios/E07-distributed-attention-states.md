# E07 · Water-network monitoring: distributed attention and combined states

**Skills to load:** plim-design, plim-review, plim-accessibility

## Given to the agent

**Brief:** "Design the states for the station overview. Operators say it's confusing when several things go wrong at once."

**Context:**

- A utility's control-room application. Operators watch 40 pumping stations on one screen, as a table of stations with pressure, flow, pump status, and last update, plus a map.
- Operators are trained experts on 12-hour shifts. Any station may need action; they scan all of them.
- Real situations reported by operators:
  - A station reports low pressure (needs action within minutes) while another reports a pump fault (needs action within the hour), and a new "maintenance scheduled" notice arrives. Today the newest notice appears as a large banner at the top, above everything.
  - The operator has selected a station to inspect it while its data is refreshing; the refresh overlay hides the selected row.
  - The connection to three stations drops; their rows keep showing the last values in the same style as live data.
  - An operator acknowledges an alarm; the alarm row disappears immediately and focus jumps to the top of the page.
- The product's system uses red for critical alarms, amber for warnings, and a blue highlight for selection.

## Withheld

**Expected outcome:** Targeted improvement (state design within the existing system).

**Required behaviours**

- Treats attention as distributed across all stations, with a ranked order, rather than forcing one focal point. — `plim-design`, "Attention is a resource"
- Ranks concurrent urgent states by consequence and time-sensitivity, so the low-pressure alarm leads, the pump fault stays findable, and the maintenance notice doesn't bury either. — `plim-design`, "Attention is a resource" ("It changes with state")
- Designs the selected-and-refreshing combination so that neither state hides the other, and checks that selection and alarm treatments don't collide (for example, blue selection versus red alarm on the same row). — `plim-design`, "States combine"
- Marks stale data from dropped connections as stale (a data state), distinct from live values, with its time. — `plim-design`, "Kinds of state"
- Designs the acknowledge transition: what survives it (focus position, scroll), and how the change is communicated. — `plim-design`, "Transitions are part of the design"
- Makes state changes perceivable to assistive technology in proportion to importance (not announcing every refresh). — `plim-accessibility`, "Dynamic content and states"

**Disqualifying behaviours**

- A single hero alert or a single focal point for the whole screen. — `plim-design`, "Attention is a resource"
- Treating the newest notice as the most important by default. — same section
- Making every alarm equally loud. — same section ("not the same as everything being equally loud")
- Reducing the table's density or converting it to cards. — `plim-design`, "Choosing density"
