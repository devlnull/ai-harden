# ai-harden

Global rules for Claude Code.

## Structure

- `CLAUDE.md` is the entry file. It imports each rule file with `@rules/<name>.md`.
- `rules/` has one file for each topic.

## Install

Copy the files into the global Claude directory:

```sh
mkdir -p ~/.claude/rules
cp CLAUDE.md ~/.claude/CLAUDE.md
cp rules/*.md ~/.claude/rules/
```

Start a new Claude Code session. Run `/memory` to see the loaded files.

## Add a rule file

1. Add the file to `rules/`.
2. Add an `@rules/<name>.md` line to `CLAUDE.md`.
