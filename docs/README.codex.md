# Zen Archery for Codex

This repo is usable in Codex even without a dedicated Codex plugin package.

The core idea is simple: use `AGENTS.md` as the runtime-facing rules file, keep `CLAUDE.md` as the richer source text, and use `EXAMPLES.md` for concrete setup corrections.

## Why this works

Codex can read local instruction files directly. That is enough for a repo like this because the value is in the operating discipline, not in a tool API.

## File roles

| File | What Codex should use it for |
|------|------------------------------|
| `AGENTS.md` | Operational rules — what to do before, during, and after a task |
| `CLAUDE.md` | Full principles with rationale — read once for context |
| `EXAMPLES.md` | Before/after prompt examples — reference when correcting |

## Best prompt

```text
Read AGENTS.md, CLAUDE.md, and EXAMPLES.md from zen-archery-for-builders.
Use them as the workflow discipline for this session.
When output is wrong, improve the setup before rewriting the prompt.
If a correction repeats twice, make it durable.
```

## What this repo is not

- not a framework
- not a replacement for project-specific rules
- not a promise that one prompt will fix everything

It is a set of operating rules that reduce waste by improving how sessions are set up.
