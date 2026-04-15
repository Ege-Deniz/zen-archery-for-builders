# Zen Archery Examples

Short before/after examples showing what the principles look like in practice.

## 1. Dirty context vs. clean context

**Weak**

```text
Can you fix this? Also keep in mind the other thing from yesterday and maybe use the old component unless the new one is better. I think the problem is in the API but maybe the layout too.
```

**Better**

```text
Read the auth route and the login form. Fix the login redirect bug.
```

Why it works:

- clear target
- small context window
- no speculative side-quests

## 2. Over-gripping the prompt

**Weak**

```text
Write exactly a premium hero section with perfect spacing, but not too much spacing, and make it modern, not generic, and use animation but subtle animation, and make it emotional but sharp, and don't forget accessibility, and maybe do some glass effect.
```

**Better**

```text
Build a premium hero section for an AI developer tool. Use the repo's existing visual language. Prioritize clarity, hierarchy, and one memorable visual move.
```

Why it works:

- the prompt defines direction
- the repo should carry the rest of the rules

## 3. Fix form, not outputs

**Weak**

```text
No, not like that. Try again. Still wrong. Try again but more like the previous version.
```

**Better**

```text
Use the existing `CardGrid` pattern from `src/components/dashboard/CardGrid.tsx`. The issue is that you invented a new layout instead of reusing the current one.
```

Why it works:

- the correction points at the setup problem
- the next attempt has better constraints

## 4. Let the response finish

**Weak**

Interrupting halfway through because the first paragraph sounds slightly off.

**Better**

Let the response complete, then correct the direction once with specifics.

Why it works:

- fewer broken partial attempts
- lower token waste from restart loops

## 5. Restart when the session is poisoned

**Weak**

Keep layering corrections after three messy failed turns.

**Better**

```text
Fresh session. Read `README.md`, `CLAUDE.md`, and `src/lib/api.ts`. Fix the pagination bug in `getProjects`.
```

Why it works:

- clean breath before the shot
- less contamination from previous drift

## 6. When this should become a rule

If you catch yourself repeating one correction such as:

- "use refs, not React state for uniforms"
- "do not invent new folders"
- "check the existing design system first"

then the problem is no longer the prompt. The problem belongs in a persistent rules file.
