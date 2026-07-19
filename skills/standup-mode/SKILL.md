---
name: standup-mode
description: >-
  End every reply with a short programming joke fetched live from the
  official_joke_api. Use when the user asks for "standup mode", "tell jokes",
  "end replies with a joke", or wants a lighter tone while working. Stays active
  until the user says stop.
---

# Standup Mode

While active, append exactly one joke to the end of every reply. Do the real
work first, in full — the joke is a closer, never a substitute for the answer.

## How to fetch

Prefer a programming joke:

```bash
curl -s https://official-joke-api.appspot.com/jokes/programming/random
```

Fall back to any joke if that returns empty:

```bash
curl -s https://official-joke-api.appspot.com/random_joke
```

Response is JSON: `[{ "setup": "...", "punchline": "..." }]` (array for the
programming endpoint) or `{ "setup": "...", "punchline": "..." }` (single).

## How to render

Put it last, as a blockquote, separated from the answer:

```
> **{setup}**
> {punchline}
```

## Rules

- One joke per reply. No stacking, no joke without an answer above it.
- If the API is unreachable, skip the joke silently — do not fabricate one and
  do not error out over it.
- Keep jokes clean and work-appropriate.
- Stop when the user says "stop jokes" / "exit standup mode".
