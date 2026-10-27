# ai-harden

Global rules for Claude Code.

## Structure

- `rules/` has one file for each topic.
- Claude Code loads each file in `~/.claude/rules/` in every session. No import line is necessary.

## Install

Link the global rules folder to this repo. Then each change in the repo applies on the next session:

```sh
rm -rf ~/.claude/rules
ln -s "$PWD/rules" ~/.claude/rules
```

Start a new Claude Code session. Run `/memory` to see the loaded files.

## Add a rule file

Add a Markdown file to `rules/`.
