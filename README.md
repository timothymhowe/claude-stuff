# claude-stuff

Personal Claude Code configuration — custom slash commands and anything else that makes Claude more useful day-to-day.

## Setup

```bash
git clone https://github.com/timothymhowe/claude-stuff ~/Projects/claude-stuff
ln -s ~/Projects/claude-stuff/commands ~/.claude/commands
```

## Structure

```
commands/       # Custom slash commands — each .md file becomes a /command in Claude Code
```

## Commands

| Command | Description |
|---|---|
| `/commit` | Stage and commit using Conventional Commits + gitmoji, semantic-release compatible |

## Adding a New Command

Create a `.md` file in `commands/`:

```bash
touch ~/Projects/claude-stuff/commands/my-command.md
```

The filename becomes the slash command — `my-command.md` → `/my-command`. The file contents are the prompt Claude follows when you invoke it.
