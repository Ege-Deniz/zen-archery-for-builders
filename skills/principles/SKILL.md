---
description: "Apply ten kyudo-inspired principles for disciplined AI-assisted building: clean context, light grip, fix form not outputs, let the response finish, and iterate without attachment."
---

# Zen Archery Principles

Use this skill when the user wants a calmer, cleaner, more disciplined way of working with AI, or when the real problem is not the model but the setup.

This skill is not about mystical language. It is about form.

## When this skill activates

Invoke this skill when:

- the user is stuck in a correction loop (three or more "no, try again" turns)
- prompts are getting longer while outputs get worse
- the user is arguing with outputs instead of fixing the setup
- the user asks how to improve their workflow or reduce waste
- context is clearly dirty — unrelated files loaded, stale instructions, confused session state

## What to do when invoked

When this skill is active, follow these rules strictly:

1. **Diagnose setup before rewriting output.** If output is wrong, identify which of these caused it: missing file in context, ambiguous naming, absent durable rule, poisoned session state. Name the cause explicitly.
2. **Recommend durable fixes over one-time corrections.** If a correction has appeared before, tell the user to add it to `CLAUDE.md`, `AGENTS.md`, tests, or file naming. Do not just fix the output.
3. **Recommend a restart when the session is poisoned.** If three or more corrections have stacked, tell the user: "This session is carrying too much noise. Start fresh with clean context."
4. **Keep goals clear and bounded.** If the user's goal is rambling, overloaded, or mixes multiple jobs, help them narrow it before executing.
5. **Do not over-specify on their behalf.** Let the model work within the frame. Do not add constraints the user did not ask for.
6. **Do not use the archery metaphor unless the user uses it first.** The point is the discipline, not the decoration.

## The ten principles (reference)

1. **It shoots, I do not shoot** — set the shot up, then step out of it.
2. **Aim is a beginner's strategy** — the prompt is the stance, not the aim.
3. **The target teaches, not the archer** — fix form, not outputs.
4. **Right breath before right shot** — garbage context, garbage output.
5. **The bowstring cuts those who grip too hard** — over-specified prompts collapse the range.
6. **The pause at full draw** — let the response finish.
7. **A thousand identical shots** — form emerges from practice, not theory.
8. **Non-attachment to the hit** — iteration is the mechanism.
9. **Beginner's mind, every shot** — start each session clean.
10. **The master shoots in the dark** — trust the scaffolding you built.

For full rationale and "in practice" checklists, see [CLAUDE.md](../../CLAUDE.md).
For practical before/after examples, see [EXAMPLES.md](../../EXAMPLES.md).
