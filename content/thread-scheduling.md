---
title: Thread Scheduling
---

## What is Thread Scheduling?

Thread scheduling is the process of deciding the order in which threads use the CPU.

Since multiple threads may be ready to run at the same time, the operating system needs a scheduling policy to decide which thread gets CPU time first, how long it runs, and when another thread should run.

---

## Types of Thread Scheduling

### 1. Preemptive Scheduling

Preemptive scheduling is a scheduling method where the operating system can forcibly stop the currently running thread and assign the CPU to another thread.

In this method, a thread does not necessarily run until it finishes. Instead, the operating system may interrupt it depending on the scheduling policy.

Examples of preemptive scheduling policies include:

* Round Robin
* Priority-Based Scheduling
* Shortest Job First

#### Advantages

Preemptive scheduling allows the CPU to be shared more dynamically among multiple threads. This can improve responsiveness and make the system feel faster, especially when many threads are running.

#### Disadvantages

Because threads may be switched frequently, context switching costs occur. A context switch takes time because the system must save the current thread's state and load another thread's state.

---

### 2. Non-Preemptive Scheduling

Non-preemptive scheduling is a scheduling method where once a thread gets the CPU, it continues using the CPU until it finishes or voluntarily gives up control.

In this method, the operating system does not forcibly interrupt the running thread.

#### Advantages

Non-preemptive scheduling is simpler to implement and does not cause frequent context switching costs.

#### Disadvantages

It may be difficult to use the CPU efficiently when multiple threads are waiting. If one thread runs for a long time, other threads may have to wait for a long time before they can execute.

---

## Thread States

### 1. New / Ready State

This is the state where a thread has been created and allocated in memory. The thread is ready to use the CPU, but it has not been assigned CPU time yet.

### 2. Running State

This is the state where a thread is currently using the CPU.

### 3. Not Runnable State

This is the state where a thread exists in memory but cannot currently use the CPU.

### 4. Dead / Terminated State

This is the state where a thread has finished its execution and is no longer active.

Related: [[Thread]]