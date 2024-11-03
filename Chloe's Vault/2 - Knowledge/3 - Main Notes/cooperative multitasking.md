
###### 2024-10-31 22:33
###### Status: 
###### Tags: [[Optimisation]] [[Parallelism]]

# Cooperative multitasking
**[[multitasking]]** refers to when OS runs several *concurrently* at the same CPU. Done by switching from one to other fast enough.

_[[cooperative multitasking]]_ : each program controls how much CPU time it needs. This means that a program must cooperate in yielding control to other programs, or else it will hog the CPU.

# Related Pages
- Example: Asyncio in [[Python]]
- [[multitasking vs multithreading]]

# Reference
- - - https://ocw.mit.edu/courses/1-124j-foundations-of-software-engineering-fall-2000/pages/lecture-notes/multithreading/