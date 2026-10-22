# coding-agent-guides

Modular `AGENTS.md` instructions for LLM coding agents. Pick the files a
project needs from `instructions/` and copy them in to `AGENTS.md.d` of your project.

## How it works

- `AGENTS-vN.md` is the entry point. Copy it to the target project and symlink it to `AGENTS.md`.
- It tells the agent to also follow the files in `AGENTS.md.d/`, if that
  directory exists.
- All other files are optional add-ons to be put in the `AGENTS.md.d/` directory.
- The `-vN` suffix is the file's version. Keep it when you copy a file, so
  you can see at a glance how far behind a project is.


## Files

| File | Contents |
|---|---|
| `AGENTS` | Entry point: ask clarifying questions; flag contradictions, scope creep, simplification and reuse opportunities; never push. |
| `AGENT-RETROSPECTION` | After a tricky problem, propose additions to `AGENT-LESSONS-LEARNED.md`. |
| `CLI-DESIGN` | UX and code structure for command-line tools. |
| `CLI-WRITING-STYLE` | Writing style for READMEs, `--help`, docstrings, comments and runtime messages. |
| `CODE` | Code readability, docstrings, modern language features; unit tests. |
| `CODE-QUALITY` | Raises the bar: code will be reviewed by senior developers. |
| `DO-NO-EVIL` | Leave the host system alone: no package installs, config changes, `sudo` or privilege escalation. |
| `DOCUMENTATION-EXTRAS` | Keep terms and conventions files, linked from the README. |
| `DSCHULTZ` | General assistant persona: factual, concise, says "I don't know", documents code and decisions. |
| `GIT` | Propose commit messages instead of committing; no branches; record reasoning in commit messages. |
| `PROJECT-DISCOVERABILITY` | Keep the README and GitHub About/Topics search-engine friendly. |
| `PYTHON` | Run `ruff format` and `ruff check`. |

`AGENTS.md` (symlinked as `CLAUDE.md`) holds instructions for agents working
on this repo itself. Don't deploy it.

## License

MIT
