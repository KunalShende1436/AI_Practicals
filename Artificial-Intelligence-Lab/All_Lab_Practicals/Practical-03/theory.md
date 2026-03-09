# Theory – Tic Tac Toe with AI Opponent

## Overview
Tic Tac Toe is a turn-based strategy game that serves as a useful exercise for exploring **AI decision-making** and **rule-driven behaviour**. In this implementation, a human player competes against a computer opponent that selects moves using a set of prioritized rules.

The game takes place on a **3×3 board**, and the objective is to align three of the same symbol horizontally, vertically, or diagonally before the opponent does.

---

## Goals of the Practical
- Build a working Tic Tac Toe game in Python
- Implement a **rule-based AI** for the computer player
- Evaluate the board state after every turn
- Demonstrate interaction between a human and an automated agent

---

## Rules of the Game
1. A 3×3 grid serves as the playing field.
2. The human player marks cells with **X**.
3. The AI marks cells with **O**.
4. Turns alternate between the human and the AI.
5. Victory is achieved when three matching symbols appear in any row, column, or diagonal.
6. When every cell is filled without a winner, the match is declared a **draw**.

---

## Board Representation
The board state is stored as a 2D list. A sample mid-game state looks like:
```
-------------
| X | O | X |
-------------
| X | O | X |
-------------
|   | X | O |
-------------
```

Empty cells indicate positions that are still available for play.

---

## AI Decision Rules (Priority Order)
The computer opponent follows this logic on each turn:

1. **Win if possible** – Check if placing O in any open cell leads to a win; if so, take that cell.
2. **Block the opponent** – If the human can win on the next move, occupy that cell to prevent it.
3. **Random fallback** – If neither condition applies, pick any available cell at random.
4. **Draw detection** – If no cells remain and nobody has won, the game ends in a tie.

---

## Step-by-Step Flow
1. Create an empty 3×3 grid.
2. The human places their symbol first.
3. After each placement, check whether the current player has won.
4. On the AI's turn, apply the decision rules to pick the best available cell.
5. Continue alternating turns until a win or draw occurs.
6. Print the final board and announce the outcome.

---

## Benefits
- Straightforward to implement and understand
- Highlights core AI concepts like evaluation and rule priority
- Provides a hands-on example of game-state analysis
- Bridges the gap between human reasoning and automated logic

---

## Practical Relevance
- Foundational concept in game AI development
- Basis for understanding more advanced techniques like Minimax
- Useful for studying human-computer interaction patterns
- Applicable to educational tools and simple decision engines

---

## Summary
This practical shows how a rule-based agent can play Tic Tac Toe competently by evaluating the board after every move and selecting actions based on a fixed priority. It provides a clear illustration of how simple heuristics can drive intelligent-seeming behaviour in games.

