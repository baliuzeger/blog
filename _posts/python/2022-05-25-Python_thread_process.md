---
layout: post
title: "Thread vs Process"
---

A thread is an execution context, which is all the information a CPU needs to execute a stream of instructions. A process is a bunch of resources associated with a computation, or an executing instance of a program. A process can have one or many threads. Resources are allocated to the processes, and resoueces of different process are not shared with others. To share resources between proecesses, one have to do special handling, e.g. using pipes of queue to share information. All the threads of a process share all its resoureces, e.g. memory.

Threads can perform concurrency but not parallelism, so threads cannot leverage the computing power of multiple CPUs. Processes can perform both concurrency and parallelism, so to leverage the computing powert of multiple CPUs, one should use multi-processing.

## Reference

[Python 浅析线程（threading模块）和进程（process）](https://www.cnblogs.com/wj-1314/p/8263328.html)
