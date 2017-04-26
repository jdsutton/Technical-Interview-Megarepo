# Operating Systems

## Udacity, Introduction to Operating Systems - Notes
[Course Homepage](https://www.udacity.com/course/introduction-to-operating-systems--ud923)

1. [Course Overview](https://docs.google.com/document/d/1NHgibsFIYxuzP6F-MUfdp7960ryAcPkuZmwCSgiys5A/pub)
2. [OS Introduction](https://docs.google.com/document/d/1ArRpNXkm4q2-OBP9RWjT5LhYdC0TwLwKnUqSNhL9JVE/pub)
3. [Processes and Process Management](https://docs.google.com/document/d/1egz8qH27XD6c4QYzd9akeO_0e-AvlCjzLkfZQfsn_nE/pub)
4. [Threads and Concurrency](https://docs.google.com/document/d/1LKAnbB42pv-bpr3QhqHgELdGkE7FUwSSWSozAP4DoDo/pub)

## Textbooks
* Operating System Concepts
* Operating System Concepts: Essentials
* Modern Operating Systems
* [Operating Systems: Three Easy Pieces](http://pages.cs.wisc.edu/~remzi/OSTEP/) (free from the authors)

## Vocabulary
* https://quizlet.com/9875856/operating-system-concepts-ch-1-flash-cards/

## Papers
* [An Introduction to Programming with Threads](https://s3.amazonaws.com/content.udacity-data.com/courses/ud923/references/ud923-birrell-paper.pdf)

## Articles
* [Grok the GIL: How to write fast and thread-safe Python](https://opensource.com/article/17/4/grok-gil)

## System Calls
* Requests to the kernel to perform some privileged operation
* "A system call is the programmatic way in which a computer program requests a service from the kernel of the operating system it is executed on. This may include hardware-related services (for example, accessing a hard disk drive), creation and execution of new processes, and communication with integral kernel services such as process scheduling. System calls provide an essential interface between a process and the operating system." [[Wikipedia - System Call](https://en.wikipedia.org/wiki/System_call)]
* On x86, it is usually performed using the `int` instruction, which generates a software trap, switching the processor to "ring-0" (allows priveleged instructions).
    * Linux uses `int 0x80`
* Most platforms wrap these system calls in standard libraries, such as libc on \*nix systems.

## Processes and Threads
* "A process is an instance of a computer program that is being executed. It contains the program code and its current activity. Depending on the operating system (OS), a process may be made up of multiple threads of execution that execute instructions concurrently" [[Wikipedia - Process](https://en.wikipedia.org/wiki/Process_(computing))].
* "A thread of execution is the smallest sequence of programmed instructions that can be managed independently by a scheduler, which is typically a part of the operating system." [[Wikipedia - Thread](https://en.wikipedia.org/wiki/Thread_(computing))]
* Often, threads of the same process share the same address space and system resources.

## IPC
[Interprocess Communication](http://advancedlinuxprogramming.com/alp-folder/alp-ch05-ipc.pdf)

## Concurrency
* "Concurrent computing is a form of computing in which several computations are executing during overlapping time periods—concurrently—instead of sequentially (one completing before the next starts)." [[Wikipedia - Concurrent Computing](https://en.wikipedia.org/wiki/Concurrent_computing)]
* The most common sources of concurrency are multiprocessing and multithreading.
* Concurrency can significantly improve performance because multiple computations are happening at the same time.
* Unfortunately, concurrency can be a source of nondeterministic bugs that are hard to find or debug.
* Concurrency control primitives, such as locks, are used to ensure that use of common resources by multiple threads or processes is done correctly. Several concurrency control primitives are described below.

### Lock/Mutex
* [University of Wisconson - Locks](http://pages.cs.wisc.edu/~remzi/OSTEP/threads-locks.pdf)
* "A lock or mutex (from mutual exclusion) is a synchronization mechanism for enforcing limits on access to a resource in an environment where there are many threads of execution. A lock is designed to enforce a mutual exclusion concurrency control policy." [[Wikiepedia - Lock](https://en.wikipedia.org/wiki/Lock_(computer_science))]

### Semaphores
* "A semaphore is a variable or abstract data type that is used for controlling access, by multiple processes, to a common resource in a concurrent system such as a multiprogramming operating system." [[Wikipedia - Semaphore](https://en.wikipedia.org/wiki/Semaphore_(programming))]
* "A semaphore is hardware or a software tag variable whose value indicates the status of a common resource. Its purpose is to lock the resource being used" [[CareerRide - Semaphore](http://www.careerride.com/OS-semaphore.aspx)]
* A simple implementation is to have an atomic counter in memory (e.g. using atomic compare and swap assembly instructions provided by most modern architectures).
    * The counter begins at some initially value X, signifying that X threads can use the resource at a time.
    * When a thread requests the resource, the counter is decremented.
    * If the counter is greater than 0, the thread can proceed. Otherwise, it blocks until the counter becomes greater than 0.
    * When a thread releases the resource, the counter is incremented.
* A semaphore in which X=1 is a mutex since only one thread can use the resource at a time.

### Monitors
* [Wikipedia - Monitor](https://en.wikipedia.org/wiki/Monitor_(synchronization))
* "In concurrent programming, a monitor is a synchronization construct that allows threads to have both mutual exclusion and the ability to wait (block) for a certain condition to become true. Monitors also have a mechanism for signalling other threads that their condition has been met. "

### Deadlock, Livelock
* In concurrent programs, there may be executions (resulting from bugs) in which threads cease to make progress. Deadlock and livelock are two such cases.

#### Deadlock
![deadlock](http://cse.csusb.edu/tongyu/courses/cs660/images/deadlock/lock.gif)

* Deadlock usually occur in the context of locks.
* A deadlock occurs when two processes become mutually dependent. That is, process A cannot make progress until B finishes, and B cannot make progress until A finishes.
* For example, process A locks access to the printer and tries to get access to file `foo.txt`, which it wants to print. Meanwhile, process B locks access to the file and then tries to get access to the printer. Imagine the following sequence of events:
   * A locks printer
   * B locks file
   * A attempts to lock file, but blocks because B has already locked it
   * B attempts to lock printer, but blocks because A has already locked it
* How to avoid deadlock
  * Careful design: if all threads acquire locks in the same order, they cannot deadlock. In the example above, if A and B try to lock the file first, neither can deadlock, though one may block temporarily.
  * Detection schemes: Some systems, such as database systems, try to detect deadlocks when they happen. Then, they kill one of the processes deadlocking and release its resources so the others can proceed.
  * Dependency graphs can be constructed by representing each thread as a node. If A needs a resource that B has currently, a directed edge is drawn from A to B. If this graph has a cycle the processes in the cycle are deadlocked.
 
#### Livelock
![livelock](https://image.slidesharecdn.com/29-deadlocks-sp082-111116105142-phpapp02/95/deadlocks-in-operating-system-31-638.jpg?cb=1422635342)

* A livelock occurs when two processes continually change state but do not make progress.
* For example,
   * A locks printer
   * B locks file
   * A attempts to lock file, but cannot because B has already locked it
   * B attempts to lock printer, but blocks because A has already locked it
   * A releases the printer and waits for the file to be unlocked
   * B releases the file and waits for the printer to be unlocked
   * A notices that the file is unlocked and tries again
   * B notices that the printer is unlocked and tries again
   * Repeat forever
* How to avoid livelock
  * Variable timeouts
