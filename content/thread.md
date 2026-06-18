---
title: Thread
---

A thread is the smallest unit of execution inside a process.

A process can contain multiple threads, and each thread can run a different task. Threads in the same process share memory, which makes communication faster but also requires careful synchronization.

A thread allows a program to do multiple tasks at the same time.


## Process vs Thread

A process is the whole running program.
A thread is a worker inside that process.

```text
Process
 ├── Thread 1
 ├── Thread 2
 └── Thread 3
```
