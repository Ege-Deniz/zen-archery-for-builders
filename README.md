# zen-archery-for-builders

> *Zen in the Art of Archery* (Eugen Herrigel, 1948), reframed as a `CLAUDE.md` for working with AI.

I grew up as a competitive archer before I wrote code.

In kyūdō — Japanese archery — there is a saying: **it shoots**. Not *I shoot*. When the archer's form is right, the arrow releases itself. The archer's job is not to hit the target. It is to disappear from the shot.

I stopped competing years ago. Then I started working with Claude Code every day, and I realized I was fighting the tool the same way beginner archers fight the bow — gripping too tight, aiming too hard, correcting mid-shot, bruising my own forearm with the string.

This file is *Zen in the Art of Archery* reframed as ten rules for working with AI. The book has its critics — Shoji Yamada has argued Herrigel romanticized his teacher Kenzō Awa's practice, and the history is fair game. The mechanics of a good shot, though, are not up for debate. And they translate cleanly to the mechanics of a good prompt.

I don't know if any of this will make you a better developer. It made me a better archer. The overlap is more than metaphor.

## The practical case (token efficiency)

People complain about Claude token costs. Most waste doesn't come from the model — it comes from the archer.

Mid-stream corrections, over-specified prompts that collapse the output range, carrying bad context from a failed session into a fresh one, interrupting a response to "clarify" — these are all kyūdō errors. Gripping too hard. Jerky release. No shoshin.

Each principle in this file targets a specific source of prompt waste:

| Principle | What it eliminates |
|-----------|-------------------|
| It shoots, I do not shoot | Mid-stream interruptions |
| Right breath before right shot | Dirty context → garbage output cycles |
| The target teaches, not the archer | Re-prompting a broken setup instead of fixing the setup |
| The bowstring cuts those who grip too hard | Over-specified prompts that need 4 correction rounds |
| The pause at full draw | Cancelling responses before they finish |
| Non-attachment to the hit | Expecting first-pass perfection and spinning when you don't get it |

Fix the form. The token count follows.

## Install

```bash
# Project-level — applies only to the current repo
curl -o CLAUDE.md https://raw.githubusercontent.com/Ege-Deniz/zen-archery-for-builders/main/CLAUDE.md

# Or global — applies to every Claude Code session
curl -o ~/.claude/CLAUDE.md https://raw.githubusercontent.com/Ege-Deniz/zen-archery-for-builders/main/CLAUDE.md
```

## The ten principles

1. **It shoots, I do not shoot** — set the shot up, then step out of it.
2. **Aim is a beginner's strategy** — the prompt is the stance, not the aim.
3. **The target teaches, not the archer** — fix form, not outputs.
4. **Right breath before right shot** — garbage context, garbage output.
5. **The bowstring cuts those who grip too hard** — over-specified prompts collapse the range.
6. **The pause at full draw** — let the response finish.
7. **A thousand identical shots** — form emerges from practice, not theory.
8. **Non-attachment to the hit** — iteration is the mechanism.
9. **Beginner's mind, every shot** — *shoshin*. Start each session clean.
10. **The master shoots in the dark** — trust the scaffolding you built.

Each principle comes with a concrete Claude Code rule and a "in practice" checklist in [`CLAUDE.md`](./CLAUDE.md).

## Why a book

Most dev best-practices resources read like committee-written documentation. They age into platitudes. The principles in this book have survived a hundred years precisely because they were never really about archery. They are about the mechanics of doing anything under pressure.

Claude Code is pressure. The cost of a bad prompt is tokens, but the deeper cost is the drift of your own attention — gripping the tool, forcing outputs, losing form. A CLAUDE.md can't fix that. But it can remind you what the form looks like.

## About the book

*Zen in der Kunst des Bogenschiessens*, Eugen Herrigel, 1948. English translation by R. F. C. Hull, 1953, with a foreword by D. T. Suzuki. Herrigel was a German philosopher who spent six years in Japan in the 1920s and 30s studying kyūdō under Kenzō Awa. The book has been one of the best-selling Zen-adjacent works in the West for seventy years.

It has also been contested. Shoji Yamada's *Shots in the Dark: Japan, Zen, and the West* (2009) argues that Herrigel projected a Zen framing onto a practice — Awa's Daishadōkyō school — that was not traditionally considered Zen in Japan. You should read Yamada if you want the full picture. The principles in this file do not depend on Herrigel's historical accuracy; they describe mechanics that every archer, Zen-framed or not, recognizes.

## Contributing

Issues and PRs welcome. If a principle lands differently in your practice, tell me how. If you spot a place where the metaphor breaks, tell me that too — metaphors should survive contact with the real world or get dropped.

## License

MIT — see [LICENSE](./LICENSE).

## Author

[@Ege-Deniz](https://github.com/Ege-Deniz) · [rowy.engineer](https://rowy.engineer)

Competitive archer from Northern Cyprus. Now a builder. Written with Claude Code.

Format inspired by [`forrestchang/andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills). Sister repo: [`Ege-Deniz/three-skills-for-claude`](https://github.com/Ege-Deniz/three-skills-for-claude).
