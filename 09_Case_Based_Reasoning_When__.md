# 09 - Case-Based Reasoning

When a cognitive agent addresses new problems by tweaking solutions to previous similar problems.

Lesson Preview:

- Recording cases revisited. 
- Need for case-based reasoning
- Phases of case-based reasoning
- Advanced case-based reasoning

## Recording Cases to Case-Based Reasoning

1. **Retrieval**: Retrieving case from memory similar to the current problem (e.g., kNN result).
2. **Adaptation**: Adapting the solution to that case to fit the current problem.
3. **Evaluation**: Evaluating how well the adapted solution address the current problem.
4. **Storage**: Storing the new problem and solution as a case (encapsulation). 

### Assumptions of Case-Based Reasoning

- Patterns exist in the world.
- Similar problems have similar solutions

One could consider two examples for cases:

1. Navigation from an *office* to a *restaurant*.
2. Data persistence between instances of a program.

We will reference both in the following explanations:

## Case Retrieval

As discussed previously, the process whereby we retrieve existing cases that match some similarity criteria for our specific agent. For example, k Nearest Neighbors (kNN).

For the following sections, we will consider two examples:

- **Example 1**: *Case Retrieval* process returns existing case of navigation from *office* to *doctors*, which is nearby *restaurant*.
- **Example 2**: *Case Retrieval* process (e.g., a programmer's memory) returns existing code for file IO in a Python program.

## Case Adaptation

A slight tweaking of a retrieved case (problem and solution), that allows to solve the present problem.

### by Model of the World

- **Example 1**: Search using a map (the model), to find navigation from *doctor* to *restaurant*.
- **Example 2**: an API for interacting with language: Python's API is likely similar to Java's, and one can leverage the Java API (a model) to translate the implementation from Python to Java.

### by Recursive Reasoning

- **Example 1**: Consider now that one needs to navigate from *home* to *restaurant*. Assuming the previous solution navigating from *office* to *restaurant* was successful, and given I already have an existing case for navigation from *home* to *office*, I can recursively navigate first using the solution from *home* to *office* and then from *office* to *resaurant*.
- **Example 2**: Break apart the need for data persistence into two sub processes, file input and file output. One could leverage existing code for file input, and another implementation for file output.

### by Rules (Heuristics)

Rule's of thumb. For instance, where is downtown? In North America, find the cluster of large buildings and assume this is the city center. Note, this isn't always true and is likely localize.

- **Example 1**: Consider now that one needs to return from *restaurant* to *home*. Assuming the previous solution navigating from  *home* to *resaurant* was successful, a heuristic would be to reverse the solution path.
- **Example 2**:  Efficiency is now a concern for file IO. Adapt existing code for file IO that reads one byte at a time to instead alway read arrays of bytes instead.

## Case Evaluation

In some domains, execution cost can be small (simply doing what the solution proposes), however, other domains, it can be very costly. What then? **Simulation FTW**!

- **Example 1**: trying to return in a car with one way streets
- **Example 2**: executing adapted code to see if it compiles and performs.

## Case Storage

Storing the new problem and solution as a case (Encapsulation is the packing of data and functions into a single component).

- **Example 1**: Indexing multiple navigation route origins, with x and y components. Might also include other parameters like time of route or the route scenery.
- **Example 2**: Store file IO cases based on language, data types, speed, etc.

### Discrimination Tree

A tree structure, where cases are represented in *leaf* nodes. The *root* and all *intermediate* nodes are questions. Can be used also in Case Retrieval operations.

## Advanced Case-Based Reasoning

1. Steps in case-based reasoning don't have to be performed linearly.
2. Storing failed cases can be effective in more quickly finding better solutions
3. Storing all solutions isn't optimal as we need to only store solutions that are novel in their parameter space.

## The Cognitive Connection

Analogical reasoning depends on a spectrum of similarity:

1. On side: problems *identical* to previous problems: simply retrieve solution and apply
2. Other side: problems semantically dissimilar from previous problems: to be discussed later
3. Now: problems which are similar (yet not identical) to previous problems (the most common in human cognition).

### Mapping to Cognitive Architecture

The three components are important because:

1. Reasoning: tweaking existing experience to encounter new problems.
2. Learning: because we need to acquire and store experiences.
3. Memory: because we need to retrieve experiences when needed.