# Code

- Never write comments in code. No inline comments, block comments, docstrings, or JSDoc. Code should be self-explanatory through naming and structure.
- Write the smallest amount of code that solves the task. Do not add code that nobody needs.
- Least code, most impact. Each change must touch the fewest lines and files that give the full result.
- Before you edit, find the one place that controls the behavior (the source, the shared helper, the config, the root cause). Change that place, not every caller.
- Do not edit many files to apply one change when a change in fewer files gives the same result.
- If the correct fix must touch many files, tell the user why before you start.
- Do not rename, move, or reformat code that the task does not need.
