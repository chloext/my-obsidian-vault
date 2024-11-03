
###### 2024-10-31 22:51
###### Status: 
###### Tags: [[Operating Systems]]

# process vs thread
- [[process]]
	- has its own set of variables
- threads
	- share the _same data and system resources_. A multithreaded program must therefore be very careful about the way that threads access and modify data, or else unpredictable behaviour may occur.

#### Python Example
Because of [[Global Interpreter Lock (GIL)]], threading doesn't solve any cpu bound scenarios, but it has multiprocessing libraries to handle those.
For IO bound scenarios on the other hand, because of the nature of sharing data,  multiple threads is great when access to the same resources, such as a database or file system.

# Related pages
- [[Python concurrency - multiprocessing vs multithreading vs asyncio]]

# Reference
- - https://ocw.mit.edu/courses/1-124j-foundations-of-software-engineering-fall-2000/pages/lecture-notes/multithreading/