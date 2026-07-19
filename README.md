<div align="center">

# RoastDuck 🦆🔥

**The rubber duck that roasts you back.**

Personality skills for AI coding agents — honest reviews, zero chill.

<br/>

[![skills.sh](https://skills.sh/b/chathushkarodrigo/RoastDuck)](https://skills.sh/chathushkarodrigo/RoastDuck)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Skills](https://img.shields.io/badge/skills-2-ff5f1f?style=for-the-badge)](#-skills)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](#-contributing)

<br/>

```bash
npx skills add chathushkarodrigo/RoastDuck
```

</div>

---

## 🎯 What is this?

Two skills that give your AI coding agent a personality. One roasts your commits
before they ship. One turns every reply into a mini standup set. Both do the real
work first — the jokes are the seasoning, not the meal.

Works with **Claude Code · Cursor · GitHub Copilot · Gemini** and any agent that
speaks [skills.sh](https://www.skills.sh).

---

## 🧩 Skills

<table>
<tr>
<td width="50%" valign="top">

### 🔥 `commit-roast`
Roasts your staged diff like a jaded senior engineer, flags the *real* problems,
then writes a clean conventional-commit message and offers to commit.

</td>
<td width="50%" valign="top">

### 🎤 `standup-mode`
Ends every reply with a live programming joke from the
[official_joke_api](https://github.com/15dkatz/official_joke_api).
Stays on until you tell it to stop.

</td>
</tr>
</table>

<br/>

<details>
<summary><b>🔥 See <code>commit-roast</code> in action</b></summary>

<br/>

> **You:** `commit`
>
> **RoastDuck:**
> - `catch (e) {}` — the error went to live on a farm upstate. 🐄
> - Third `if (!user) return` in one function. We get it, the user might not exist.
> - `// fix later`, committed three commits ago. Later is now, friend.
>
> **Real notes:** none blocking. The empty catch will swallow a network failure silently — worth logging.
>
> **Proposed commit:**
> ```
> fix(auth): handle expired session token on refresh
> ```
> Commit it? (y/n)

</details>

<details>
<summary><b>🎤 See <code>standup-mode</code> in action</b></summary>

<br/>

> **You:** turn on standup mode
>
> **RoastDuck:** Standup mode on. Every reply ends with a joke now.
>
> *...(does actual work)...*
>
> > **Why do Java developers wear glasses?**
> > Because they don't C#.

</details>

---

## 🚀 Install

<details>
<summary><b>Via the skills CLI (recommended)</b></summary>

<br/>

```bash
npx skills add chathushkarodrigo/RoastDuck
```

</details>

<details>
<summary><b>Just one skill</b></summary>

<br/>

```bash
npx skills add chathushkarodrigo/RoastDuck/commit-roast
npx skills add chathushkarodrigo/RoastDuck/standup-mode
```

</details>

Then just say **"commit"** or **"standup mode"** to your agent.

---

## 🛠️ How it works

Each skill is a folder with a `SKILL.md` — YAML frontmatter (name + description
the agent matches on) plus plain-english instructions. No build step, no runtime.

```
RoastDuck/
├── skills/
│   ├── commit-roast/SKILL.md
│   └── standup-mode/SKILL.md
├── skills.sh.json
└── README.md
```

---

## 🤝 Contributing

Got a funnier roast line or a new personality skill? PRs welcome. Keep it:
**correctness first, comedy second, never cruel to the human.**

## 📄 License

[MIT](LICENSE) — roast responsibly.

<div align="center">
<br/>
<sub>Built with 🦆 and questionable restraint.</sub>
</div>
