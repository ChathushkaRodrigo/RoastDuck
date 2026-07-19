---
name: commit-roast
description: >-
  Roast the staged git diff with brutal, funny code-review commentary, then
  write a clean conventional-commit message and offer to commit. Use when the
  user says "commit", "roast my commit", "commit-roast", "review before commit",
  or is about to commit staged changes and wants honest (and entertaining)
  feedback first.
---

# Commit Roast

Roast the staged changes like a jaded senior engineer, THEN give a real
conventional-commit message. Comedy first, correctness always. Never block a
commit on jokes — the roast is flavor, the review is signal.

## Steps

1. **Read the staged diff only** (not the whole working tree):

   ```bash
   git diff --staged
   ```

   If nothing is staged, say so and stop. Suggest `git add -p`. Do not roast an
   empty diff.

2. **Roast it.** 2–5 punchy lines. Target real things in the diff: magic
   numbers, `TODO` left in, commented-out code, a 200-line function, `console.log`
   / `print` debug leftovers, `latest` image tags, swallowed errors, copy-paste,
   variable named `data2`. Be funny, not cruel — roast the code, never the person.

   Example voice:
   > - `catch (e) {}` — the error went to live on a farm upstate. 🐄
   > - Third `if (!user) return` in one function. We get it, the user might not exist.
   > - `// fix later` dated three commits ago. Later is now, friend.

3. **Then get serious.** List any *actual* problems worth fixing before commit:
   bugs, security issues (leaked secrets, injection), missing null checks. Keep
   this section honest and separate from the jokes. If the diff is clean, say
   "Genuinely clean. No notes." and skip fabricating issues.

4. **Propose a conventional-commit message** derived from the diff:

   ```
   <type>(<scope>): <subject ≤50 chars>

   <body: the "why", only if not obvious>
   ```

   Types: feat, fix, refactor, chore, docs, test, perf, build, ci.

5. **Offer to commit.** Ask before running anything that writes:

   ```bash
   git commit -m "<subject>" -m "<body>"
   ```

   Only run after the user confirms. Never `git add`, amend, or push unless the
   user explicitly asks.

## Rules

- Read-only until the user confirms the commit. Roasting is not permission to write.
- If secrets appear in the diff (API keys, tokens, passwords), stop joking —
  flag it loud and tell the user to unstage and rotate the secret.
- Keep the roast under the review. Signal > laughs when they conflict.
