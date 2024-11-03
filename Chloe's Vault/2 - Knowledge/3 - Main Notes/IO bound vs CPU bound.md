
###### 2024-10-31 21:49
###### Status:
###### Tags: [[Optimisation]] [[System Design]]

# IO bound vs CPU bound

- CPU bound task s
	- relies heavily on CPU
	- can go faster if the CPU goes faster
	- eg. math computation, graphics rendering
	- improvement: fast cpu, parallel processing
- I/O bound tasks
	- relies on rated of data transfer going in and out of the system, is more about "waiting"
	- goes faster if I/O systems goes faster
	- eg. downloading data from internet, reading from database
	- improvement: faster I/O devices, [[asynchronous]] processing

# Reference
- 