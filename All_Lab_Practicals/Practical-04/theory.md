# Theory – A* Pathfinding Algorithm

## Overview
A* is an informed search algorithm frequently employed in AI for finding the least-cost path between a source and a target node. It leverages two cost components:
- **g(n)** – the accumulated cost from the source to node n
- **h(n)** – a heuristic estimate of the remaining cost from n to the target

These are combined into a single evaluation function:
**f(n) = g(n) + h(n)**

## Purpose
The goal of this practical is to implement A* search on a weighted graph and trace the shortest route from a given start node to a designated goal node.

## Core Mechanism
A* maintains two collections during execution:
- **Frontier (Open Set)** – nodes that have been discovered but not yet fully processed
- **Explored (Closed Set)** – nodes whose neighbours have already been examined
- **Heuristic function** – provides an admissible estimate of distance to the goal

At each iteration, the node with the smallest f(n) is expanded first.

## Procedure
1. Place the start node into the frontier with g = 0 and f = h(start).
2. Extract the node with the minimum f value from the frontier.
3. If this node is the goal, reconstruct and return the path.
4. Otherwise, examine each of its neighbours.
5. For each neighbour, compute the tentative g cost via the current node.
6. If this cost improves upon the previously recorded g value, update the neighbour's cost and parent pointer, then add it to the frontier.
7. Continue until the goal is reached or the frontier is empty.

## Strengths
- Guaranteed to find the optimal path when using an admissible heuristic
- More efficient than uninformed search methods like BFS or Dijkstra
- Applicable to a wide range of graph and grid-based problems

## Use Cases
- Navigation and route planning
- Autonomous robot pathfinding
- NPC movement in video games
- Network routing and logistics

## Summary
A* blends the completeness of uniform-cost search with the speed of greedy best-first search. By combining actual path cost with heuristic estimation, it explores fewer nodes while still guaranteeing an optimal solution, making it one of the most practical search algorithms in AI.
