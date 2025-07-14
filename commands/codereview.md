---
description: "Systematic code review tool that enforces methodical, multi-dimensional analysis with step-by-step investigation workflow"
---

SYSTEMATIC CODE REVIEW SESSION

Code to review: "$ARGUMENTS"

**REVIEW METHODOLOGY:**
You will conduct a comprehensive, systematic code review using a structured investigation workflow. This process requires methodical analysis across multiple dimensions with evidence gathering at each step.

**STEP 1 - INITIAL PLANNING & SCOPE ASSESSMENT:**
Begin with systematic planning:

- **Scope Definition**: What code components, files, or modules need review?
- **Review Type Selection**: Is this a full review, security-focused, performance-focused, or architectural review?
- **Context Gathering**: What is the purpose and function of this code? What problem does it solve?
- **Technology Stack**: What languages, frameworks, and dependencies are involved?
- **Review Priorities**: Based on the code's purpose, what are the most critical aspects to examine?

**INVESTIGATION PAUSE**: Gather concrete evidence before proceeding. Do not make assumptions.

**STEP 2 - STRUCTURAL ANALYSIS:**
Examine the overall code structure and organization:

- **Architecture Patterns**: What design patterns are used? Are they appropriate for the problem domain?
- **Module Organization**: How is the code organized? Is the structure logical and maintainable?
- **Dependency Management**: How are dependencies handled? Any circular dependencies or tight coupling?
- **Interface Design**: Are APIs and interfaces well-designed and consistent?
- **Separation of Concerns**: Is functionality properly separated and organized?

**EVIDENCE GATHERING**: Document specific examples of structural strengths and weaknesses.

**STEP 3 - SECURITY VULNERABILITY ASSESSMENT:**
Conduct thorough security analysis:

- **Input Validation**: How is user input validated and sanitized?
- **Authentication & Authorization**: Are access controls properly implemented?
- **Data Protection**: How is sensitive data handled, stored, and transmitted?
- **Injection Attacks**: Are there vulnerabilities to SQL injection, XSS, or other injection attacks?
- **Error Handling**: Does error handling expose sensitive information?
- **Dependency Vulnerabilities**: Are there known vulnerabilities in dependencies?

**SEVERITY CLASSIFICATION**: Classify findings as Critical, High, Medium, or Low severity.

**STEP 4 - PERFORMANCE & EFFICIENCY ANALYSIS:**
Examine performance characteristics:

- **Algorithmic Complexity**: Are algorithms efficient for expected data sizes?
- **Resource Management**: How are memory, connections, and other resources managed?
- **Bottlenecks**: Are there obvious performance bottlenecks or inefficiencies?
- **Scalability**: Will the code scale appropriately under load?
- **Caching & Optimization**: Are appropriate caching and optimization strategies used?

**STEP 5 - CODE QUALITY & MAINTAINABILITY:**
Assess code quality and long-term maintainability:

- **Readability**: Is the code clear, well-commented, and self-documenting?
- **Testing Coverage**: What testing strategies are used? Is coverage adequate?
- **Error Handling**: Is error handling comprehensive and appropriate?
- **Code Duplication**: Is there unnecessary code duplication?
- **Standards Compliance**: Does the code follow established coding standards and best practices?
- **Documentation**: Is the code adequately documented for future maintainers?

**STEP 6 - DETAILED EXAMINATION:**
Dive deep into specific areas of concern:

- **Critical Functions**: Examine the most important or complex functions in detail
- **Edge Cases**: How does the code handle edge cases and error conditions?
- **State Management**: How is application state managed and mutated?
- **Concurrency**: If applicable, how are concurrency and threading handled?
- **External Integrations**: How does the code interact with external systems or APIs?

**VERIFICATION PAUSE**: Cross-reference findings and validate concerns with concrete evidence.

**STEP 7 - FINAL ASSESSMENT & RECOMMENDATIONS:**
Synthesize findings into actionable recommendations:

**SUMMARY OF FINDINGS:**
- **Critical Issues**: List any critical security or functionality issues requiring immediate attention
- **High Priority**: Important issues that should be addressed soon
- **Medium Priority**: Issues that should be addressed in upcoming development cycles
- **Low Priority**: Minor improvements and optimizations

**POSITIVE PATTERNS:**
- Identify well-implemented patterns and good practices
- Highlight code that demonstrates quality and maintainability

**ACTIONABLE RECOMMENDATIONS:**
- Specific, concrete steps to address identified issues
- Prioritized list of improvements
- Suggestions for refactoring or architectural improvements

**CONFIDENCE ASSESSMENT:**
- Rate confidence level in findings (High/Medium/Low)
- Identify areas that may need additional investigation
- Note any limitations in the review scope

**REVIEW QUALITY ASSURANCE:**
Before concluding, ensure your review:
- Provides concrete evidence for all findings
- Covers all requested review dimensions
- Offers actionable, specific recommendations
- Maintains objectivity and focuses on code quality
- Identifies both problems and strengths

Present findings in a structured format with clear severity levels and actionable next steps.