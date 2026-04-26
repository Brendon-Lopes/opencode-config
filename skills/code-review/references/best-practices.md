# Code Review Best Practices

When reviewing code, consider the following areas comprehensively.

## 1. Bugs & Security
-   **Logic Errors**: Are there any off-by-one errors, infinite loops, or incorrect boolean logic?
-   **Race Conditions**: Are shared resources accessed safely in concurrent environments?
-   **Input Validation**: Is all external input validated and sanitized?
-   **Error Handling**: Are errors caught and handled gracefully? Are error messages safe to expose?
-   **Dependencies**: Are new dependencies safe and strictly necessary?

## 2. Architecture & Design
-   **SOLID Principles**: Does the code adhere to Single Responsibility, Open-Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion?
-   **Coupling/Cohesion**: Are modules loosely coupled and highly cohesive?
-   **Reusability**: Is the code designed for reuse where appropriate, or conversely, is it prematurely generalized?
-   **State Management**: Is state localized and immutable where possible?

## 3. Style & Maintainability
-   **Naming Conventions**: Are variables, functions, and classes named clearly and descriptively?
-   **Readability**: Is the code easy to understand? Are complex parts well-commented?
-   **Idiomatic Code**: Does the code follow the conventions of the language and framework being used?
-   **Testability**: Is the new code easily testable? Are there accompanying tests?
-   **Formatting**: Is the formatting consistent? (Rely on linters if available, but flag egregious violations).

## 4. Performance
-   **Complexity**: Are there any unnecessary O(N^2) or worse algorithms?
-   **Memory Usage**: Are large objects held in memory longer than necessary? Are there memory leaks?
-   **Network/IO**: Are database queries or network requests optimized and batched? Is there excessive logging?
