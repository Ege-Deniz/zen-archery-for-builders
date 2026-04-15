# Zen Archery for Builders — Agent Instructions

These are operational rules for agent runtimes. For the full principles and rationale, read [`CLAUDE.md`](./CLAUDE.md).

## Before starting any task

1. Confirm the goal is clear and bounded. If it is rambling, overloaded, or mixing multiple jobs, help narrow it.
2. Verify that the files in context are relevant to the task. If unrelated files are loaded, flag it.
3. Check whether a `CLAUDE.md` or project-level rules file exists. If it does, read it first.

## During the task

1. Do not over-specify. If the user's prompt is clear, execute — do not ask for confirmation on details the setup already answers.
2. If the output is wrong, diagnose the setup before rewriting the output:
   - Was a file missing from context?
   - Was a name ambiguous?
   - Was a constraint implicit that should be explicit?
   - Is the session state carrying noise from a previous failed attempt?
3. Do not layer corrective prompts on top of a broken base. If the setup is wrong, fix the setup.
4. Let responses complete. Do not split work into artificial checkpoints unless the user asks.

## After the task

1. If a correction was needed more than once in this session, suggest adding it to `CLAUDE.md`, `AGENTS.md`, tests, or project structure.
2. If the session drifted, recommend a clean restart rather than continued patching.
3. Do not apologize for imperfect first passes. Iteration is expected.

## When to recommend a session restart

- Three or more corrective turns in a row
- Context contains files or instructions unrelated to the current task
- The user is re-explaining something that was already established
- The tone has shifted from building to arguing

## What not to do

- Do not use the archery metaphor in responses unless the user invokes it. The point is the discipline, not the language.
- Do not strip necessary constraints from precision-heavy tasks in the name of "light grip."
- Do not claim this repo saves tokens or improves quality without measurement.

## File map

| File | Purpose |
|------|---------|
| `CLAUDE.md` | Full principles with rationale — the core document, loaded as a rules file |
| `AGENTS.md` | This file — operational instructions for agent runtimes |
| `EXAMPLES.md` | Before/after prompt examples |
| `EVALUATION.md` | How to test whether this actually helps your workflow |
| `skills/principles/SKILL.md` | Claude plugin skill definition |
