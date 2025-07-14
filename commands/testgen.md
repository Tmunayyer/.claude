---
description: "Systematic test generation tool that enforces methodical investigation and comprehensive test design through structured workflow"
---

SYSTEMATIC TEST GENERATION SESSION

Code to generate tests for: "$ARGUMENTS"

**TEST GENERATION METHODOLOGY:**
You will conduct comprehensive test generation using a systematic investigation workflow. This process requires methodical examination with confidence-building progression through multiple investigation steps.

**SCOPE SPECIFICATION REQUIREMENT:**
BE SPECIFIC about scope: Target specific functions, classes, or modules rather than entire applications. Identify the exact components that need test coverage.

**STEP 1 - INITIAL CODE INVESTIGATION:**
Begin with systematic code examination:

- **Scope Definition**: What specific functions, classes, or modules are we generating tests for?
- **Framework Detection**: What testing framework should be used? (Jest, pytest, JUnit, etc.)
- **Code Complexity Assessment**: How complex is the code? Simple functions, standard modules, or critical systems?
- **Dependency Analysis**: What dependencies and external systems does the code interact with?
- **Existing Test Coverage**: What tests already exist? What gaps need to be filled?

**CONFIDENCE LEVEL**: Exploring → Building Understanding

**MANDATORY INVESTIGATION PAUSE**: Examine the actual code structure and behavior before proceeding.

**STEP 2 - CRITICAL PATH & BEHAVIOR ANALYSIS:**
Identify core behaviors and critical execution paths:

- **Public API Surface**: What are the public methods, functions, and interfaces that need testing?
- **Critical Business Logic**: What business rules and algorithms are implemented?
- **Data Flow Paths**: How does data move through the functions? What transformations occur?
- **State Management**: How does the code manage and mutate state?
- **Integration Points**: What external systems, APIs, or services does the code interact with?
- **Complex Algorithms**: What algorithms or calculations need verification?

**CONFIDENCE LEVEL**: Building Understanding → Gaining Clarity

**STEP 3 - EDGE CASE & BOUNDARY CONDITION IDENTIFICATION:**
Systematically identify edge cases and boundary conditions:

- **Input Boundaries**: What are the minimum, maximum, and boundary values for inputs?
- **Error Conditions**: What error states and exception scenarios can occur?
- **Null/Empty Cases**: How does the code handle null, undefined, empty, or missing values?
- **Type Boundaries**: What happens with different data types or invalid type inputs?
- **Size Limitations**: How does the code behave with very large or very small datasets?
- **Concurrent Access**: If applicable, what race conditions or concurrency issues exist?

**CONFIDENCE LEVEL**: Gaining Clarity → Becoming Confident

**STEP 4 - FAILURE MODE & ERROR SCENARIO ANALYSIS:**
Examine potential failure modes and error scenarios:

- **Exception Handling**: What exceptions can be thrown and how should they be tested?
- **Network Failures**: How should network timeouts, connectivity issues be handled?
- **Resource Exhaustion**: What happens when memory, disk, or other resources are exhausted?
- **Invalid State**: What happens when the system is in an invalid or unexpected state?
- **Security Boundaries**: What security-related failure modes need testing?
- **Performance Degradation**: What performance edge cases should be tested?

**STEP 5 - TEST DESIGN PATTERN SELECTION:**
Choose appropriate test design patterns:

- **Unit Tests**: Pure function testing with isolated dependencies
- **Integration Tests**: Testing interactions between components
- **Mock Strategy**: What dependencies should be mocked vs. tested with real implementations?
- **Test Data Strategy**: What test data fixtures and factories are needed?
- **Parameterized Tests**: What scenarios benefit from parameterized test approaches?
- **Property-Based Testing**: What properties can be tested with generated inputs?

**CONFIDENCE LEVEL**: Becoming Confident → Certain

**VERIFICATION PAUSE**: Cross-reference test scenarios with code paths to ensure comprehensive coverage.

**STEP 6 - COMPREHENSIVE TEST SUITE GENERATION:**
Generate the complete test suite with systematic coverage:

**SUCCESS CASE TESTS:**
- Happy path scenarios with valid inputs
- Typical use cases and workflows
- Expected return values and state changes

**EDGE CASE TESTS:**
- Boundary value testing
- Empty/null input handling
- Maximum and minimum value scenarios

**ERROR CASE TESTS:**
- Invalid input handling
- Exception scenario testing
- Error recovery and cleanup

**INTEGRATION TESTS:**
- External dependency interactions
- API integration scenarios
- Database interaction tests (if applicable)

**PERFORMANCE TESTS (if applicable):**
- Load testing for critical functions
- Performance regression detection
- Resource usage validation

**TEST IMPLEMENTATION REQUIREMENTS:**
For each test, provide:
- **Clear Test Names**: Descriptive names that explain what is being tested
- **Arrange-Act-Assert Structure**: Well-structured test organization
- **Proper Mocking**: Appropriate isolation of dependencies
- **Assertion Strategy**: Comprehensive assertions covering all important outcomes
- **Test Data**: Realistic and varied test data scenarios

**COVERAGE VALIDATION:**
Before concluding, ensure your test suite:
- Covers all public API methods and functions
- Tests both success and failure scenarios
- Includes appropriate edge cases and boundary conditions
- Uses the correct testing framework and patterns for the codebase
- Provides clear, maintainable test code
- Includes setup and teardown as needed

**EXPERT VALIDATION:**
- Are there additional test scenarios that should be considered?
- Does the test suite adequately cover the critical business logic?
- Are the test patterns appropriate for the codebase?
- Is the test coverage comprehensive without being excessive?

Present the generated tests with clear organization, proper documentation, and comprehensive coverage of the specified code components.