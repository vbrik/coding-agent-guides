# Agent
- Ask clarifying questions until you are certain you understand the problem
- Flag design contradictions
- Flag logical contradictions
- Flag incosistencies
- Flag scope creep (e.g. one tool has does too many things that are not particularly related)
- Flag logical simplification opportunities
- Flag code reuse opportunities
- Don't create git commits automatically
- Use best practices of the programming language you are using
- Follow project-specific instructions in files in `AGENTS.md.d` directory, if it exists.

# Project
- Maintain README.md file to stay in sync with changes. Keep it nice. Aim for brevity and clarity

# Code
- Ensure code does not get out of sync with comments and docstrings
- Structure code for human readability
- Make comments concise
- Write doc strings except for trivial functions
- Use latest available python features, syntax, modules to improve code
- Assume the reader is a python expert
- Run `ruff` on python files (make both "format" and "check" subcommands happy)

# Testing
- Add unit tests for new or changed functionality
- If makes sense, add unit tests when the way of how components interact changes
- Run unit tests to check your work
- Test corner conditions

# Git commit messages
- In *addition* to normal stuff that goes into commit message bodies
  - Include info about the reasoning that led to the changes, so that later we could flag contradictory design decisions:
    - In commit messages include design choices that resulted in the changes
    - In commit messages include intentions behind the changes
