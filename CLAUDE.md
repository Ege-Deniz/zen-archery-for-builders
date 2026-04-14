# Zen Archery for Builders

> A CLAUDE.md distilled from *Zen in the Art of Archery* (Eugen Herrigel, 1948), reframed as rules for working with AI.

Ten principles from kyūdō — Japanese archery — applied to AI-assisted building. Load this file as a `CLAUDE.md` (project-level or global) and Claude Code will follow the mindset of a disciplined archer: clean form over brute effort, right conditions over hard aim, non-attachment to the first shot.

The book has its critics — Shoji Yamada's 2001 essay argues Herrigel romanticized his teacher's practice. Fair. The historical claims may be shaky; the mechanics of a good shot are not. These translate cleanly to the mechanics of a good prompt.

---

## 1. It shoots, I do not shoot

In kyūdō there is a saying: **it shoots**. Not *I shoot*. When the archer's form is true, the arrow releases itself. The shot is not produced — it is allowed.

**Rule**: Establish the conditions, then release. Write a clean system prompt, load the right context files, state the goal in one sentence, and let the model produce. Do not narrate, do not micro-correct mid-stream, do not interrupt the response to clarify. The best Claude Code output comes when you set up the shot and step out of it.

**In practice**:
- Open only the files relevant to the task before invoking Claude.
- State the goal in the first message — no preamble.
- Resist the urge to add "oh and also..." after pressing enter.

## 2. Aim is a beginner's strategy

Novice archers aim with the eyes. Masters aim with the stance. By the time the master draws the bow, the arrow is already on the target — the body integrated it before the mind noticed.

**Rule**: Do not over-specify the prompt. An over-specified prompt signals distrust of the model and blocks the range of acceptable outputs. Under-specifying with a clean setup signals trust of your own framing. The prompt is the stance, not the aim.

**In practice**:
- If you find yourself writing more than three "make sure to..." clauses, your project structure is doing too little of the work.
- Move constraints into `CLAUDE.md` or file naming, not into every prompt.

## 3. The target teaches, not the archer

When the arrow misses, the beginner asks "what did I do wrong?" and grips harder. The master asks "what did my form not know?" and loosens.

**Rule**: When Claude's output is wrong, do not argue with the output. Read the failure as a diagnosis of the setup — which file was missing, which constraint was implicit, which name was ambiguous. Fix the setup, then re-shoot. Never debug by adding apology-prompts on top of a broken base.

**In practice**:
- If Claude writes to the wrong file, your file naming was unclear. Rename.
- If Claude picks the wrong pattern, your `CLAUDE.md` didn't contain the rule. Add it.
- If Claude hallucinates an API, your context didn't include the real one. Load it.

## 4. Right breath before right shot

No kyūdō shot begins with the draw. It begins with the breath and the posture. Without those, the draw is tension disguised as intent.

**Rule**: Before invoking Claude, your context must be clean. Files open should match files relevant. The goal should be one sentence, not a paragraph. The `CLAUDE.md` should be loaded. The last session's noise should be closed. **Garbage context, garbage output.** Always.

**In practice**:
- Close unrelated editor tabs before starting a new task.
- Start hard tasks in a fresh session, not a mid-context one.
- If the previous prompt went badly, restart — do not layer corrections.

## 5. The bowstring cuts those who grip too hard

A tight grip produces a jerky release and the string catches the forearm on its return. You can see a novice archer by the bruises.

**Rule**: Over-specified prompts waste tokens, collapse the model's range, and produce brittle outputs. Light grip. Clean release. Let the model breathe inside the frame you set. If you can feel yourself writing the output in the prompt, you are not prompting — you are typing.

**In practice**:
- If the prompt is longer than the expected output, you are gripping too hard.
- Replace "write exactly X doing Y with Z" with "implement X" and a clear context.

## 6. The pause at full draw

At full draw there is a moment the master waits for — not a count of seconds, a quality of stillness — where time opens and the shot becomes possible. Rushing it ruins the shot. Forcing it ruins the shot.

**Rule**: After you press enter, let the response finish. Do not interrupt to clarify. Do not cancel on the first sign of drift. Most "corrections" mid-stream are the archer jerking at the bow. You cannot fix form by adding force.

**In practice**:
- Never interrupt a streaming response unless it is genuinely off-rails.
- If Claude says "let me know if I should continue", answer yes by default unless the direction is already wrong.

## 7. A thousand identical shots

Kyūdō form is not reasoned into. It is repeated into. A thousand near-identical shots before any of them land where the master intended. The discipline is the practice, not the theory.

**Rule**: Do not design your AI workflow from first principles or blog posts. Ship two hundred real sessions, watch what repeats, codify that. The `CLAUDE.md` that works is the one written from two hundred sessions — not the one written from twenty articles about prompting.

**In practice**:
- Keep a log of what broke this week and why.
- Every friction you hit twice is a rule that belongs in `CLAUDE.md`.
- Prompt-engineering guides are a map; your sessions are the territory.

## 8. Non-attachment to the hit

Wanting the target creates the tension that makes you miss. The master wants nothing. The arrow flies anyway.

**Rule**: Accept that the first output is not the shipped output. The model knows you are watching and still cannot read your mind. Detach from first-pass perfection. Iteration is not failure — it is the mechanism.

**In practice**:
- Budget two to four iterations for any non-trivial task. Plan them in.
- If the first pass is 70% right, that is a hit. Ship the 70%, correct the 30%.

## 9. Beginner's mind, every shot

*Shoshin*. The hundred-thousandth shot is approached like the first. No memory of yesterday's misses. No pride in yesterday's hits. Only this breath, this bow, this arrow.

**Rule**: Do not carry frustration from the last prompt into the next one. Each session starts clean. Context from a bad session poisons the next. When you feel yourself tightening against the tool, close the window and walk away for five minutes.

**In practice**:
- If two prompts in a row feel wrong, stop. Stretch. Come back.
- Never insult the model mid-session. It changes nothing and poisons your own state.

## 10. The master shoots in the dark

Kenzō Awa, Herrigel's teacher, was said to have shot a target in the night — one arrow finding the bullseye, a second splitting the first. Whether true or myth, the point stands: when form is absolute, sight is unnecessary.

**Rule**: When your scaffolding is right — your `CLAUDE.md`, your project structure, your naming, your commit discipline — you do not need to review every output in detail. Trust the form you built. If you cannot trust it, the problem is the form, not the trust.

**In practice**:
- Build systems where wrong outputs fail loudly, not silently.
- Write tests that catch the class of error you fear. Then stop fearing it.
- At some point, you stop reading every diff. That moment is earned.

---

## When in doubt

- **Set the shot up. Step out of it.**
- **Fix form, not outputs.**
- **One sentence, not a paragraph.**
- **Light grip.**
- **Shoshin.**

---

## Credits and sources

- *Zen in the Art of Archery*, Eugen Herrigel, 1948 (English: 1953). The original source.
- "Shots in the Dark: Japan, Zen, and the West", Shoji Yamada, 2009. The critical counter-reading.
- Every kyūdō teacher who has ever said *it shoots* and meant it.
- Format inspired by [`forrestchang/andrej-karpathy-skills`](https://github.com/forrestchang/andrej-karpathy-skills) and [`Ege-Deniz/three-skills-for-claude`](https://github.com/Ege-Deniz/three-skills-for-claude).

Distilled by [@Ege-Deniz](https://github.com/Ege-Deniz), former national archer for Turkey, now a builder. If this file changes how you work with AI, tell me.
