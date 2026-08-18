# STE-ELI5

An output format for AI coding agents. One markdown file, added to the system prompt of Claude Code, Codex, opencode, or pi.

It is not a skill. Nothing invokes it. It changes the shape of every sentence the agent writes, for the whole session.

[`ste-eli5.md`](ste-eli5.md) is that file. It is 539 words, about 720 tokens. Every harness below caches it, so it costs you once, not once per turn.

Each rule carries its counter-example, such as "write `the retry timeout`, not `the client request retry timeout value`". Keep those examples. A model follows a rule it can pattern-match better than a rule it has to interpret.

## Why this exists

Agent prose fails in the same five ways, in every harness, on every model. The failures are stylistic, so no test catches them. You read the answer, feel informed, and act on something the agent never actually claimed.

1. **Hedge drift.** The model finds a likely cause and writes it as the cause. One dropped "may" turns a guess into a fact, and you refactor the wrong module.
2. **Synonym rotation.** `authToken` becomes "the token", then "the credential", then "the auth string". Three names, one thing. You now search the codebase for two identifiers that do not exist.
3. **Jargon first.** The answer opens with the term you needed the answer to understand. You are stuck, and the reply assumes you are not.
4. **Setup before answer.** Four sentences of history, then the fix. On a phone, on a pager, at 3am, the fix is below the fold.
5. **Adjectives that measure nothing.** "Robust", "seamless", "significant". They take space and carry no claim you can check.

STE-ELI5 fixes each one with a rule the model can follow mechanically, because each rule is about form, not about judgement.

## What it is, in plain words

Two constraints, stacked. They do not conflict, because they act on different things.

