# Claude Code Basics: Revision Notes

Source: `Claude_Code.pdf` (OneNote export, 40 pages). All 44 embedded images were extracted into [`images/`](images/) and embedded in the relevant notes.

## Index
| # | Topic | Key idea |
|---|---|---|
| 01 | [Basics & Ollama](01-basics-and-ollama.md) | Bash mode, run Claude Code on open-source models |
| 02 | [Slash commands, sessions & models](02-slash-commands-sessions-models.md) | `/resume`, `/rename`, `/model`, `/permissions`, ... |
| 03 | [Editing code](03-editing-code.md) | `@` files, paste images, prompts in files |
| 04 | [Context engineering](04-context-engineering.md) | Context window, triangular cost, `/compact`, `/clear` |
| 05 | [CLAUDE.md & memory](05-claude-md-and-memory.md) | Persistent project instructions, `.claude/rules`, MEMORY.md |
| 06 | [Vibe coding vs SDD](06-spec-driven-development.md) | Spec → Review → Design → Review → Tasks → Build → Validate |
| 07 | [Plan mode & git workflow](07-plan-mode-and-git-workflow.md) | `/plan`, `/effort`, `/ultraplan`, branch-per-feature |
| 08 | [Custom slash commands](08-custom-slash-commands.md) | `.claude/commands/*.md`, args, `create-spec` |
| 09 | [Skills](09-skills.md) | `SKILL.md`, progressive disclosure |
| 10 | [Subagents](10-subagents.md) | Own context window, frontmatter fields, test/review agents |
| 11 | [MCP](11-mcp.md) | SQLite, Figma, GitHub, Context7, Jira, Notion, Slack, AWS, Docker |
| 12 | [Harness & hooks](12-harness-and-hooks.md) | Agent loop, PreToolUse hooks, exit code 2 = block |
| 13 | [Plugins & marketplaces](13-plugins-and-marketplaces.md) | `plugin.json`, `marketplace.json`, `/plugin` |

## The whole workflow in one line
New branch → `/create-spec` → review → `/plan` → build → `/test-feature` → `/code-review-feature` → GitHub MCP / `/ship-feature` → delete branch, back to `main`. Hooks guard the dangerous bits.

## Quick cheat sheet
| Folder / file | Holds |
|---|---|
| `CLAUDE.md`, `CLAUDE.local.md` | Project instructions (team / personal) |
| `.claude/settings.json`, `settings.local.json` | Permissions, hooks |
| `.claude/commands/` | Custom slash commands |
| `.claude/skills/<name>/SKILL.md` | Skills |
| `.claude/agents/` | Custom subagents |
| `.claude/rules/` | Rules loaded on demand |
| `.claude/specs/`, `.claude/plans/` | Specs and technical plans |
| `.claude/hooks/` | Hook scripts |
| `~/.claude/...` | Same, but global/personal |
| `~/.claude/projects/` | Stored sessions and auto-memory |

## ⚠️ Security warning
The original PDF (pages ~23–24, MCP section) contains a **GitHub personal access token in plain text**. It was deliberately **not** copied into these notes. Since the PDF sits in a OneDrive folder, **revoke that token** in GitHub → Settings → Developer settings → Personal access tokens, and create a new one if needed. Then remove it from the OneNote page too.

## Not covered by the PDF text
The prompt for turning these notes into a LinkedIn blog (pages 39–40) just repeats notes 01–03, so it isn't split out separately.
