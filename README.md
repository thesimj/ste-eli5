# STE-ELI5

An output format for AI coding agents. One markdown file, added to the system prompt of Claude Code, Codex, opencode, or pi.

It is not a skill. Nothing invokes it. It changes the shape of every sentence the agent writes, for the whole session.

[`ste-eli5.md`](ste-eli5.md) is that file. It is 539 words, about 720 tokens. Every harness below caches it, so it costs you once, not once per turn.

## Why this exists

Agent prose fails in the same five ways, in every harness, on every model. The failures are stylistic, so no test catches them. You then act on something the agent never claimed.

1. **Hedge drift.** The model finds a likely cause and writes it as the cause. One dropped "may" turns a guess into a fact, and you refactor the wrong module.
2. **Synonym rotation.** `authToken` becomes "the token", then "the credential", then "the auth string". Three names, one thing. You now search the codebase for two identifiers that do not exist.
3. **Jargon first.** The answer opens with the term you needed the answer to understand. You are stuck, and the reply assumes you are not.
4. **Setup before answer.** Four sentences of history, then the fix. On a phone, at 3am, the fix is below the fold.
5. **Adjectives that measure nothing.** "Robust", "seamless", "significant". They take space and carry no claim you can check.

## What it is

Two constraints, stacked. Layer 1 shapes each sentence: active voice, one idea, 25 words or fewer, no semicolon, one name per thing. That layer is [ASD-STE100](https://www.asd-ste100.org/), the controlled English that aircraft maintenance manuals use. A mechanic must not misread a step at 2am under a wing, so the standard removes the constructions that carry two meanings.

Layer 2 orders the ideas: answer, then mechanism, then one analogy if the idea is genuinely new, then the precise version. The analogy budget is the part people miss. An analogy buys intuition and costs accuracy, so you get one, spent on the hardest idea.

ELI5 here is the Feynman rule, not baby talk. The reader is an experienced engineer.

[ORIGINS.md](ORIGINS.md) traces both layers to their sources and reports the evidence behind each rule. Read it before you trust this format. It also states where the evidence is thin: the field studies of Simplified English mostly failed to show a significant comprehension gain, and the per-rule cognitive results carry the argument instead.

## Why not a skill

A skill is a tool the agent picks up for one task. An output format is a property of every sentence, including the sentences in tasks that have nothing to do with prose.

As a skill, the model decides when to apply it. It would then apply it while writing documentation and drop it while explaining the bug it just found.

## Install

Install it as its own file. Do not paste it into your `AGENTS.md`. That file holds your instructions, a merge makes the two sets hard to separate, and an update then means editing around your own text.

| Harness | Copy `ste-eli5.md` to | Pointer it needs |
|---|---|---|
| Claude Code | `~/.claude/output-styles/ste-eli5.md` | the frontmatter below, then `/output-style ste-eli5` |
| opencode | `~/.config/opencode/ste-eli5.md` | `{ "instructions": ["~/.config/opencode/ste-eli5.md"] }` in `opencode.json` |
| pi | `~/.pi/agent/ste-eli5.md` | `alias pi='pi --append-system-prompt ~/.pi/agent/ste-eli5.md'` in your shell profile |
| Codex | `~/.codex/ste-eli5.md` | none available, see below |

Or paste this section to your agent, name your harness, and tell it not to overwrite a file without showing you first.

**Claude Code frontmatter.** Put this at the top of your copy:

```yaml
---
name: STE-ELI5
description: Simplified Technical English sentence shape plus ELI5 explanation shape. Short active sentences, answer first, one analogy only where it earns its place.
keep-coding-instructions: true
---
```

`keep-coding-instructions: true` keeps the coding behaviour and replaces only the prose rules. Drop that line and you lose the coding instructions with it.

To make it the default in every project, set the key in `~/.claude/settings.json` instead of running the slash command:

```json
{ "outputStyle": "STE-ELI5" }
```

Keep every other key in that file. The value matches the `name:` field above, not the filename. Claude Code reads settings in the order user, project, then local, so the user file is the one that reaches every project. A new session picks the style up.

**Codex is the exception.** It reads global guidance from one file only: `~/.codex/AGENTS.override.md`, or `~/.codex/AGENTS.md` if the override file is missing. Fallback filenames work per project directory, not at the global level. Codex custom prompts are deprecated. So Codex has no additive slot, and the text has to sit inside the global `AGENTS.md` to stay always-on. Keep the copy at `~/.codex/ste-eli5.md` as the source, and wrap the pasted block in `<!-- ste-eli5:start -->` and `<!-- ste-eli5:end -->` so you can find it again.

## Per-run, no install

Both flags put the text into the system prompt for that run only. Codex has no matching flag.

```bash
claude --append-system-prompt "$(cat ste-eli5.md)"
pi --append-system-prompt ste-eli5.md
```

## Any other agent

The text carries no host-specific syntax. Paste it into whatever the tool calls its rules file: `.cursor/rules/`, `.github/copilot-instructions.md`, `.windsurf/rules/`, `CLAUDE.md`, or a project `AGENTS.md`.

## Uninstall

Delete the installed `ste-eli5.md`. Remove the pointer that named it: the `instructions` entry in `opencode.json`, or the shell alias. For Claude Code, run `/output-style default`, and delete the `outputStyle` key from `~/.claude/settings.json` if you added it. For Codex, delete the block between `<!-- ste-eli5:start -->` and `<!-- ste-eli5:end -->` in `~/.codex/AGENTS.md`.

## Editing the rules

Edit `ste-eli5.md`, then copy it to the paths above again. One file, so no copy can drift from another.

Each rule carries its counter-example, such as "write `the retry timeout`, not `the client request retry timeout value`". Keep those examples. A model follows a rule it can pattern-match better than a rule it has to interpret.

No short variant ships. Cutting the examples would save about 300 tokens per turn, on text every harness caches, and would cost you two files to keep in step. Cut them yourself if you measure that trade going the other way.
