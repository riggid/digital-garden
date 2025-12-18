---
{"dg-publish":true,"permalink":"/semester-1/python/unit-1/pyqs/"}
---


# Previous Year Questions (PYQs)

# [[Semester 1/Python/Python\|Back]]
***
[[Semester 1/Python/Unit 1/Core Notes\|Core Notes]] | [[Semester 1/Python/Unit 1/Questions\|Questions]] | [[Semester 1/Python/Unit 1/pyqs\|PYQs]] | [[Semester 1/Python/Unit 1/mcqs\|MCQs]]
***

## 📝 Selected Previous Year Questions with Solutions

### Problem Solving & Python Basics

### 1. Translator Systems
**Question:** Differentiate between an Interpreter and a Compiler. Why is Python considered an interpreted language?

**Answer:**
-   **Compiler**: Translates the entire code into machine code (binary) at once before execution. Faster execution. Errors shown after compilation. (e.g., C, C++).
-   **Interpreter**: Translates code line-by-line during execution. Slower execution. Stops at first error. Easier debugging. (e.g., Python, Ruby).
-   **Python**: It is interpreted because the source code (.py) is compiled to bytecode (.pyc) which is then interpreted by the Python Virtual Machine (PVM) line-by-line.

### 2. Errors
**Question:** Define 'Logical Error' and 'Syntax Error' with appropriate examples.

**Answer:**
-   **Syntax Error**: Violation of the grammar rules of the programming language. The parser detects this before execution.
    -   *Example*: `print("Hello"` (Missing parenthesis).
-   **Logical Error**: The program runs without crashing but produces incorrect results due to flawed logic (Bug).
    -   *Example*: Calculating average as `sum / n * 100` instead of `sum / n`.

### 3. Data Types
**Question:** Discuss the difference between immutable and mutable data types in Python. Give examples of each.

**Answer:**
-   **Mutable**: The value of the object **can be changed** after it is created.
    -   *Examples*: `list`, `dictionary`, `set`.
    -   `L = [1, 2]; L[0] = 5` (Allowed).
-   **Immutable**: The value of the object **cannot be changed** after it is created. Any "change" creates a new object.
    -   *Examples*: `int`, `float`, `string`, `tuple`.
    -   `S = "Hello"; S[0] = "h"` (Error).

---

*Last updated: December 2025*
