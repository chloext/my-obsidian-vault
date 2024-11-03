
###### 2024-11-04 00:12
###### Status: 
###### Tags: [[Operating Systems]] 

# Forking
**fork** is an operation whereby a [process](https://en.wikipedia.org/wiki/Computer_process "Computer process") creates a copy of itself.

In [[multitasking]] operating systems, [[process]]es (running programs) need a way to create new processes, e.g. to run other programs. Fork and its variants are typically the only way of doing so in Unix-like systems. 
For a process to start the execution of a different program, it first forks to create a copy of itself. Then, the copy, called the "[child process](https://en.wikipedia.org/wiki/Child_process "Child process")", calls the [exec](https://en.wikipedia.org/wiki/Exec_(system_call)) system call to overlay itself with the other program: it ceases execution of its former program in favour of the other.


# Related pages
- 

# Reference
- https://en.wikipedia.org/wiki/Fork_(system_call)#:~:text=In%20computing%2C%20particularly%20in%20the,and%20Single%20UNIX%20Specification%20standards.