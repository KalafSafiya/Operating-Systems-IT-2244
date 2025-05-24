# Summary of Process Creation Practicals Using `fork()` in C

This set of practical exercises demonstrates key concepts of process creation and management in Unix-like operating systems using the `fork()` system call in the C programming language.

---

## Practical Overview

1. **Simple Fork and PID Identification**  
   The first practical explores how a single call to `fork()` creates a child process. It shows how the parent and child processes receive different return values from `fork()`, enabling them to identify themselves and print their respective process IDs.

2. **Fork with Basic Output and PID Display**  
   The second practical extends the first by printing a message ("Hello World") and then using `fork()` to create a child process. Both parent and child print their process IDs and the fork return value to illustrate how process creation affects program output and process identity.

3. **Parent with Two Child Processes (Sibling Processes)**  
   The third practical uses two consecutive `fork()` calls from the original parent to create two child (sibling) processes. Each process prints its own process ID and its parent’s process ID to clearly demonstrate the process hierarchy and sibling relationships.

---

## Key Concepts Learned

- **Process Creation:** Using `fork()` to spawn new processes, which duplicate the calling process.
- **Process Identification:** Using `getpid()` and `getppid()` system calls to retrieve the current process ID and its parent’s process ID, respectively.
- **Process Hierarchy:** Understanding how parent, child, and sibling processes are related.
- **Concurrency and Scheduling:** Observing that process execution order is nondeterministic due to operating system scheduling.
- **Return Values of `fork()`:** Interpreting the return value of `fork()` to distinguish between parent (positive PID) and child (zero) processes.

---

## Overall Summary

Through these practicals, we gain hands-on understanding of how operating systems manage multiple processes, how processes are created and identified, and how process relationships form a hierarchy. These fundamentals are essential for learning about multitasking, process control, and inter-process communication in systems programming.
