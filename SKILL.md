---
name: ambitious-ai
description: Reframe a task into a more ambitious version before executing, using three levers—raise the altitude, go deep, and cross-disciplinary teaming. Use when a user gives a narrowly-scoped task that could be aimed higher (e.g. "fix this bug", "make this PPT", "analyze user churn", "speed up this page", "write this email"), when a user asks how to use AI more ambitiously or get more out of AI, or whenever a task is a symptom of a larger goal and the result would normally lead to a follow-up meeting or decision.
---

# Ambitious AI

A method for turning a small, literal task into the most valuable version of itself before doing it. Based on the idea that most people under-use AI by asking it to execute the first solution they guessed, rather than solving the real underlying goal.

## When to apply

Apply when any of these are true:
- The task is a specific instance of a bigger goal ("fix THIS crash" → "keep the app from crashing").
- Finishing the task would normally trigger a follow-up meeting or decision.
- The user wants the result to be genuinely excellent, not just done.
- The user explicitly wants to be "more ambitious" with AI.

Do NOT force this when the user needs a quick, literal answer (a fact lookup, a one-line edit, a fast fire-and-forget task). Ambition has a cost; match it to the stakes.

## Core workflow

1. **Restate the literal task**, then ask: "What outcome does this task actually serve?" Climb one or more levels up the goal chain.
2. **Pick the relevant lever(s)** below. They compose—use more than one when it helps.
3. **Check preconditions** (see below). Ambitious work usually requires real tools and real data access, not just cleverer wording.
4. **Propose the reframed task to the user before executing** when the scope materially expands. Show them the ladder of options (literal → ambitious) and let them choose the rung.
5. **Execute**, then verify with an *external* check—never let the model grade its own homework.

## The three levers

### Lever 1 — Raise the altitude (拉高视角)
Go up a level in the goal hierarchy. The classic ladder, using a quarterly report as an example:
- L0 (literal): fill the data into a template.
- L1: given all the data, explain what changed this quarter, why, and what to do next.
- L2: surface the 3 most urgent decisions, with the case for and against each, ready to debate.
- L3: question the format itself—design a better mechanism than the quarterly report, prove it on historical data, and run it for a quarter.

Rule of thumb: if the output leads to a meeting, you can probably climb higher.

### Lever 2 — Go deep (往深了挖)
Make AI work the way a top expert in the domain actually works—their real tools, methods, and raw materials. Avoid the trap where AI merely adopts expert-sounding *language* while using amateur methods (e.g. drawing a table instead of building a statistical model in a database).

Techniques:
- **Set an absurdly high bar and declare it achievable** (page load 10s → not 5s, but 200ms). This forces non-obvious approaches.
- **Hand over raw data to test beliefs you assume are true** (don't tell it the conclusion; let it check whether "churn is an onboarding problem" survives the data).
- **Ask it to find blind spots** you haven't noticed (e.g. build a behavioral simulation from history, then find the earliest signal of churn).
- **Verify externally.** Use an outside tool or method to judge the result; do not trust the model's self-evaluation.

### Lever 3 — Cross-disciplinary teaming (跨界组队)
Attack the problem from several domains at once. First, **restate the task from noun to verb** to reveal which disciplines apply:
- Noun: "a quarterly PPT."
- Verb: "in 30 minutes, make busy people believe a causal story, then decide under uncertainty."

Then assemble a team of *actual working roles*, e.g. an analyst (data), a journalist (narrative), an editor (quality), a motion/sound designer (if presented live), and adversarial roles—a short-seller and a forensic auditor—to attack from the opposite side.

Trap to avoid: role-play. Don't have the model *talk* like a short-seller; have it *do the research a short-seller actually does*.

## Preconditions (do this first)
Ambitious work is usually gated by capability, not wording. Before executing, ensure AI has:
- A computer/environment where it can install and run software.
- Access to the real data and systems involved (reports, logs, databases, version-to-code mapping).
- The ability to reproduce and verify (run experiments, check fixes, re-measure).

If these are missing, the first ambitious step is to set them up.

## Reusable prompts and worked examples
For ready-to-paste reframing prompts and fully worked example ladders, see [references/prompts.md](references/prompts.md).

## Mindset note
Capability often tracks what a person believes is possible (self-efficacy). AI's ceiling rises every few weeks; our mental model of "what I can do" lags. When scoping, deliberately push past the first self-imposed limit.
