# Theory – Alpha-Beta Pruning in Game Trees

## Objective
Implement alpha-beta pruning to optimize the minimax decision process for two-player games.

---

## Background
Alpha-beta pruning is an enhancement to the standard **minimax algorithm** that skips the evaluation of subtrees which cannot influence the final outcome. By doing so, it significantly cuts down the number of nodes the algorithm needs to inspect, allowing the search to go deeper within the same time budget.

---

## The Minimax Framework
Minimax applies to adversarial two-player scenarios:

- The **maximizing player** aims to achieve the highest possible score.
- The **minimizing player** aims to achieve the lowest possible score.

The algorithm recursively evaluates every reachable game state and propagates scores upward, with each layer alternating between maximization and minimization.

---

## How Alpha-Beta Pruning Works
Two running bounds are maintained throughout the search:

**Alpha (α)** – the highest score the maximizing player can secure on the path so far.

**Beta (β)** – the lowest score the minimizing player can secure on the path so far.

At any node, if the condition **α ≥ β** holds, the remaining children of that node are **pruned** — they cannot yield a better result for either player, so exploring them is unnecessary.

---

## Benefits
- Dramatically reduces the number of evaluated nodes compared to plain minimax
- Enables searching deeper levels of the game tree
- Produces the same optimal result as full minimax
- Standard technique in competitive game AI

---

## Where It's Applied
- Chess and Go engines
- Tic Tac Toe solvers
- Checkers and Othello programs
- General adversarial decision-making systems

---

## Summary
Alpha-beta pruning preserves the correctness of minimax while eliminating redundant computation. It achieves this by tracking upper and lower score bounds and discarding branches that fall outside these bounds, resulting in faster and more scalable game-tree evaluation.