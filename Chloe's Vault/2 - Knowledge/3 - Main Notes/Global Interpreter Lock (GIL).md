
###### 2024-10-31 22:26
###### Status: 
###### Tags: [[Python]] [[Optimisation]]

# Global Interpreter Lock (GIL)

a mutex (or a lock) that allows only one [thread](https://realpython.com/intro-to-python-threading/) to hold the control of the Python interpreter.

Only one thread can be in a state of execution at any point in time, even in a multi-threaded architecture with more than one CPU core. This means that it can be a performance bottleneck in CPU-bound and multi-threaded code.




(# [What's the point of multithreading in Python if the GIL exists?](https://stackoverflow.com/questions/52507601/whats-the-point-of-multithreading-in-python-if-the-gil-exists))

The GIL **does not** prevent these operations from running in parallel:

1. **IO operations**, such as [sending & receiving network data](https://github.com/python/cpython/blob/cce836296016463032495c6ca739ab469ed13d3c/Modules/socketmodule.c#L926) or [reading/writing to a file](https://github.com/python/cpython/blob/5f55067e238c21de25f09ece9bb24ae8c42d02b4/Python/fileutils.c#L1731).
2. **Heavy builtin CPU bound operations**, such as [hashing](https://github.com/python/cpython/blob/f4c03484da59049eb62a9bf7777b963e2267d187/Modules/hashlib.h#L34) or [compressing](https://github.com/python/cpython/blob/65dd745f1a343dd80f5e612736f36200631f2840/Modules/zlibmodule.c#L376).
3. **Some C extension operations**, such as [numpy calculations](https://github.com/numpy/numpy/blob/d4b2d4f80060285ac085ea874aceaf9fa1bfb757/numpy/core/include/numpy/ndarraytypes.h#L1005).

# Reference
- https://realpython.com/python-gil/