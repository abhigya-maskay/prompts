## Step 1: Generate Test Plan

1. **Analyze Target File:** Copilot reads the target source code file completely to identify all functions, methods, classes, dependencies, and business logic flows.

2. **Identify Test Cases:**
   * **Happy Path Tests:** Test each function with valid inputs and verify expected outputs
   * **Edge Cases:** Test boundary values, empty inputs, invalid data types, and malformed inputs
   * **Error Scenarios:** Test network failures, database errors, permission issues, and timeout scenarios
   * **Integration Points:** Test component interactions, data flow, callbacks, and event handling

3. **Plan Test Data Strategy:**
   * Check for existing factory files in `test/`, `spec/`, or `__tests__/` directories
   * Plan minimal valid objects, edge case data sets, and invalid data scenarios
   * Use existing factory methods when available

4. **Determine Mock Strategy:**
   * Identify external dependencies that need mocking (APIs, databases, file I/O, third-party services)
   * Plan mocks for internal dependencies not under test

5. **Create Test Plan Document:** Generate a comprehensive markdown file documenting all test cases, data requirements, and mock strategies.

6. **User Checkpoint:** Present the test plan to the user for review and confirmation before proceeding to implementation.
