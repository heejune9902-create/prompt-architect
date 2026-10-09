# Prompt Architect

English | [한국어](../README.md)

A Claude skill that **designs the prompt and instruction files** for a task you want to hand off.

It contains 16 method modules drawn from recent research and talks on using AI agents (verification loops, computing in code, context management, checking against ground truth, least privilege, separating the monitor, fixed classification, and more). It diagnoses the task, then **picks and combines only the methods it needs**. The point is not to attach every technique.

## What it does

- Task diagnosis: type, risk, verifiability (at most 3 questions)
- Method selection table: methods chosen and methods dropped, with the reason for each
- An execution prompt you can paste in and use right away
- Instruction files when needed (`CLAUDE.md`, `AGENTS.md`, `SKILL.md` formats)
- A prompt test plan and reviewer agent setup
- On your approval, runs the prompt test (repeated runs and scoring) with subagents and reports a scorecard

## Folder layout

| Path (from the repository root) | Purpose |
| --- | --- |
| `en/skills/prompt-architect/SKILL.md` | The Claude skill itself |
| `en/guide/prompt-architect-guide.md` | Guide version to attach to AIs that can't use skills (ChatGPT, Codex, etc.) |
| `skills/`, `guide/` | Korean originals |

## Installation

### Claude Code

```bash
git clone https://github.com/heejune9902-create/prompt-architect.git
mkdir -p ~/.claude/skills
cp -r prompt-architect/en/skills/prompt-architect ~/.claude/skills/
```

To use it in one project only, put it in that project's `.claude/skills/` instead of `~/.claude/skills/`.

The Korean and English versions share the skill name `prompt-architect`, so install only one of them.

### claude.ai

Zip the `en/skills/prompt-architect` folder and upload it from the skills menu in Settings.

### Other AI tools

Attach `en/guide/prompt-architect-guide.md` to the conversation and ask as shown below.

## Example

```text
Design the prompt and instruction file for the task below.
Where it will be used: chat
Task: I want to analyze short-form videos that went viral on social media in the last 3 days
```

In Claude Code, you can call it directly by typing `/prompt-architect` followed by the task.

## Caveats

- Most of the evidence behind the modules comes from preprints that have not been peer-reviewed, or from company announcements. Effects are not guaranteed, and any prompt you design should be confirmed by testing.
- Prompt testing involves repeated runs, so it uses up quota. It asks for your approval once before testing.
- This is an English translation of the Korean original at the repository root.

## License

MIT
