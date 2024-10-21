
###### 2024-10-22 01:01
###### Status:
###### Tags: [[Algorithm]]

# Fibonacci Number (Recursion vs DP)

###  Example: Leetcode 509. Fibonacci Number

> The Fibonacci numbers, commonly denoted `F(n)` form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from `0` and `1`. That is,
> 
> F[0] = 0 as the first number
> 
> F[1] = 1 as our second number
> 
> And the number after that is easy to compute:
> 
> F[n] = F[n-1] + F[n-2]
> 
> **How could we find F[n] with a given n?**
#### [[Recursion]]

```
# Recursion O(2^n), Space O(N)
class Solution(object):
    def fib(self, n):
        if n == 0:
            return(0)
        if n == 1:
            return(1)
        return(self.fib(n-1) + self.fib(n-2))
```
![[1_WnzJmsVLxhXAhjXI9GUYDg.webp]]
#### [[Dynamic Programming]]

```
# DP time complexity O(n),Space O(n)
class Solution(object):
    def fib(self, n):
        if n == 0:
            return(0)
        if n == 1:
            return(1)

        # create empty dp array
        dp = [0] * (n + 1)

        dp[0] = 0
        dp[1] = 1

        for i in range(2,n+1):
            dp[i] = dp[i-1] + dp[i-2]

        return(dp[n])
```
![[1_KeQ9h7cIMS5eI2SydsWT5A.webp]]
# Reference
- https://towardsdatascience.com/dynamic-programming-i-python-8b20387870f5