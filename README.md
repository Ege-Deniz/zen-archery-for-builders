# zen-archery-for-builders

> You keep making the same corrections every session. This file helps you stop.

`Zen in the Art of Archery` (Eugen Herrigel, 1948), reframed as a workflow discipline for AI-assisted building.

I grew up as a competitive archer before I wrote code.

In kyudo there is a saying: **it shoots**. Not *I shoot*. When the archer's form is right, the arrow releases itself. The archer's job is not to force the shot. It is to establish the conditions and get out of the way.

That maps surprisingly well to AI-assisted work. A lot of wasted time does not come from weak models. It comes from bad setup: stale context, panicked mid-stream corrections, prompts bloated with five layers of patchwork instructions, and repeated fixes that never become durable rules.

This repo turns that discipline into a reusable `CLAUDE.md`, a Claude plugin, and a set of agent-facing instructions.

## What this is

A workflow discipline layer for builders who:

- repeat the same corrections across sessions
- keep poisoning clean tasks with dirty context
- over-specify prompts until outputs get brittle
- want a calmer, cleaner way to work without pretending every workflow should be minimal

## What this is not

- a universal performance booster
- a guarantee of lower token cost
- a replacement for project-specific rules
- a reason to remove necessary constraints from precision-heavy workflows

If your team already has a strong ruleset, compliance gates, or highly specific formatting constraints, you may need more structure than "light grip" suggests. The wrong use of this repo is stripping away necessary instructions and calling it simplicity.

## Who should use it

Use it if your main problem is workflow quality:

- too many corrective follow-ups
- too much stale context
- long prompts that still miss the point
- repeated mistakes that should have become durable rules

Do not use it because the story sounds good. Use it if the pattern matches your real friction.

## Who should not

This repo may be a poor fit when:

- the task is precision-heavy and every constraint really does need to be explicit
- your team already has a very strong project-specific ruleset
- the metaphor encourages people to remove necessary instructions
- you want a benchmarked optimization tool rather than a workflow discipline

## The ten principles

1. **It shoots, I do not shoot** — set the shot up, then step out of it.
2. **Aim is a beginner's strategy** — the prompt is the stance, not the aim.
3. **The target teaches, not the archer** — fix form, not outputs.
4. **Right breath before right shot** — garbage context, garbage output.
5. **The bowstring cuts those who grip too hard** — over-specified prompts collapse the range.
6. **The pause at full draw** — let the response finish.
7. **A thousand identical shots** — form emerges from practice, not theory.
8. **Non-attachment to the hit** — iteration is the mechanism.
9. **Beginner's mind, every shot** — shoshin. Start each session clean.
10. **The master shoots in the dark** — trust the scaffolding you built.

Each principle comes with a concrete rule and an "in practice" checklist in [`CLAUDE.md`](./CLAUDE.md). Practical before/after setups live in [`EXAMPLES.md`](./EXAMPLES.md).

## How to know it's working

These principles are working if you notice:

- **fewer corrective follow-ups** — you stop saying "no, not like that" and start fixing the setup instead
- **shorter prompts with the same or better outcomes** — constraints move into `CLAUDE.md`, not into every message
- **proactive session restarts** — you restart when context is dirty, instead of layering corrections
- **repeated corrections becoming durable rules** — frictions you hit twice get codified, not re-typed
- **calmer sessions** — less gripping, less interrupting, less arguing with outputs

If none of these happen after a week of real use, the repo is not helping your workflow. Narrow it or stop using it.

## What is actually backed up

The strongest backing is not the metaphor. It is Claude's own documentation:

- Claude Code supports durable project and user memory through `CLAUDE.md`, which is exactly where repeated corrections should move: [Manage Claude's memory](https://code.claude.com/docs/en/memory)
- Anthropic recommends clear structure, examples, and explicit organization for better prompt reliability: [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices#structure-prompts-with-xml-tags)
- Anthropic's Claude Code docs say token costs scale with context size, stale context wastes tokens, and better structure can reduce unnecessary exploration: [Manage costs effectively](https://code.claude.com/docs/en/costs)
- Anthropic also warns that more prompt complexity can degrade performance, especially in cost-sensitive cases: [Reduce prompt leak](https://platform.claude.com/docs/en/test-and-evaluate/strengthen-guardrails/reduce-prompt-leak), [Prompting tools](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/prompting-tools)

So the honest position is:

- reusable structured instructions are backed up
- cleaner context management is backed up
- examples and durable rules are backed up
- this specific kyudo framing is a memorable wrapper, not a proven scientific result

## How to evaluate it

Do not trust the story alone. Run it against real work.

- evaluation guide: [`EVALUATION.md`](./EVALUATION.md)
- initial author-side pilot rows are included there; proper baseline-vs-zen comparisons are still pending
- use 5 to 20 real tasks, not toy prompts
- compare baseline vs zen-archery
- track turns, corrections, and whether the result was acceptable

If it does not reduce wasted corrections, does not improve setup discipline, or actively hurts precision in your workflow, narrow the file or stop using it.

## Install as `CLAUDE.md`

```bash
# Project-level — applies only to the current repo
curl -o CLAUDE.md https://raw.githubusercontent.com/Ege-Deniz/zen-archery-for-builders/main/CLAUDE.md

# Or global — applies to every Claude Code session
curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/Ege-Deniz/zen-archery-for-builders/main/CLAUDE.md
```

## Use as a Claude plugin

This repo also includes a Claude plugin package:

- manifest: [`.claude-plugin/plugin.json`](./.claude-plugin/plugin.json)
- skill: [`skills/principles/SKILL.md`](./skills/principles/SKILL.md)

For local testing:

```bash
claude --plugin-dir /path/to/zen-archery-for-builders
```

Then invoke:

```text
/zen-archery:principles
```

## Use with Codex and other agents

This repo is not Claude-only in structure.

- runtime-facing instructions: [`AGENTS.md`](./AGENTS.md)
- Codex install note: [`.codex/INSTALL.md`](./.codex/INSTALL.md)
- Codex usage guide: [`docs/README.codex.md`](./docs/README.codex.md)

## Why a book

Most dev best-practices resources age into committee language. The principles in this book survived because they are not really about archery. They are about the mechanics of doing anything under pressure.

Claude Code is pressure. The cost of a bad prompt is tokens, but the deeper cost is drift: gripping the tool, forcing outputs, and losing form. A `CLAUDE.md` cannot fix that by itself. It can remind you what good form looks like.

## About the book

*Zen in der Kunst des Bogenschiessens*, Eugen Herrigel, 1948. English translation by R. F. C. Hull, 1953, with a foreword by D. T. Suzuki. Herrigel was a German philosopher who spent six years in Japan in the 1920s and 30s studying kyudo under Kenzo Awa.

It has also been contested. Shoji Yamada's *Shots in the Dark: Japan, Zen, and the West* (2009) argues that Herrigel projected a Zen framing onto a practice that was not traditionally considered Zen in Japan. You should read Yamada if you want the full picture. The principles in this repo do not depend on Herrigel being historically perfect; they depend on whether the mechanics help your workflow.

## Contributing

Issues and PRs welcome. If a principle helps, say where. If it hurts, say where. If the metaphor breaks under real use, that is exactly the kind of feedback this repo should absorb.

## License

MIT — see [LICENSE](./LICENSE).

## Author

[@Ege-Deniz](https://github.com/Ege-Deniz) · [rowy.engineer](https://rowy.engineer)

Competitive archer from Northern Cyprus. Now a builder. Written with Claude Code.

Sister repo: [`Ege-Deniz/three-skills-for-claude`](https://github.com/Ege-Deniz/three-skills-for-claude).
