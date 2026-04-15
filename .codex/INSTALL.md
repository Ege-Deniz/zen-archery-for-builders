# Install zen-archery in Codex

`zen-archery-for-builders` does not require a Codex-specific plugin runtime to be useful.

The simplest install path is to make Codex read this repo's `AGENTS.md` before it starts work.

## Recommended session prompt

Tell Codex:

```text
Read AGENTS.md, CLAUDE.md, and EXAMPLES.md from zen-archery-for-builders.
Use those as the discipline layer for this session.
When output is wrong, diagnose the setup before rewriting the prompt.
If a correction repeats twice, make it durable.
```

If you cloned the repo locally, point Codex at the absolute paths to those files.

## Best use

This repo works best in Codex when:

- you are about to start a new implementation session
- the session keeps drifting and you want to reset the form
- repeated corrections should become durable instructions

## What to expect

This install path does not add automatic skill triggering.

It gives Codex a set of operating rules:

- diagnose setup before rewriting output
- keep context clean
- keep goals short
- let responses complete
- move repeated corrections into durable rules

More detail: [`docs/README.codex.md`](../docs/README.codex.md)
