# Workflow

- Follow the workflows and conventions of the repository.
- When the task works, refactor the changed code in up to 3 rounds. Stop when a round finds nothing to improve.
- In each round, do these steps:
  1. Make the changed code shorter and easier to read.
  2. Add tests for behavior that has no test.
  3. Run the tests and make sure they pass.
- Skip the rounds when the change has no logic, for example a documentation or configuration change.

## Verify and report
- Run the tests, builds, linters, and other checks that apply.
- Read the final diff. Look for errors, unnecessary complexity, unexpected behavior, and missing tests.
- Make sure that the result satisfies the original requirement, not only that it compiles.
- Never say that a test, benchmark, deployment, or check passed if it did not pass.
- In the final report, tell what changed, why, how you verified it, and which risks remain. Keep verified facts separate from assumptions and untested behavior.
