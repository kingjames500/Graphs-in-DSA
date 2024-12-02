# Graphs in Data Structures and Algorithms (DSA)

## What is a Graph?

A graph is a collection of nodes, also known as vertices, and edges that connect pairs of nodes. Graphs are used to represent various real-world structures such as networks, social connections, and relationships between entities.

## Types of Graphs

### Directed vs Undirected Graphs

- **Directed Graphs**: In a directed graph, edges have a direction. Each edge is represented as an ordered pair of vertices (u, v), meaning there is a path from vertex u to vertex v. Directed graphs are also known as digraphs.

- **Undirected Graphs**: In an undirected graph, edges do not have a direction. Each edge is represented as an unordered pair of vertices {u, v}, meaning there is a path between vertex u and vertex v in both directions.

### Weighted vs Unweighted Graphs

- **Weighted Graphs**: In a weighted graph, each edge has an associated weight or cost. The weight can represent various metrics such as distance, time, or cost. Weighted graphs can be either directed or undirected.

- **Unweighted Graphs**: In an unweighted graph, all edges have the same weight, typically considered as 1. Unweighted graphs can also be either directed or undirected.

### Summary

| Type of Graph       | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| Directed Graph      | Edges have a direction (u, v)                                               |
| Undirected Graph    | Edges do not have a direction {u, v}                                        |
| Weighted Graph      | Edges have associated weights or costs                                      |
| Unweighted Graph    | All edges have the same weight, typically considered as 1                   |




## Dynamic Programming (DP)

Dynamic Programming is a method for solving complex problems by breaking them down into simpler subproblems. It is applicable when the problem can be divided into overlapping subproblems that can be solved independently.

### Key Concepts

- **Optimal Substructure**: A problem exhibits optimal substructure if an optimal solution to the problem contains optimal solutions to its subproblems.
- **Overlapping Subproblems**: A problem has overlapping subproblems if the same subproblems are solved multiple times.

### Steps to Solve a DP Problem

1. **Define the State**: Determine the state variables that represent the subproblems.
2. **State Transition**: Establish the recurrence relation that relates the current state to previous states.
3. **Base Cases**: Identify the base cases and their values.
4. **Compute the Result**: Use the recurrence relation to compute the result iteratively or recursively with memoization.

### Example: Fibonacci Sequence

The Fibonacci sequence is a classic example of a problem that can be solved using dynamic programming.

#### Recursive Approach

```python
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)
```

#### Dynamic Programming Approach

```python
def fibonacci_dp(n):
    if n <= 1:
        return n
    dp = [0] * (n + 1)
    dp[1] = 1
    for i in range(2, n + 1):
        dp[i] = dp[i-1] + dp[i-2]
    return dp[n]
```

### Applications of Dynamic Programming

- **Knapsack Problem**: Determining the maximum value that can be obtained with a given weight capacity.
- **Longest Common Subsequence**: Finding the longest subsequence common to two sequences.
- **Matrix Chain Multiplication**: Determining the most efficient way to multiply a given sequence of matrices.

Dynamic programming is a powerful technique that can significantly reduce the time complexity of problems with overlapping subproblems and optimal substructure.