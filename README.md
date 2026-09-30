# coding-agent-guides

Modular `AGENTS.md` instructions for LLM coding agents. Pick the files a
project needs and copy them in.

## How it works

- `AGENTS-vN.md` is the entry point. Copy it to the target project and symlink it to `AGENTS.md`.
- It tells the agent to also follow the files in `AGENTS.md.d/`, if that
  directory exists.
- All other files are optional add-ons to be put in the `AGENTS.md.d/` directory.
- The `-vN` suffix is the file's version. Keep it when you copy a file to, so
  you can see at a glance how far behind a project is.


## Files

| File | Contents |
|---|---|
| `AGENTS` | Entry point: agent behavior, README upkeep, code, testing, commit messages. |
| `AGENT-RETROSPECTION` | After a problem, propose changes to `AGENTS.md` and `AGENTS.md.d/`. |
| `CLI-DESIGN` | UX and code structure for command-line tools. |
| `CLI-WRITING-STYLE` | Writing style for READMEs, `--help`, docstrings, comments and runtime messages. |
| `CODE-QUALITY` | Raises the bar: code will be reviewed by senior developers. |
| `DOCUMENTATION-EXTRAS` | Keep documentation files, linked from the README. |
| `PROJECT-DISCOVERABILITY` | Keep the README and GitHub About/Topics search-engine friendly. |

`AGENTS.md` (symlinked as `CLAUDE.md`) holds instructions for agents working
on this repo itself. Don't deploy it.

## License

MIT
