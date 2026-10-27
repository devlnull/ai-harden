# Testing

- Use Test-Driven Development when it fits: write a test, write the code, then refactor.
- Test observable behavior and business invariants, not implementation details.
- Select the correct mix of unit, integration, contract, and end-to-end tests.
- Test edge cases, invalid inputs, concurrency, retries, and failures in proportion to the risk of the change.
- Write deterministic tests with clear assertions. Do not depend on timing or on shared external state.
- Use mocks only at real boundaries. Do not copy the implementation logic into the test.
- Do not weaken, delete, or skip a valid test to make a change pass.
- When you fix a defect, add a regression test.
