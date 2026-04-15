# Evaluate zen-archery-for-builders

This repo should be judged by outcomes, not by how elegant the metaphor sounds.

## Status

This evaluation framework has not yet been run against a real task set. The scorecard below is a template, not evidence. If you run it, please open an issue or PR with your results — positive, negative, or mixed.

The repo's claims are structured as testable hypotheses, not proven facts. This section exists so you can test them.

Initial rows below are preliminary author-side pilot observations from real work on this repo. They are useful as a starting point, but they are not controlled baseline-vs-zen comparisons yet.

## What to measure

For each task, record:

- task name and brief description
- runtime and model (e.g. Claude Code + Sonnet 4)
- mode: baseline or zen-archery
- total turns to acceptable output
- number of corrective follow-up prompts
- whether the result was acceptable (yes / no / partial)
- whether a repeated correction became a durable rule (yes / no / n/a)
- notes on what actually helped or hurt

Token counts and session cost are useful if available, but do not fake precision. If your runtime does not report tokens, skip that column and focus on turn count and correction count.

## Recommended task set

Use 5 to 20 real tasks, not toy prompts.

Good candidates:

- code change in an existing repo
- debugging a failing function
- writing a small README section
- refactoring one file with clear constraints
- navigating an unfamiliar codebase
- turning repeated corrections into durable instructions

Avoid:

- one-shot novelty prompts
- tasks with no clear acceptance criteria
- comparing across different models or different context windows

## Suggested procedure

1. Pick a real task.
2. Run it once with your normal workflow (baseline).
3. Run a comparable task with the zen-archery `CLAUDE.md` loaded and the principles applied.
4. Keep the model, repo, and difficulty as similar as possible.
5. Fill in the scorecard.
6. After 5+ tasks, look for patterns.

## Initial pilot rows

| Task | Mode | Runtime / model | Turns | Corrections | Durable rule created | Acceptable | Notes |
|------|------|-----------------|-------|-------------|---------------------|------------|-------|
| tighten README claims and add observable signals | zen-archery (pilot) | Codex GPT-5.4 + manual review | 1 | 0 | yes: README and evaluation language narrowed | yes | stronger promise, less overclaiming, added "How to know it's working" |
| separate AGENTS.md from CLAUDE.md and make the skill operational | zen-archery (pilot) | External review + Codex follow-up | 1 | 1 | yes: agent/runtime guidance became operational instead of duplicative | yes | file roles became clearer, repo felt less like the same idea repeated |
| validate plugin package and fix skill frontmatter parsing | zen-archery (pilot) | Claude CLI validate + Codex GPT-5.4 | 1 | 0 | yes: quoted skill description, validation now passes | yes | found a real packaging bug that prose review alone did not catch |
| draft LinkedIn launch post for zen-archery-for-builders | zen-archery (pilot) | Claude Code + Sonnet 4.6 | 1 | 0 | yes: load skill context before writing became a durable rule in the brain's execution layer | yes | loaded article-writing playbook before drafting; clean scoped brief; complete post in one pass with zero correction loop |
| 6-file brain infrastructure upgrade across multiple interdependent skill files and wiki pages | zen-archery (pilot) | Claude Code + Sonnet 4.6 | 7 | 0 | yes: Gate Clearance protocol documented as mandatory pre-write sub-step | yes | multi-file refactor with zero mid-session corrections; reading files before editing and stating intent per file prevented drift across all 7 operations |

## Blank scorecard template

Use this table for proper baseline-vs-zen comparisons on future tasks:

| Task | Mode | Runtime / model | Turns | Corrections | Durable rule created | Acceptable | Notes |
|------|------|-----------------|-------|-------------|---------------------|------------|-------|
|  | baseline |  |  |  |  |  |  |
|  | zen-archery |  |  |  |  |  |  |

## What would count as a real win

zen-archery is worth keeping if, across a batch of real tasks, it tends to produce one or more of:

- fewer corrective turns (the clearest signal)
- repeated corrections moving into durable rules instead of being re-typed
- proactive session restarts instead of correction spirals
- shorter prompts with the same or better outcomes
- calmer, less adversarial sessions

## What would count as failure

Drop or narrow the repo's claims if it consistently causes:

- missing necessary constraints because "light grip" was taken too far
- worse quality on precision-heavy tasks
- more follow-up correction rounds, not fewer
- longer prompts with no quality improvement
- slower workflows that only feel nicer but do not produce better results

## The narrow claim

The strongest defensible claim is not "this makes Claude better."

It is:

**"This may help builders who overcorrect, overload context, or repeat the same fixes every session."**

If your evaluation shows it does not help with that specific pattern, this repo is not for your workflow.
