
###### 2024-10-31 22:50
###### Status: 
###### Tags: [[Optimisation]] [[threading]] [[Operating Systems]]

# Multitasking vs Multithreading
- **[[multitasking]]** refers to when OS runs several *concurrently* at the same CPU. Done by switching from one to other fast enough.
	- _Preemptive multitasking_ : the OS decides how to allocate CPU time slices to each program. At the end of a time slice, the currently active program is _forced_ to yield control to the operating system.
	- _[[cooperative multitasking]]_ : each program controls how much CPU time it needs. This means that a program must cooperate in yielding control to other programs, or else it will hog the CPU.
- **Multithreading** extends the concept of multitasking by allowing individual programs to perform several tasks concurrently. Each task is referred to as a _thread_ and it represents a separate flow of control. 
	- Use-case: a web page is taking too long to load in a web browser, the user should be able interrupt the loading of the page by clicking on the stop button. The user interface can be kept responsive to the user by using a separate thread for the network activity needed to load the page.

# Related pages
- 

# Reference
- - https://ocw.mit.edu/courses/1-124j-foundations-of-software-engineering-fall-2000/pages/lecture-notes/multithreading/