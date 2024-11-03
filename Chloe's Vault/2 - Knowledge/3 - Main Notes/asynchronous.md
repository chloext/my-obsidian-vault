
###### 2024-10-25 12:46
###### Status:
###### Tags: [[Parallelism]]

# asynchrony

process/occurrence of events independent of the main program flow
- events: may be outside events like signal, or actions started by a function that take place _concurrently_ with the main program, **without the function hanging to wait for the result**


- __synchronous__ 
	- tasks execute in consecutive order, must finish previous to start next
- __asynchronous__ 
	- tasks can be executed in any order even concurrently. you may a long-run task while being able to execute other tasks, without having to wait for that task to finish.

Asynchronous programming is a technique where a single thread of execution can perform multiple tasks simultaneously.


# Related pages
- threading vs asynchrony: [[Python concurrency - multiprocessing vs multithreading vs asyncio]]

# Reference
- https://en.wikipedia.org/wiki/Asynchrony_(computer_programming)

