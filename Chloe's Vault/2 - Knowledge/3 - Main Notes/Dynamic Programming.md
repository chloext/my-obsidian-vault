
###### 2024-10-22 00:03
###### Status:
###### Tags: [[Algorithm]] [[Divide and Conquer]]

# Dynamic Programming
Dynamic Programming is a method for designing algorithms.

An algorithm designed with Dynamic Programming divides the problem into subproblems, finds solutions to the subproblems, and puts them together to form a complete solution to the problem we want to solve.
The main idea is to decompose the original question into repeatable patterns and then **store the results as many sub-answers**. Therefore, we **do not have to re-compute** the pre-step answers when needed later.  In terms of big O, this optimisation method generally reduces time complexities from exponential to polynomial.

#### Problems properties
- **Overlapping Subproblems:** can be broken down into smaller subproblems, where the solutions to the subproblems are overlapping (the solution to one subproblem is part of the solution to another subproblem).
- **Optimal Substructure:** complete solution to a problem can be constructed from the solutions of its smaller subproblems so that there is a way to combine the sub solutions to form the complete solution.

#### Steps
1. Check if the the problem has "overlapping subproblems" and an "optimal substructure".
2. Solve the most basic subproblems.
3. Find a way to put the subproblem solutions together to form solutions to new subproblems.
4. Write the algorithm (the step-by-step procedure).
5. Implement the algorithm (test if it works).

#### Common usecase
- [[Shortest Path Algorithems]]
- [[Longest Common Subsequence]]
- [[Knapsack]] 
- Optimal Stock Trading Strategies
- matrix chain multiplication

# Reference
- https://www.w3schools.com/dsa/dsa_ref_dynamic_programming.php#:~:text=Dynamic%20Programming%20is%20a%20method,problem%20we%20want%20to%20solve.
- https://towardsdatascience.com/dynamic-programming-i-python-8b20387870f5
- https://medium.com/@darshanbachhav0/recursion-vs-dynamic-programming-657661c1b96b#:~:text=Approach%3A%20Recursion%20follows%20a%20top,to%20solve%20the%20original%20problem