**Layer 1 shapes each sentence.** Active voice, one idea, 25 words or fewer, no semicolon, one name per thing. This layer is [ASD-STE100](https://www.asd-ste100.org/), the controlled English that aircraft maintenance manuals use. A mechanic must not misread a step at 2am under a wing, so the standard removes the constructions that carry two meanings.

**Layer 2 orders the ideas.** Answer, then mechanism, then one analogy if the idea is genuinely new, then the precise version.

The analogy budget is the part people miss. An analogy buys intuition and costs accuracy. You get one, spent on the hardest idea, and you state its limit in the same breath.

ELI5 here is the Feynman rule, not baby talk. The reader is an experienced engineer. Simplify the explanation, never the fact. A conditional answer stays conditional.

[ORIGINS.md](ORIGINS.md) traces both layers to their sources and reports the evidence behind each rule. Read it before you trust this format. It also states where the evidence is thin: the field studies of Simplified English mostly failed to show a significant comprehension gain, and the per-rule cognitive results carry the argument instead.

## Why not a skill

A skill is a tool the agent picks up for one task. An output format is a property of every sentence, including the sentences in tasks that have nothing to do with prose.

As a skill, the model decides when to apply it. It would then apply it while writing documentation and drop it while explaining the bug it just found — the moment the rules matter most. So the text goes in the system prompt, and it stays on.

## Where it goes, per harness

Install it as its own file. Do not paste it into your `AGENTS.md`. That file holds your instructions, a merge makes the two sets hard to separate, and an update then means editing around your own text.

Three of the four harnesses load a standalone file. Each one needs a different path and a different pointer.

| Harness | Install as | Pointer it needs |
|---|---|---|
| Claude Code | `~/.claude/output-styles/ste-eli5.md` | none, run `/output-style ste-eli5`, or one key in `settings.json` |
| opencode | `~/.config/opencode/ste-eli5.md` | one line in `opencode.json` |
| pi | `~/.pi/agent/ste-eli5.md` | one shell alias |
| Codex | `~/.codex/ste-eli5.md` | none available, see below |

**Codex is the exception.** It reads global guidance from one file only: `~/.codex/AGENTS.override.md`, or `~/.codex/AGENTS.md` if the override file is missing. Fallback filenames work per project directory, not at the global level. Codex custom prompts are deprecated. So Codex has no additive slot, and the text has to sit inside the global `AGENTS.md` to stay always-on. Keep the copy at `~/.codex/ste-eli5.md` as the source, and wrap the pasted block in `<!-- ste-eli5:start -->` and `<!-- ste-eli5:end -->` so you can find it again.

Claude Code is the only one of the four with a slot built for output format. The frontmatter it needs:

```yaml
---
name: STE-ELI5
description: Simplified Technical English sentence shape plus ELI5 explanation shape. Short active sentences, answer first, one analogy only where it earns its place.
keep-coding-instructions: true
---
```

`keep-coding-instructions: true` keeps the coding behaviour and replaces only the prose rules. Drop that line and you lose the coding instructions with it.

**To make it the default in every project**, name the style in `~/.claude/settings.json` instead of running the slash command:

```json
{ "outputStyle": "STE-ELI5" }
```

Keep every other key in that file. The value matches the `name:` field of the frontmatter above, not the filename. Claude Code reads settings in the order user, project, then local, so the user file is the one that reaches every project. A new session picks the style up.

## Install it by asking the agent

Open the harness you want to change, then paste this. It works in all four, because each one can read files and write files.

```text
Install the STE-ELI5 output format from this repo into my harness.

Rule that beats every step below: install it as its own file. Do not edit my AGENTS.md
unless the harness gives you no other way, and tell me plainly when that happens.

1. Work out which harness you are running: Claude Code, Codex, opencode, or pi.

2. Claude Code. Copy `ste-eli5.md` to `~/.claude/output-styles/ste-eli5.md`. Put the
   YAML frontmatter block from README.md at the top of the copy. Ask me whether I want
   it in this project only or in every project. For this project only, tell me to run
   `/output-style ste-eli5`. For every project, set `"outputStyle": "STE-ELI5"` in
   `~/.claude/settings.json` and keep every other key in that file.

3. opencode. Copy `ste-eli5.md` to `~/.config/opencode/ste-eli5.md`. Add that path to
   the `instructions` array in `~/.config/opencode/opencode.json`. Create the array if
   it is missing, and keep every other key. Read the file first, because a hand-edited
   config can hold a trailing comma that a strict JSON parser rejects.

4. pi. Copy `ste-eli5.md` to `~/.pi/agent/ste-eli5.md`. Print this alias for me to add
   to my shell profile, and do not edit the profile yourself:
   alias pi='pi --append-system-prompt ~/.pi/agent/ste-eli5.md'

5. Codex. Copy `ste-eli5.md` to `~/.codex/ste-eli5.md`. Codex reads global guidance
   from `~/.codex/AGENTS.md` only, so that copy alone changes nothing. Ask me before
   you touch `~/.codex/AGENTS.md`. If I agree, append the same text inside
   `<!-- ste-eli5:start -->` and `<!-- ste-eli5:end -->` markers. If those markers are
   already there, replace what sits between them. Keep every other line of that file.

6. Create parent directories that do not exist. Never overwrite a file you did not
   write, without showing me what it holds first.

7. Print each path you wrote, and the one manual step I still have to do.
```

## Install it by hand

**Claude Code.** Copy `ste-eli5.md` to `~/.claude/output-styles/ste-eli5.md`, add the frontmatter above, then run `/output-style ste-eli5`. For every project, set `"outputStyle": "STE-ELI5"` in `~/.claude/settings.json` instead.

**opencode.** Copy `ste-eli5.md` to `~/.config/opencode/ste-eli5.md`, then name it in `~/.config/opencode/opencode.json`:

```json
{ "instructions": ["~/.config/opencode/ste-eli5.md"] }
```

**pi.** Copy `ste-eli5.md` to `~/.pi/agent/ste-eli5.md`, then alias the flag in your shell profile:

```bash
alias pi='pi --append-system-prompt ~/.pi/agent/ste-eli5.md'
```

**Codex.** Copy `ste-eli5.md` to `~/.codex/ste-eli5.md` to keep a clean source. Then paste the same text into `~/.codex/AGENTS.md`, inside the two markers. Codex offers no other always-on slot.

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

A shorter variant is a fair idea and this repo does not ship one. It would save about 300 tokens per turn, on text every harness caches, and it would cost you two files to keep in step. Cut the examples yourself if you ever measure that trade going the other way.
