# coding-agent-guides

Modular `AGENTS.md` instructions for LLM coding agents. Pick the files a
project needs and copy them in.

## How it works

- `AGENTS-vN.md` is the entry point. In a project it becomes `AGENTS.md`.
- It tells the agent to also follow the files in `AGENTS.md.d/`, if that
  directory exists.
- All other files are optional add-ons for `AGENTS.md.d/`.
- The `-vN` suffix is the file's version. Keep it when you copy a file, so
  you can see at a glance how far behind a project is.

## Deploying to a project

```sh
G=path/to/coding-agent-guides
cp $G/AGENTS-vN.md . && ln -s AGENTS-vN.md AGENTS.md
mkdir -p AGENTS.md.d && cp $G/CLI-DESIGN-vN.md $G/CLI-WRITING-STYLE-vN.md AGENTS.md.d/
```

The symlink keeps the entry point's version visible. Renaming it to
`AGENTS.md` works too, but then the version is gone from the name.

## Files

| File | Contents |
|---|---|
| `AGENTS` | Entry point: agent behavior, README upkeep, code, testing, commit messages. Its code rules assume Python (`ruff`, modern syntax). |
| `AGENT-RETROSPECTION` | After a problem, propose changes to `AGENTS.md` and `AGENTS.md.d/`. |
| `CLI-DESIGN` | UX and code structure for command-line tools. |
| `CLI-WRITING-STYLE` | Writing style for READMEs, `--help`, docstrings, comments and runtime messages. |
| `CODE-QUALITY` | Raises the bar: code will be reviewed by senior developers. |
| `DOCUMENTATION-EXTRAS` | Keep separate terminology and conventions files, linked from the README. |
| `PROJECT-DISCOVERABILITY` | Keep the README and GitHub About/Topics search-engine friendly. |

Only the latest version of each file is kept here. Older versions are in git
history.

`AGENTS.md` (symlinked as `CLAUDE.md`) holds instructions for agents working
on this repo itself. Don't deploy it.

## License

MIT
