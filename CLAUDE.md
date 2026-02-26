# CLAUDE.md

This file provides guidance to Claude when working in this repository.

## Project Overview

`hello-world` is a minimal repository with a single README. There are no build tools, package managers, tests, or linters configured at this time.

## Repository Structure

```
hello-world/
├── README.md                        # Project description
├── CLAUDE.md                        # This file
└── .claude/
    ├── settings.json                # Claude Code hook configuration
    └── hooks/
        └── session-start.sh         # SessionStart hook for remote sessions
```

## Development Notes

- No dependencies to install.
- No linter or test suite is configured. Add one here when the project grows.
- The SessionStart hook (`.claude/hooks/session-start.sh`) is a no-op for now and can be extended to install dependencies as the project evolves.

## Adding Dependencies

When you add a package manager to this project, update `.claude/hooks/session-start.sh` to install dependencies. For example:

- **Node.js**: add `npm install`
- **Python**: add `pip install -r requirements.txt` or `poetry install`
- **Ruby**: add `bundle install`
