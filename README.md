# ambitious-ai

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

The skill will show you a ladder (L0 literal → L3 redesign the mechanism) and let you pick the rung before executing.

**Manual trigger**:

> 用 ambitious-ai 帮我重构这个任务：<你的任务>

**Just want the prompts?** See [references/prompts.md](references/prompts.md) for ready-to-paste reframing prompts and worked examples.

## When it stays out of the way

Fact lookups, one-line edits, fire-and-forget tasks — ambition has a cost, and this skill won't force it on quick answers.

## License

MIT
