# 04 - Generate and Test

Lesson preview:

- Generate and test method
- Smart Generators
- Smart Testers
- Examples


## Generators and Testers

### Smart Generator

Takes one state, and generates all possible states, however, should not generate states that are not productive. 

### Smart Tester

Analyzes all generated states, and filters to only legal (i.e., those states that adhere to logical constraints) and productive (i.e., resultant states that have not yet been observed) states.

**Note**: For each problem, we have to find the right balance the smartness of generators and testers.


## Generate and Test for Raven's Problems

### Explicity

1. Setup semantic network for A and B, and construct transformation.
2. Apply transformation to C to generate D
3. Compare D to possible solutions and find highest match (via level of confidence).
4. Ensure that D meets a confidence level threshold.
5. If not, repeat 1-4, however using new semantic network construction approach.

### Implicitly

1. Setup semantic network for A and B and constuct transformation
2. Take a solution (1-6) and C and setup semantic network and construct transformation.
3. Compare resultant transformation
4. Repeate for every solution to find best match (via wieghting) 



