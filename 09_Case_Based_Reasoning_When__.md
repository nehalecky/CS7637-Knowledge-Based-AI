# 09 - Case-Based Reasoning

When a cognitive agent addresses new problems by tweaking solutions to previous similar problems.

Lesson Preview:

- Recording cases revisited. 
- Need for case-based reasoning
- Phases of case-based reasoning
- Advanced case-based reasoning

## Recording Cases to Case-Based Reasoning

1. **Retrieval**: Retriving case from memory similar to the current problem (e.g., kNN result).
2. **Adaptation**: Adpating the solution to that case to fit the current problem.
3. **Evaluation**: Evalutating how well the adapted solution address the current problem.
4. **Storage**: Storing the new problem and solution as a case (encapsulation). 

### Assumptions of Case-Based Reasoning

- Patterns exist in the world.
- Similar problems have similar solutions

One could consider two examples for cases:

1. Navigation from an *office* to a *restuarant*.
2. Data persistence between instances of a program.

We will reference both in the following explanations:

## Case Retrevial

As discussed previously, the process whereby we retrieve existing cases that match some similarity criteria for our specific agent. For example, k Nearest Neighbors (kNN).

For the following sections, we will consider two examples:

- **Example 1**: *Case Retrieval* process returns existing case of navigation from *office* to *doctors*, which is nearby *restuarant*.
- **Example 2**: *Case Retrieval* process (e.g., a programmer's memory) returns existing code for file IO in a Python program.

## Case Adaptation

A slight tweaking of a retrieved case (problem and solution), that allows to solve the present problem.

### by Model of the World

- **Example 1**: Search using a map (the model), to find navigation from *doctor* to *resturant*.
- **Example 2**: an API for interacting with language: Python's API is likely similar to Java's, and one can leverage the Java API (a model) to translate the implementation from Python to Java.

### by Recursive Reasoning

- **Example 1**: Consider now that one needs to navigate from *home* to *resaurant*. Assuming the previous solution navigating from *office* to *restaurant* was successful, and given I already have an existing case for navigation from *home* to *office*, I can recursively navigate first using the solution from *home* to *office* and then from *office* to *resaurant*.
- **Example 2**: Break apart the need for data persistence into two sub processes, file input and file output. One could leverage existing code for file input, and another implemention for file output.

### by Rules (Hueristics)


## Case Evalutation


- 