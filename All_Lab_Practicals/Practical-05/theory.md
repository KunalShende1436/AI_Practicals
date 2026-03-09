# Theory – Cryptarithmetic Puzzle Solver

## Objective
Study and implement an appropriate solving strategy for cryptarithmetic puzzles using Python.

---

## What Are Cryptarithmetic Puzzles?
A cryptarithmetic puzzle presents an arithmetic equation in which each letter stands for a distinct digit (0 through 9). The challenge is to determine the letter-to-digit mapping that makes the equation mathematically correct.

Classic example:

```
  SEND
+ MORE
------
 MONEY
```

No two letters may share the same digit, and the solver must find the unique assignment that satisfies the sum.

---

## Solving Approach – Backtracking
The puzzle is solved through **systematic trial with backtracking**.

This technique works by tentatively assigning a digit to each letter, proceeding forward as long as no conflict arises. When a dead end is encountered (the equation fails or digits are exhausted), the algorithm reverts to the previous assignment and tries the next possibility.

---

## Step-by-Step Process
1. Extract every distinct letter appearing in the puzzle words.
2. Attempt to assign a digit from 0–9 to each letter.
3. Enforce the uniqueness constraint — no digit is assigned to more than one letter.
4. Translate the letter strings into their numeric equivalents.
5. Evaluate whether the resulting numbers satisfy the arithmetic equation.
6. If valid, report the solution; otherwise, backtrack and try alternative assignments.

---

## Worked Example

**SEND + MORE = MONEY**

One valid mapping yields:

| Word  | Numeric Value |
|-------|---------------|
| SEND  | 9567          |
| MORE  | 1085          |
| MONEY | 10652         |

---

## Algorithm Outline
1. Parse the input words (addend 1, addend 2, and sum).
2. Collect all unique characters across the words.
3. Recursively assign digits via backtracking, respecting the uniqueness constraint.
4. After each complete assignment, convert letters to digits and verify the equation.
5. Return the first valid solution or indicate that no solution exists.

---

## Practical Relevance
- Demonstrates constraint satisfaction in AI
- Applies backtracking to a real combinatorial task
- Builds intuition for search-space pruning
- Foundational concept for more advanced solvers (e.g., CSP frameworks)

---

## Summary
This practical shows how backtracking can systematically explore a constrained search space to find the letter-to-digit assignment that satisfies a given arithmetic puzzle. It highlights the interplay between trial, validation, and rollback that underpins many AI problem-solving strategies.
