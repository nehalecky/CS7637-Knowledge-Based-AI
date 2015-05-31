# 05 Means-end Analysis and Problem Reduction

Useful for *well-formed* problems.

Lesson preview:
- State Spaces
- Means-End Analysis 
- Problems Solving with Means-End Analysis
- Problem Reduction

## State Spaces

### The Block Problem

1. You may only move one block at a time.
2. You may only move blocks that have nothing on top of them.

```
Move(C, Table)
Move(B, C)
Move(A, B)
```

### Definition 
Have some sort of *Intial State* to a *Goal State*. From state transitions are performed via valid operations.

Q: How do agents know which operations to perform?

## Means-End Analysis

For each operator that can be applied:

- Apply the current operator to the current state.
- Calculate the difference between the current state and the goal state.
- Prefer the state the minimizes the distance between the new state and goal state.
