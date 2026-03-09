

# Theory – Magic Square Generation

## What is a Magic Square?

A Magic Square is an n × n grid filled with distinct positive integers (1 to n²) such that the sum along every row, every column, and both principal diagonals yields the same value. This fixed sum is referred to as the **Magic Constant**.

These squares have significance in areas like recreational mathematics, AI-based pattern recognition, and combinatorial problem-solving.

## Computing the Magic Constant

For a square of order n, the magic constant M can be derived as:

**M = n(n² + 1) / 2**

For instance, when n = 3:

M = 3 × (9 + 1) / 2 = 15

## How It Works – The Siamese Technique

This approach is applicable exclusively for odd-order squares and follows a diagonal placement strategy:

1. Begin by placing 1 at the center column of the topmost row.
2. For each subsequent number, move one cell upward and one cell to the right.
3. If moving outside the grid boundary, wrap to the opposite edge.
4. If the target cell is already occupied, drop down one row from the previous position instead.
5. Continue this process until all n² values have been assigned.

## Steps in the Algorithm

1. Allocate a 2D matrix of dimensions n × n, initialized to zero.
2. Set the starting cell to the center of the top row.
3. Sequentially assign values from 1 through n² following the Siamese placement rules.
4. Handle wrap-around and collision cases at each step.
5. Output the completed magic square along with the magic constant.

## Where It's Used

- Logical reasoning tasks in AI
- Matrix-based algorithm design exercises
- Number theory and mathematical puzzles
- Teaching algorithmic thinking and iteration control

## Summary

This practical illustrates how structured rules can be used to fill a grid such that all directional sums remain equal. The Siamese method provides an elegant and efficient approach for constructing odd-order magic squares in Python.
