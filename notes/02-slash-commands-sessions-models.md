# 02 · Slash Commands, Sessions & Models

Claude Code ships with many **built-in slash commands**, and you can create **custom** ones (see [08](08-custom-slash-commands.md)).

## Launch / resume
| Command | What it does |
|---|---|
| `claude` | Launch Claude Code |
| `claude -r` | List all past sessions and resume one directly |
| `/resume` | Switch to a different session after Claude Code has launched |
| `/exit` | Exit the current session |

Sessions are stored locally under `~/.claude/projects`.

## Session management
- **One task, one session** principle: keeps work organized and focused.
- Commit work frequently within sessions so you don't lose progress.

| Command | What it does |
|---|---|
| `/rename` | Rename the current session at any time |
| `/btw` | Quick off-the-record question. Not saved to session history; disappears after use (press space to dismiss) |
| `/export <file_name>` | Save the whole conversation history to a file |
| `/login` / `/logout` | Log in/out. You can keep multiple accounts (personal + company) |
| `/rewind` | Go back to an earlier point in the conversation **and undo code changes** |

## Models
| Model | Best for |
|---|---|
| **Opus** | Complex programming, deep reasoning |
| **Sonnet** | Day-to-day development |
| **Haiku** | Faster and cheaper, lightweight tasks |

- **Recommended workflow:** Opus for thinking/planning, then Sonnet for code generation.
- `/model` switches models mid-session.

## Usage & configuration
| Command | What it does |
|---|---|
| `/usage` | Current session and weekly usage limits |
| `/extra-usage` | Request an increase to your usage limit |
| `/stats` | Detailed usage statistics |
| `/insights` | Personalized suggestions on using Claude Code better |
| `/config` | Manage configuration settings |
| `/permissions` | Define which tools can run: auto-allow, ask first, or deny. Scoped at local / project / global level |
| `/theme` | Change the visual theme |
| `/voice` | Voice mode (hands-free) |

> **/permissions = human in the loop.** Decide which tools Claude may use without asking and which need your approval.

---
Prev: [01](01-basics-and-ollama.md) · Next: [03 · Editing code](03-editing-code.md)
