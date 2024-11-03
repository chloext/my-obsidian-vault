
###### 2024-10-31 22:02
###### Status:
###### Tags: [[Optimisation]]

# threading

**Multithreading** extends the concept of [[multitasking]] by allowing individual programs to perform several tasks concurrently. Each task is referred to as a _thread_ and it represents a separate flow of control. 

Threads share the _same data and system resources_. A multithreaded program must therefore be very careful about the way that threads access and modify data, or else unpredictable behaviour may occur.

##### Example
A web page is taking too long to load in a web browser, the user should be able interrupt the loading of the page by clicking on the stop button. The user interface can be kept responsive to the user by using a separate thread for the network activity needed to load the page.

# Related pages
- [[Multitasking vs Multithreading]]
- [[process vs thread]]
- Python example: [[Python concurrency - multiprocessing vs multithreading vs asyncio]]

# Reference
- https://ocw.mit.edu/courses/1-124j-foundations-of-software-engineering-fall-2000/pages/lecture-notes/multithreading/