# Improvement and Testing List

Use this after the initial push. Do not treat all of it as day-one work.

## Immediate testing

- run `claude plugins validate .` from the repo root after every packaging change
- test `claude --plugin-dir /path/to/zen-archery-for-builders`
- confirm `/zen-archery:principles` appears and invokes correctly
- test one Codex session using `AGENTS.md`, `CLAUDE.md`, and `EXAMPLES.md`
- check that the install instructions work exactly as written

## Evaluation work

- add 2 more real rows to `EVALUATION.md` from actual usage after push
- run the first proper baseline-vs-zen comparison on a real repo task
- log whether fewer corrective follow-ups actually happen
- log whether repeated fixes become durable rules faster
- add one real case study to `EXAMPLES.md` once a strong example exists

## Product improvements

- sharpen the README only if public feedback shows confusion
- keep claims narrow unless evidence gets stronger
- test whether the plugin package should stay minimal or gain one more practical skill
- make `AGENTS.md` even more runtime-specific if Codex usage reveals gaps
- decide later whether `three-skills-for-claude` should match this exact family structure

## Distribution improvements

- collect the first public reactions before changing the core positioning
- note which line hooks better:
  - "You keep making the same corrections every session. This file helps you stop."
  - "Cleaner sessions, less drift, fewer avoidable corrections."
- if people understand the story but not the utility, add one stronger real-world case study
- if people like the utility but ignore the story, tighten the opening further

## Things not to do

- do not broaden the claims before real usage data exists
- do not add files just to make the repo feel bigger
- do not turn the repo into generic AI productivity language
- do not remove the personal archery angle; it is part of the reason the repo is memorable
