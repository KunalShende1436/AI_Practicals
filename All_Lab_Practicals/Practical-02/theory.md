# Theory – Water Jug Puzzle

## Overview
The Water Jug Puzzle is a well-known AI problem that showcases how **state-space exploration** and **rule-based transitions** can be applied to reach a desired configuration. Two containers with different volumes are used, and the task is to arrive at a specific quantity of water through a limited set of allowed actions.

## Problem Setup
Consider the following scenario:
- Container A with a capacity of 4 litres
- Container B with a capacity of 3 litres
- An infinite water source is available
- Neither container has measurement markings

The goal is to measure **exactly 2 litres** in Container A.

## Representing States
Every configuration is expressed as a tuple:
**(a, b)**

Where:
- a = current volume in Container A
- b = current volume in Container B

Starting configuration: **(0, 0)**

Desired configuration: **(2, 0)**

## Allowed Operations (Transition Rules)
The following operations define how one state transitions to another:

1. Completely fill Container A
2. Completely fill Container B
3. Drain Container A entirely
4. Drain Container B entirely
5. Transfer water from A into B (until B is full or A is empty)
6. Transfer water from B into A (until A is full or B is empty)

Applying these rules generates new states from the current one.

## Search Strategy – BFS
The puzzle is tackled using **Breadth-First Search**:
1. Begin at the starting configuration.
2. At each step, apply every valid operation to generate successor states.
3. Track already-visited states to prevent loops.
4. Expand states level by level until the target is found.
5. Output the path from initial to goal state.

## Summary
This practical demonstrates how a logical problem can be modeled as a graph of states and solved via systematic exploration. BFS guarantees finding the shortest sequence of operations to reach the desired water measurement.
