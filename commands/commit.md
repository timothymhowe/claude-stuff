Create a git commit using Conventional Commits format with gitmoji, compatible with semantic-release.

## Steps

1. Run `git status` and `git diff` (staged and unstaged) to understand all changes
2. Run `git log --oneline -5` to match the repo's existing commit style
3. Stage appropriate files (prefer specific files over `git add -A`)
4. Write and create the commit

## Commit Format

```
<emoji> <type>(<scope>): <short description>

[optional body — explain the *why*, not the what]

[optional footer(s)]
```

## Type → Emoji Mapping

| Type | Emoji | Triggers semantic-release |
|---|---|---|
| feat | ✨ | minor |
| fix | 🐛 | patch |
| perf | ⚡️ | patch |
| revert | ⏪️ | patch |
| docs | 📝 | no |
| style | 💄 | no |
| refactor | ♻️ | no |
| test | ✅ | no |
| build | 📦️ | no |
| ci | 👷 | no |
| chore | 🔧 | no |

For breaking changes, append `!` after the type and add a `BREAKING CHANGE:` footer:

```
💥 feat!(<scope>): drop support for Node 16

BREAKING CHANGE: Node 16 is no longer supported, upgrade to Node 18+.
```

Other useful emoji:
- 🎉 `init` — initial commit
- 🔥 removing code/files
- 🚑️ critical hotfix
- 🔒️ security fix
- 🏗️ architectural changes

## Rules

- Subject line: imperative mood, lowercase, no period, max 72 chars
- Scope: optional, lowercase, describes the module/area (e.g. `auth`, `api`, `memory`)
- Body: wrap at 72 chars, explain *why* not *what*
- Do NOT add Co-Authored-By lines
- Do NOT use `git add -A` or `git add .` — stage files by name
- Do NOT skip hooks (`--no-verify`)
- Do NOT amend existing commits — always create a new one
