
###### 2024-10-22 01:33
###### Status:
###### Tags: [[Dynamic Programming]]

# Maximum Subarray Sum – Kadane’s Algorithm

Given an integer array `nums`, find the subarray with the largest sum, and return _its sum_.

**Example 1:**
```
**Input:** nums = [-2,1,-3,4,-1,2,1,-5,4]
**Output:** 6
**Explanation:** The subarray [4,-1,2,1] has the largest sum 6.
```

#### DP Steps
1. Check if the the problem has "overlapping subproblems" and an "optimal substructure".
2. Solve the most basic subproblems.
3. Find a way to put the subproblem solutions together to form solutions to new subproblems.
4. Write the algorithm (the step-by-step procedure).
5. Implement the algorithm (test if it works).

# Reference
- https://leetcode.com/problems/maximum-subarray/description/
- https://www.geeksforgeeks.org/largest-sum-contiguous-subarray/