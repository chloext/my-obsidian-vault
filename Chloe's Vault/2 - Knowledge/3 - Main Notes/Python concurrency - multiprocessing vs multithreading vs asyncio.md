
###### 2024-10-31 21:57
###### Status:
###### Tags: [[Python]] [[Optimisation]] [[Operating Systems]]

# Python multiprocessing vs multithreading vs asyncio

Multiple ways of [[Parallelism]]

|                  | definition                                                                                                                                                      | benefit                                                                                                                                                                | limitation                                                                                                                                              | suited scenarios                                           |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| [[threading]]    | multiple threads of execution run within a single process. Each thread operates independently, allowing the program to perform multiple tasks simultaneously.   | easy _data sharing_ between threads. This can be useful when multiple threads need access to the same resources, such as a database or file system.                    | Because of the [[Global Interpreter Lock (GIL)]], only one thread can execute Python code at a time, making it unsuitable for CPU-bound tasks.          | I/O-bound tasks and data sharing between threads           |
| multiprocessing  | multiple processes run independently of each other, with each process having its _own memory space_. ([[process vs thread]])                                    | Suitable for CPU-bound tasks as it allows the program to take advantage of multiple CPU cores.                                                                         | the difficulty in sharing data between processes due to the lack of shared memory. Starting and stopping processes can be more expensive than  threads. | CPU-bound tasks and taking advantage of multiple CPU cores |
| [[asynchronous]] | a single thread of execution can perform multiple tasks simultaneously. This is achieved using [[coroutines]] and an event loop. ([[cooperative multitasking]]) | ideal for I/O-bound tasks as it allows the program to perform other tasks while waiting for I/O operations to complete, making more efficient use of system resources. | difficult to predict the order in which tasks will be executed due to coroutines’ suspendability at any time.                                           | concurrent I/O-bound tasks                                 |

- CPU Bound => Multi Processing
- I/O Bound, Fast I/O, Limited Number of Connections => Multi Threading
- I/O Bound, Slow I/O, Many connections => Asyncio



# Reference
- https://stackoverflow.com/questions/27435284/multiprocessing-vs-multithreading-vs-asyncio
- https://martinxpn.medium.com/multithreading-vs-multiprocessing-vs-asyncio-in-python-80-100-days-of-python-bf576031a05a
