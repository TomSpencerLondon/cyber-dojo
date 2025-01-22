# Learning Test-Driven Development (TDD) with Cyber Dojo

Test-Driven Development (TDD) is a disciplined approach to programming that emphasizes writing tests before writing the actual implementation. By practicing TDD, developers can ensure their code is reliable, maintainable, and aligned with requirements. Recently, I had the opportunity to use [Cyber Dojo](https://beta.cyber-dojo.org/), a collaborative platform for coding challenges, to learn TDD by solving the classic FizzBuzz problem. Here's what I learned and why Cyber Dojo is a useful tool for honing programming skills.

## Problem Statement: FizzBuzz
FizzBuzz is a well-known programming exercise often used in coding interviews and practice sessions. The task is straightforward:
- Print numbers from 1 to 100.
- Replace multiples of 3 with "Fizz."
- Replace multiples of 5 with "Buzz."
- Replace multiples of both 3 and 5 with "FizzBuzz."

In this case, I started small and focused on generating results for numbers 1 to 5 to build the implementation iteratively. You can view the specific problem I worked on [here](https://beta.cyber-dojo.org/kata/edit/SaLDwW).

## Implementing FizzBuzz
The core logic for FizzBuzz was encapsulated in a `FizzBuzz` class, which included a `result()` method. Here’s the high-level overview:

1. **Code Implementation**:
    - Created a `FizzBuzz` class with a `result()` method that generated a list of results for numbers 1 to 5.
    - Used conditional logic to determine whether to append "Fizz," "Buzz," "FizzBuzz," or the number itself as a string.

2. **Incremental Testing**:
    - Started with simple tests for smaller ranges, ensuring correctness before expanding the functionality.

```java
for (int i = 1; i <= 5; i++) {
    if (i % 5 == 0 && i % 3 == 0) {
        result.add("FizzBuzz");
    } else if (i % 5 == 0) {
        result.add("Buzz");
    } else if (i % 3 == 0) {
        result.add("Fizz");
    } else {
        result.add("" + i);
    }
}
```

## Writing and Running Tests
Tests were written using JUnit, the default Java testing library. Three test cases were created to validate the functionality:

1. **oneToThree**:
    - Validated results for numbers 1 to 3.
    - Expected output: `["1", "2", "Fizz"]`.

2. **oneToFive**:
    - Expanded the range to 1 to 5.
    - Expected output: `["1", "2", "Fizz", "4", "Buzz"]`.

3. **oneToFifteen**:
    - Designed to test numbers 1 to 15, but initially failed due to incomplete range logic in the implementation.
    - This failure highlighted the need to refactor the `FizzBuzz` class to accommodate larger ranges.

## Key Observations
1. **Test Failures Are Insightful**:
    - The initial implementation was limited to numbers 1 to 5. Tests for broader ranges failed, revealing gaps in the logic.
    - Iterative debugging using JUnit assertions helped refine the implementation.

2. **Incremental Learning**:
    - Starting with small, testable pieces of functionality made the learning process manageable.
    - Expanding functionality and re-running tests reinforced the principles of TDD.

## Why Cyber Dojo is a Great Learning Tool
Cyber Dojo stands out as an effective platform for learning TDD and programming for several reasons:

1. **Interactive Environment**:
    - Offers a controlled and distraction-free space for solving coding challenges.
    - Provides immediate feedback through integrated testing frameworks.

2. **Promotes TDD Practices**:
    - Encourages writing tests first, fostering a disciplined approach to coding.
    - Helps developers internalize the importance of verifying functionality.

3. **Facilitates Debugging**:
    - Detailed error messages highlight discrepancies between expected and actual results, making debugging more efficient.

4. **Supports Iterative Development**:
    - Allows incremental improvements, encouraging continuous testing and refinement.

5. **Accessible and Collaborative**:
    - Ideal for individual practice or pair programming.
    - Its simplicity makes it suitable for beginners and experienced developers alike.

## Conclusion
Cyber Dojo provided a structured and interactive environment to practice TDD with the FizzBuzz challenge. The platform's focus on testing, debugging, and iterative learning made it an useful tool for sharpening programming skills. For developers looking to master TDD or enhance their problem-solving abilities, Cyber Dojo is good resource to explore.

