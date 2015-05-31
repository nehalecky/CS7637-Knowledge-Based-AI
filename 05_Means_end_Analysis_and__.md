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

*Note*: as a general method, means-end can be applied to a varied range of problems. Due to it generality, it can however, get caught in local minima and cannot converge to the global solution.

### Problem Reduction

Take the goal of a problem and break it apart into more simple goals. Apply means-end after.

## Summary
We learned about two additional methods for problem solving, means-ends analysis and problem reduction. Means-end takes advantage of optimizing navigation through problem state space, by electing minima differences between state spaces and goal state. Problem reduction leverages the same navigation, however, by achieving smaller much simpler goals that collectively allow for achieving the goal state. Also, we were presented some application of the methods to Raven's progressive matrices. Finally, the differences between weak methods and strong methods was discussed.
