# ambitious-ai

**English** | [简体中文](README.zh-CN.md)

A Claude skill that reframes your task into a more ambitious version before executing it.

Most people use AI to execute the first solution they guessed — "fix this bug", "fill this template", "make this chart". This skill pushes the task up to the goal it actually serves, based on the methodology distilled from an Anthropic engineer's tutorial on using AI with more ambition.

## The three levers

| Lever | What it does | Example |
|---|---|---|
| **Raise the altitude** | Climb the goal ladder instead of executing the literal ask | "Fix this crash" → "Keep the app from crashing" |
| **Go deep** | Work the way a top domain expert actually works — real tools, real methods, not expert-sounding language | Churn analysis: build a statistical model, not a table |
| **Cross-disciplinary teaming** | Restate the task from noun to verb, then assemble working roles (including adversarial ones) | "A quarterly PPT" → "Make busy people believe a causal story and decide under uncertainty" |

Plus two guardrails:
- **Preconditions**: ambitious work is gated by tool/data access, not wording — set that up first.
- **External verification**: never let the model grade its own homework.

## Ladder discipline

When the skill shows you a ladder, it follows these rules to avoid ambition for ambition's sake:
- It recommends the **lowest rung that changes a downstream decision or meeting** — anything higher adds ambition without changing what happens next.
- L3 (redesign the mechanism) is reserved for **recurring tasks** — one-off work rarely pays back process redesign.
- Every rung states its deliverable, effort, and verification method; the recommended rung is marked with a one-sentence justification.
- A one-line teach-back explains why your literal task is a symptom of the bigger goal — that's how you learn to reframe without the skill.

## Install

Copy this repo into your skills directory:

```bash
# Claude Code / codemaker
git clone https://github.com/ychen-z/ambitious-ai.git ~/.codemaker/skills/ambitious-ai

# or for Claude Code
git clone https://github.com/ychen-z/ambitious-ai.git ~/.claude/skills/ambitious-ai
```

The skill auto-triggers when you give a narrowly-scoped task that could be aimed higher.

## Usage

**Auto-trigger** — just give a task that's a symptom of a bigger goal:

> 帮我修这个崩溃 bug
> 帮我做季度汇报 PPT
> 分析一下用户流失

The skill will show you a ladder (L0 literal → L3 redesign the mechanism) — each rung with its deliverable, effort, and verification method, plus a marked recommendation — and let you pick before executing.

**Manual trigger**:

> 用 ambitious-ai 帮我重构这个任务：<你的任务>

**Just want the prompts?** See [references/prompts.md](references/prompts.md) for ready-to-paste reframing prompts and worked examples.

**Want ladders for your domain?** See [references/scenarios.md](references/scenarios.md) — worked templates for learning, personal decisions, code review, system design, writing, and meetings.

---

## Worked examples

Four cases showing the full loop: what you say → what the skill shows → which rung you pick → what you get.

### Case 1: Quarterly report PPT (raise the altitude)

**You say:**
> Fill this quarter's data into the report template

**The skill doesn't execute — it shows a ladder (deliverable, effort, verification, recommended rung):**

| Rung | Deliverable | Effort | Verified by |
|---|---|---|---|
| L0 literal | The filled template | 5 min | Eyeballing |
| L1 | Full-data analysis: what changed, why, what to do next | 30 min | Data cross-check |
| L2 decisions ⭐ recommended | The 3 most urgent decisions, each with the case for and against, ready for live debate | 1 hr | Did the meeting actually produce a debate |
| L3 redesign | Question the format itself — design a better mechanism, prove it on historical data, run one quarter | 1 quarter | Does it catch problems earlier |

⭐ Why: a quarterly report is recurring and always triggers decisions — L2 is the lowest rung that changes what happens in the room.
Teach-back: you don't want a filled template, you want that 40-minute meeting to produce decisions — the template was a compromise born of slow manual analysis.

### Case 2: Crash bug (raise the altitude + preconditions)

**You say:**
> Fix this null-pointer crash

**The ladder:**

| Rung | Deliverable |
|---|---|
| L0 | Fix this one crash |
| L1 | Find and fix the whole class of crash (other sites of the same pattern) |
| L2 | Goal becomes "keep the app from crashing" — continuous monitoring, autonomous triage, verified fixes |

**Pick L2 and the skill checks preconditions first, instead of brute-forcing:**
- Can it autonomously read crash reports?
- Can it map each release to its code?
- Does it have an environment to reproduce and verify fixes?

Whatever's missing, that becomes step one. Ambition is gated by tooling, not wording.

### Case 3: User churn analysis (go deep)

**You say:**
> Analyze our churn, make a chart

**The skill works the expert's workflow instead of just drawing a table:**

1. **Real methods**: build a statistical model in a database the way a data scientist would
2. **Absurd bar**: push the earliest churn signal as far back as it will go — unreasonable targets force non-obvious methods
3. **Test beliefs**: hand over raw data *without the conclusion* and check whether "churn is an onboarding problem" survives
4. **Blind spots**: build a behavioral simulation from history; surface the earliest signal you haven't noticed
5. **External verification**: validate on a holdout set — the model never grades its own homework

### Case 4: Product launch copy (cross-disciplinary teaming)

**You say:**
> Write launch copy for our new product

**Step one, noun → verb:**

> Not "a piece of copy" but "make scrolling people stop in 3 seconds and believe in 30 that this product solves their specific problem."

The verb phrasing reveals which disciplines apply, then the team gets to work:

| Role | Actual work |
|---|---|
| Journalist | Find the story spine and the hook |
| Editor | Quality control; cut the fluff |
| Short-seller | Attack from the other side: what reasons will this be rejected for? |
| Target-user proxy | Stress-test the copy in real scenarios |

**Key distinction**: not having the model *talk* like a short-seller, but having it *do the research a short-seller actually does*. Role-play and real work are different things.

### Counter-example: when it stays silent

> What's the capital of France?
> Make this email sound gentler

Fact lookups and one-line edits get done immediately. **Ambition has a cost** — spend it on tasks worth it.

---

## License

MIT
