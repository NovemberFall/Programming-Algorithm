## Concurrency, Thread Interface(API), Locks

#### Thread VS Process

- Usually, a process has only one thread of control:
  - one set of machine instructions executing at a time
- Some problems are easier to solve when >1 thread of control 
  can operate on different parts of the problem.
  - Example: read a very large file in blocks, 1 thread per block
- Additionally, multiple threads of control can exploit the parallelism 
  possible on multiprocessor systems.
- All threads within a process share the same address space and file descriptors.

- Each thread executes on its own stack in the same process.
- Challenge: Because they can access the same memory, the threads need to 
  synchronize access to shared data among themselves to avoid inconsistencies.
 
---

## Threads and Thread IDs

- Like processes, threads are identified by IDs.
- Thread IDs, however, are local to a process.
- A thread ID from one process has no meaning in another process
- We use thread IDs to refer to specific threads as we manipulate the threads
  within a process.
 
---

## What is a thread

- A new abstraction for <u>a single running process</u>
  - Threads were added to the UNIX System long after the 
    process model was established

- Multi-threaded program
  - A multi-threaded program has more than one point of execution
  - Multiple PCs (Program Counter)
  - They share the same `address space`.


## Threads Context Switch
- Each thread has its own `program counter` and `set of registers`
  - **Thread control blocks(TCBs)** store the state of each thread

- When switching from running one (T1) to running the other (T2)
  - The register state of T1 be saved
  - The register state of T2 restored
  - The address space remains the same.
 
















