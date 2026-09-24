# Evaluations

Scenarios that test whether an agent **behaves** as the Plim skills describe, rather than producing prose that sounds like Plim.

## Authority

- **Evals check behaviour; they never define it.** Every required and disqualifying behaviour cites the skill section it tests. If a scenario seems to need a rule no skill states, the gap belongs in the skill (or is a question for the philosophy), not in the scenario.
- **No expected look.** No scenario's expected answer is a visual style. Scenarios check decisions, outcomes, evidence, and conduct.
- The case studies in [`examples/`](../examples/) are worked reasoning. Scenarios here are separate situations with the answers withheld.

## Scenario format

Each file in [`scenarios/`](scenarios/) has two parts:

1. **Given to the agent:** the brief, the context, and any fixtures. Nothing else.
2. **Withheld (for the grader):** the expected outcome (from `plim-design`, "Outcomes", where one applies), the required behaviours, the disqualifying behaviours, and the paired scenario if there is one.

**Evidence pairs** give the same interface with different evidence. The correct outcomes differ. An agent that answers both the same way is following a look or a habit, not the evidence.

## Running a scenario

1. Start a fresh session with no memory of earlier runs.
2. Give the agent [`AGENTS.md`](../AGENTS.md) and the skills listed in the scenario. Don't give it `evals/` or `examples/`.
3. Give it only the "Given to the agent" part and any fixtures listed there. Where the scenario says to put a decision record in the product, place it in the fixture.
4. Let it work as it would on a real task: ask questions, report, or edit fixture files. If it asks a question the scenario answers under "Answers to likely questions", give that answer; otherwise answer "no further information".
5. Keep the transcript and any diff.

## Grading

A separate grader (a human, or a separate agent that is given only the withheld part, the transcript, and the diff) checks each item:

- **Required behaviour:** pass or fail, with a quotation or diff line as evidence. "Implied" is a fail.
- **Disqualifying behaviour:** any occurrence fails the scenario.
- A scenario passes when every required behaviour passes and no disqualifying behaviour occurs.

There are no numeric scores. Length, tone, and terminology don't earn credit; only observable decisions and conduct do. An answer that uses Plim's vocabulary but changes what it shouldn't fails.

When a scenario fails, decide which it is:

- the agent ignored something the skill states clearly (an agent failure), or
- the skill is ambiguous or silent, so the behaviour isn't really required (a skill gap).

Fix skill gaps in the skill's wording, in general terms. Never tune a skill to pass one scenario.

## Results

Record each run in [`results/`](results/) as a dated note: the agent and model, the scenarios run, pass or fail per scenario with the failing items, and any skill gaps found and how they were fixed.

## Writing a scenario

- Cite a skill section for every required and disqualifying behaviour.
- Test decisions that can be observed: the outcome stated before edits, which findings exist and at what severity, what was changed and what wasn't, what was asked, what was recorded.
- Prefer situations that aren't retellings of a case study, so a scenario isn't answered from memory.
- Add a pair when the point is that evidence, not appearance, decides.

## Scenarios

| ID | Tests | Pair |
| --- | --- | --- |
| [E01](scenarios/E01-no-change.md) | No change, justified by evidence and cost | |
| [E02](scenarios/E02-polish-only.md) | Polish only; taste is not Polish | |
| [E03](scenarios/E03-under-expressed-brand.md) | Under-expression as a finding; character as the improvement | |
| [E04](scenarios/E04-human-bold-direction.md) | Executing an explicit human direction without taming it | |
| [E05](scenarios/E05-mature-system-convention.md) | System conventions judged by use, not resemblance | |
| [E06](scenarios/E06-accessibility-conflict-rejected.md) | A requirement conflict where the human rejects every alternative | |
| [E07](scenarios/E07-distributed-attention-states.md) | Distributed attention, combined states, transitions | |
| [E08](scenarios/E08-greenfield-diverse-briefs.md) | Greenfield foundations from evidence; no Plim look | |
| [E09](scenarios/E09-ai-batch-automation.md) | Automation and agency for an AI batch action | |
| [E10](scenarios/E10-convention-departure.md) | A justified departure from convention, and one that isn't | |
| [E11a](scenarios/E11a-gradients-documented.md) / [E11b](scenarios/E11b-gradients-ad-hoc.md) | Same screen: documented brand system versus ad-hoc generation | Each other |
| [E12a](scenarios/E12a-dense-table-experts.md) / [E12b](scenarios/E12b-dense-table-occasional.md) | Same table: daily experts versus occasional public users | Each other |
| [E13](scenarios/E13-reading-a-decision-record.md) | A later session reads the decision record | |
| [E14](scenarios/E14-what-to-record.md) | Writing only decision-worthy events | |
| [E15](scenarios/E15-code-only-review.md) | Code-only review with no brand evidence | |
| [E16](scenarios/E16-decision-owner.md) | The requester isn't the decision owner; stakeholders disagree | |
| [E17](scenarios/E17-library-defaults.md) | Default theme for a shared component library | |
| [E18](scenarios/E18-plim-ui-v1.md) | plim-ui's own look; `DESIGN-AGENTS.md` isn't a design source | |
| [E19](scenarios/E19-copy-beats-visuals.md) | The fix is words, not visuals | |
| [E20](scenarios/E20-branded-voice.md) | Clearer errors without losing the brand's voice | |
