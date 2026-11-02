# Reusable prompts and worked examples

## Table of contents
- Prompt: Go deep (expert reframing)
- Prompt: Raise the altitude
- Prompt: Cross-disciplinary teaming
- Worked ladder: Quarterly report
- Worked ladder: Software stability
- Worked ladder: User churn

## Prompt: Go deep (expert reframing)
Paste before a task when you want expert-grade work:

> Before you rewrite my task, tell me:
> 1. How would the top expert in this field actually approach it?
> 2. What raw materials/source data would they start from?
> 3. What tools and methods would they use (the real ones, not expert-sounding language)?
> 4. Besides you and me, what external tool or method could judge whether the result is correct?
> Then rewrite my task to meet those standards, and execute it.

## Prompt: Raise the altitude
> Here is the task I asked for: [TASK].
> Don't do it yet. First climb the goal ladder: what outcome does this task actually serve, one level up, two levels up, and at the highest level where the format/process itself could be redesigned?
> Give me the ladder (L0 literal → L3 redesign the mechanism) with the concrete deliverable at each rung, then ask me which rung to execute.

## Prompt: Cross-disciplinary teaming
> Restate this task from a noun ("a [X]") into a verb describing the real job to be done.
> Then list the working roles (not personas) whose actual methods this task needs, including at least one adversarial role that attacks the result from the opposite side.
> For each role, describe the concrete work they would do here—not how they would talk. Then do that work.

## Worked ladder: Quarterly report
- L0: Fill data into the slide template.
- L1: From all available data, explain what changed, why, and the recommended next actions.
- L2: Identify the 3 most urgent decisions; for each, list the case for and against; prepare them for live debate.
- L3: Challenge the report format itself—design a replacement mechanism, validate it on historical data to show it catches problems earlier, and pilot it for one quarter.

## Worked ladder: Software stability
- L0: Fix this specific crash.
- L1: Fix this class of crash across the codebase.
- L2: "Keep our app from crashing"—with access to crash reports, version-to-code mapping, and a machine to reproduce and verify fixes autonomously.
Precondition: AI needs crash-report access, source mapping per release, and an environment to reproduce and validate.

## Worked ladder: User churn
- L0: Make a churn chart.
- L1 (go deep): Build a statistical model in a database the way a data scientist would; don't just tabulate.
- L2 (test beliefs): Hand over raw data; check whether the assumed cause ("onboarding problem") actually holds, without being told the answer.
- L3 (blind spots): Build a behavioral simulation from historical data and surface the earliest predictive signal of churn.
- Verify: use an external method/holdout to validate, not the model's self-assessment.
