# Global Rules

## Language
- The user has B2 English skills. Use simple English.
- Do not use advanced words, idioms, slang, or phrasal verbs that are hard to understand.
- Use ASD-STE100 (Simplified Technical English) for all communication: chat replies, questions, summaries, plans, commit messages, merge request text, and documents. Use short sentences, one idea per sentence, active voice, simple present tense, and the same word for the same thing.

## Code
- Never write comments in code. No inline comments, block comments, docstrings, or JSDoc. Code should be self-explanatory through naming and structure.
- Write the smallest amount of code that solves the task. Do not add code that nobody needs.
- Least code, most impact. Each change must touch the fewest lines and files that give the full result.
- Before you edit, find the one place that controls the behavior (the source, the shared helper, the config, the root cause). Change that place, not every caller.
- Do not edit many files to apply one change when a change in fewer files gives the same result.
- If the correct fix must touch many files, tell the user why before you start.
- Do not rename, move, or reformat code that the task does not need.

## Git
- Never add Co-Authored-By lines or any Claude attribution to commit messages or pull request descriptions.
- Make micro-commits. Each commit has one meaning.
- Group changes by meaning, not by file.
- If one action changes many files, make one commit for all these files.
- If one action changes only one file, make one commit for that file.
- Do not put two different actions in one commit.

## Workflow
- Use Test-Driven Development when it fits: write a test, write the code, then refactor.
- When the task works, do not stop. Do 3 refactor rounds first.
- In each round, do these steps:
  1. Refactor the changed code like a professional software engineer.
  2. Make the code shorter and easier to read.
  3. Add or improve tests to increase test coverage.
  4. Run the tests and make sure they pass.
- Report the task as complete only after the 3 rounds.
