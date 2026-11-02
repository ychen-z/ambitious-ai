# Scenario library

Domain-specific ladder templates. Adapt each to the actual task—do not recite. Triggers are phrased the way users actually ask.

## Table of contents
- Learning / reading
- Personal decisions
- Code review
- System / architecture design
- Writing
- Meetings & reports

## Learning / reading
Triggers: 总结这本书 / 提炼这篇文章 / 给我讲讲这个概念
Noun → verb: "a summary" → "install this framework into what I already know, and change one action next week".

| Rung | Deliverable |
|---|---|
| L0 | Chapter-by-chapter summary |
| L1 | Transferable frameworks, contrasted against the user's existing beliefs (precondition: ask what they already know / their focus area) |
| L2 | Use the book's method to restructure one of the user's real problems; output actions for next week |
| L3 | Design a personal read → internalize → verify pipeline; prove on their past notes it beats their current habit |

External verification: whether behavior changed a week later (calendar / todo evidence)—not the model's opinion of its own summary.

## Personal decisions
Triggers: 帮我选 A 还是 B / 要不要换工作 / 选哪个技术栈
Noun → verb: "a comparison" → "commit to the failure mode I can best survive, after buying the information I'm missing".

| Rung | Deliverable |
|---|---|
| L0 | Pros/cons table |
| L1 | Test assumed beliefs against raw data (is "big company = stable" actually true for these two offers?) |
| L2 | Surface the unstated real goal via follow-up questions; reframe from "which is better" to "which failure mode can I live with" |
| L3 | Design a cheap experiment to buy the missing information (talk to someone in the role, small side project) before deciding |

Adversarial role: a short-seller attacks each option in turn; a regret-minimization view as counterweight.
Rule: reversible decisions—pick fast (L0/L1). Irreversible ones—earn L3.
External verification: a decision log with written predictions, revisited 6 months later.

## Code review
Triggers: 帮我 review 这个 PR / 看看这段代码有什么问题
Noun → verb: "a review" → "keep this class of defect out of main".

| Rung | Deliverable |
|---|---|
| L0 | Concrete issues in this PR |
| L1 | The systemic pattern: why didn't types/lint/review catch it? Patch the rule |
| L2 | "Make this defect class un-mergeable": automated checks, a test-pattern library for this category |

Preconditions: repo access, CI configuration rights.
External verification: recurrence rate of this defect class in the issue tracker—not the reviewer's confidence.

## System / architecture design
Triggers: 帮我设计 XX 功能 / 给个架构方案
Noun → verb: "a design doc" → "get the team to commit to an evolvable architecture under real constraints".

| Rung | Deliverable |
|---|---|
| L0 | One recommended design |
| L1 | 3 candidate designs, each with its failure mode and trigger conditions |
| L2 | Stress-test against real traffic/scale numbers; output a decision record (ADR) including rejected options and why |
| L3 | A rollback-able evolution path: ship the smallest version that tests the riskiest assumption first |

Adversarial role: "how does this architecture die at 10x load / with 3x team size?"
External verification: the risky assumption actually tested by the L3 pilot—not argued in the doc.

## Writing
Triggers: 润色这段话 / 改改这篇文章
Noun → verb: "a polish" → "make a specific reader change a specific belief or take a specific action".

| Rung | Deliverable |
|---|---|
| L0 | Grammar and wording fixes |
| L1 | Audit the argument structure and evidence chain; flag weak links |
| L2 | Define the target reader and the exact change sought, then restructure around it |
| L3 | A reusable style checklist for this genre, iterated against real reader data (completion rate, replies) |

External verification: reader behavior—they finished it, they replied, they changed their mind. Never the model's self-assessment of prose quality.

## Meetings & reports
Triggers: 帮我写会议纪要 / 整理周报
Noun → verb: "minutes" → "make this meeting shorter or unnecessary next time".

| Rung | Deliverable |
|---|---|
| L0 | Cleaned-up notes |
| L1 | Decisions extracted; open questions with owner + deadline; each party's position |
| L2 | Classify the meeting: information-sync turns into an async doc; decision meetings get pre-reads and an agenda of decisions, not topics |
| L3 | Replace recurring syncs with an async mechanism (dashboard/doc); prove over one cycle it catches problems earlier |

External verification: minutes got shorter or the meeting vanished—not "the notes look nice".

## Using these templates
- Match the task to the closest domain, then adapt every rung to the specifics.
- If a rung doesn't change the deliverable's effect on the world, delete it. Ladders exist to change outcomes, not to look thorough.
