Banker’s algorithm
------------------Pretest part------------------------
Banker’s algorithm is a Deadlock______
Avoidance and prevention algorithm
Detection algorithm
Ignorance algorithm
Recovery algorithm

Modern operating systems knows how many resources process will require in order to complete its execution.
True
False
Some OS knows but most of them does not know the resource requirement of every process.
None

What problem is solved by Dijkstra banker’s algorithm?
Cache coherence
Mutual exclusion
Deadlock recovery
Deadlock avoidance

Which of the following condition is required for deadlock to be possible?
Mutual exclusion
A process may hold allocated resources while awaiting assignment of other resources
No resource can be forcibly removed from a process holding it
All of the mentioned

For non sharable resources like a printer, mutual exclusion :
Must exist
Must not exist
May exist
None

------------------post-test-----------------------
What is the drawback of banker’s algorithm?
In advance processes rarely know that how much resource they will need
The number of processes changes as time progresses
Resource once available can disappear
All of the mentioned

System is in safe state if _____
It is possible for all processes to finish executing
The system can allocate resources to each process in some order and still avoid a deadlock
Both a and b
None

If system is in safe state then deadlock cannot occur for any sequence of process execution.
True
False

Safe sequence is ____________
Sequence of processes whose execution does not causes deadlock
Sequence of processes whose execution may cause deadlock
Sequence in which execution of processes is going to happen
Both a & c

Unsafe state is state in which______
Processor cannot serve any process because of heavy load
Deadlock may occur while execution
It is not possible for processes to finish executing in any order
None




Deadlock
-------------------------Pretest---------------------------------
The methods for dealing with the deadlock problem is
Use of  protocol to make sure that the system never enters in to the deadlock state
Allow the system to enter a deadlock state and then recover
Ignore the problem and pretend that deadlock never occurred in system. The UNIX OS uses this solution.
All of these

Deadlock is a situation in which
No process can complete its execution
Few processes cannot complete their execution
Processes waits for longer time than usual time to complete its execution
None

With single resource, deadlock occurs
If there are more than two processes competing for that resources
If there are only two processes competing for that resources
If there is a single process competing for that resources
None of these

The request and release of resources are ___________
Command line statements
Interrupts
System calls
Special programs

Which one of the following is a visual way to determine the deadlock occurrence?
Resource allocation graph
Starvation graph
Inversion graph
None

The dining – philosophers problem will occur in case of :
5 philosophers and 5 chopsticks
4 philosophers and 5 chopsticks
3 philosophers and 5 chopsticks
6 philosophers and 5 chopsticks

------------Post test-----------------
A system has 3 process sharing 4 resources. If each process need max of 2 units then
Deadlock can never occur
Deadlock may occur
Deadlock may not occur
None

A system has 6 identical resources and N processes competing for them. Each process can request at most 2 resources. Which one of the following values of N could lead to a deadlock?
5
6
7
None

What is the minimum number of resources required to ensure that deadlock will never occur, if there are currently three processes P1, P2 and P3 running in a system whose maximum demand for the resources of same type are 3, 4, and 5 respectively.
3
7
9
10

Which of the following is not a necessary condition for deadlock?
Mutual exclusion
Reentrancy
Hold and wait
No pre-emption
Solution: Necessary conditions for Deadlock: Mutual Exclusion, No pre-emption, Hold and Wait, Circular wait

For a deadlock to arise, which of the following conditions must hold simultaneously ?
Mutual exclusion
No preemption
Hold and wait
All of above

A solution to the Dining Philosophers Problem which avoids deadlock is:
Ensure that all philosophers pick up the left fork before the right fork
Ensure that all philosophers pick up the right fork before the left fork
Ensure that one particular philosopher picks up the left fork before the right fork, and that all other philosophers pick up the right fork before the left fork
None

A deadlock free solution to the dining philosophers problem :
Necessarily eliminates the possibility of starvation
Does not necessarily eliminate the possibility of starvation
Eliminates any possibility of any kind of problem further
None





Forking
-------------------pretest-----------------------
Fork is
The creation of a new job
the dispatching of a task
increasing the priority of a task
the creation of a new process

Fork is a ___?
System call that is used to create a new process in Windows OS
System call that is used by Unix like OS to create new process
System call that is used by both Unix and Windows OS to create new process
C function used to create new function in any OS

System call are executed in _____
User mode
Kernel mode
User mode as well as kernel mode
None

A fork system call will fail if :
The previously executed statement is also a fork call
The limit on the maximum number of processes in the system would be executed
The limit on the minimum number of processes that can be under execution by a single user would be executed
All of above

Fork ____?
Creates a process which cannot have another program loaded into it
A new process which is not a child of parent process
Creates a duplicate of the parent process
All of above

------Post test--------------------
How many new processes are created if n consecutive fork statements are executed?
2^n
(2^n)-1
2^(n-1)
N+1

A process executes the code:
fork();
fork();
fork();
The total number of child processes created is
3
4
7
8

The following C program
main()
{
    fork() ;
    fork() ;
    printf ("yes");
}
If we execute this core segment, how many times the string yes will be printed ?
1
2
4
8

In UNIX, the return value for the fork system call is _____ for the child process and _____ for the parent process.
A Negative integer, Zero
Zero, A Negative integer
Zero, A nonzero integer
A nonzero integer, Zero

Fork system call returns negative value
In child process if process creation is successful.
In parent process if fork fails to create a new process
Fork always returns 0 or positive integer which is a pid of newly created process
None

The following program:
main()
   {
      if(fork()>0)
      sleep(100);
   }
results in the creation of:
An orphan process
A zombie process
A process that executes forever
None

Interrupt:
--------------pretest-------------------
A processor needs software interrupt to
test the interrupt system of the processor
implement coroutines
obtain system services which need execution of privileged instructions
return from subroutine

Interrupts form an important part of _____ systems.
Batch processing
Multitasking
Real-time processing
Multi-user
Explanation: This forms an important part of the Real time system since if a process arrives with greater priority then it raises an interrupt and the other process is stopped and the interrupt will be serviced.

An interrupt that can be temporarily ignored is
Vectored interrupt
Non-maskable interrupt
Maskable interrupt
High priority interrupt
Explanation: The maskable interrupts are usually low priority interrupts which can be ignored if a higher priority process is being executed.

The return address from the interrupt-service routine is stored on the
System heap
Processor register
Processor stack
Memory
Explanation: The Processor after servicing the interrupts as to load the address of the previous process and this address is stored in the stack.

The time between the receiver of an interrupt and its service is ______
Interrupt latency
Cycle time
Switching time
None

-------------post test-------------
A computer handles several interrupt sources of which the following are relevant for this question.
Interrupt from CPU temperature sensor (raises interrupt if CPU temperature is too high)
Interrupt from Mouse(raises interrupt if the mouse is moved or a button is pressed)
Interrupt from Keyboard(raises interrupt when a key is pressed or released)
Interrupt from Hard Disk(raises interrupt when a disk read is completed)
Which one of these will be handled at the HIGHEST priority?
Interrupt from Hard Disk
Interrupt from Mouse
Interrupt from Keyboard
Interrupt from CPU temperature sensor

The signal sent to the device from the processor to the device after receiving an interrupt is
Interrupt-acknowledge
Return signal
Service signal
Permission signal
The Processor upon receiving the interrupt should let the device know that its request is received.

CPU as two modes privileged and non-privileged. In order to change the mode from privileged to non-privileged
A hardware interrupt is needed
A software interrupt is needed
Either hardware or software interrupt is needed
A non-privileged instruction (which does not generate an interrupt)is needed
A software interrupt by some program which needs some CPU service, at that time the two modes can be interchanged.

Which table handle stores the addresses of the interrupt handling subroutines?
Interrupt-vector table
Vector table
Symbol link table
None

A single Interrupt line can be used to service n different devices?
True
False

When an interrupt occurs, an operating system
ignores the interrupt
always changes state of interrupted process after processing the interrupt
always resumes execution of interrupted process after processing the interrupt
may change state of interrupted process to ‘blocked’ and schedule another process.
Page Replacement Algo:
----------pretest-----------------
Increasing the RAM of a computer typically improves performance because:
Virtual Memory increases
Larger RAMs are faster
Fewer page faults occur
Fewer segmentation faults occur

Thrashing
reduces page I/O
decreases the degree of multiprogramming
implies excessive page I/O
improve the system performance

A memory page containing a heavily used variable that was initialized very early and is in constant use is removed then
LRU page replacement algorithm is used
FIFO page replacement algorithm is used
LFU page replacement algorithm is used
None of the above

If no frames are free, _____ page transfer(s) is/are required.
One
Two
Three
Four

The aim of creating page replacement algorithms is to :
Replace pages faster
Increase the page fault rate
Decrease the page fault rate
To allocate multiple pages to processes

---------------Post test-------------------
Which of the following page replacement algorithms suffers from Belady’s anomaly?
Optimal replacement
LRU
FIFO
Both (A) and (C)
--All FIFO based algorithms suffers from Belady's anomaly

In which one of the following page replacement algorithms it is possible for the page fault rate to increase even when the number of allocated frames increases?
LRU (Least Recently Used)
OPT (Optimal Page Replacement)
MRU (Most Recently Used)
FIFO (First In First Out)

The optimal page replacement algorithm will select the page that
Has not been used for the longest time in the past
Will not be used for the longest time in the future
Has been used least number of times
Has been used most number of times    

A process, has been allocated 3 page frames. Assume that none of the pages of the process are available in the memory initially. The process makes the following sequence of page references (reference string): 1, 2, 1, 3, 7, 4, 5, 6, 3, 1
If optimal page replacement policy is used, how many page faults occur for the above reference string?
7
8
9
10

Assume that there are 3 page frames which are initially empty. If the page reference string is 1, 2, 3, 4, 2, 1, 5, 3, 2, 4, 6 the number of page faults using the optimal replacement policy is__________.
6
7
8
9

Optimal page replacement algorithm is difficult to implement, because _____
It requires a lot of information
It requires future knowledge of the reference string
It is too complex
It is extremely expensive

Applying the LRU page replacement to the following reference string : 1 2 4 5 2 1 2 4
The main memory can accommodate 3 pages and it already has pages 1 and 2. Page 1 came in before page 2.
How many page faults will occur ?
2
3
4    
5

The reason for using the Least Frequently Used page replacement algorithm is :
An actively used page should have a large reference count
A less used page has more chances to be used again
It is extremely efficient and optimal
All of above



Producer Consumer
---------pre test------------
A critical section is a program segment
which should run in a certain amount of time
which avoids deadlocks
where shared resources are accessed
which must be enclosed by a pair of semaphore operations

The bounded buffer problem is also known as :
Readers Writers problem
Dining Philosophers problem
Producer Consumer problem
None of above

Which process can be affected by other processes which are executing in the system?
Cooperating process
Child process
Parent process
Init process

A counting semaphore was initialized to 10. Then 6P (wait) operations and 4V (signal) operations were completed on this semaphore. The resulting value of the semaphore is
0
8
10
12

Producer consumer problem can be solved using semaphore.
True
False

----------Post test---------------

Inter process communication :
Allows processes to communicate and synchronize their actions when using the same address space
Allows processes to communicate and synchronize their actions without using the same address space
Allows the processes to only synchronize their actions without communication
None of the above

Binary semaphore maintains list of waiting processes. This list is mostly queue data structure. Binary semaphore defines two operations, down (P) and up (V) also called wait and signal. If the value of Binary semaphore is 0, that means
There is no process in waiting queue
There can be one or more processes in waiting queue
There can be zero or more process in waiting queue
 None

Let m[0]....m[4] be mutexes (binary semaphores) and P[0].......P[4] be processes. Suppose each process P[i] executes the following:
wait (m[i]);
wait (m(i+1) mod 4]);
...........
release (m[i]);
release (m(i+1) mod 4]);

This could cause___
Thrashing
Deadlock
Starvation, but not deadlock
None of the above

Which data structure is used to hold the items in producer consumer problem
Stack
Queue
List
Tree

Producer consumer problem without any synchronization mechanism suffers from
Data Loss/Inconsistency
Starvation
Deadlock
None




Scheduling Algo
-------------------pre test-----------
A CPU scheduling algorithm determines an order for the execution of its scheduled processes. Given 'n' processes to be scheduled on one processor, how many possible different schedules are there?
N
n^2
n!
2^n

The state of a process after it encounters an I/O instruction is
Ready
blocked
Idle
running

Which scheduler is responsible for scheduling process on CPU?
Short term scheduler
Medium term scheduler
Long term scheduler
None

Which of the following scheduling algorithms gives minimum average waiting time ?
FCFS
SJF
Round robin
Priority

Dispatcher is concerned with :
Assigning ready processes to CPU
Assigning ready processes to waiting queue
Assigning running processes to blocked queue
All of above

----------------Post test----------------

If the time-slice used in the round-robin scheduling policy is more than the maximum time required to execute any process, then the policy will
degenerate to shortest job first
degenerate to priority scheduling
degenerate to first come first serve
none of the above

Suppose a system contains n processes and system uses the round-robin algorithm for CPU scheduling then which data structure is best suited for ready queue of the process
Stack
Queue
circular queue
tree    

A starvation free job scheduling policy guarantees that no job indefinitely waits for a service. Which of the following job scheduling policies is starvation free?
Priority queuing
Shortest Job First
Youngest Job First
Round robin

The performance of Round Robin algorithm depends heavily on
size of the process
the I/O bursts of the process
the CPU bursts of the process
the size of the time quantum
Note: In round robin algorithm, the size of time quanta plays a very important role as: If size of quanta is too small: Context switches will increase and it is counted as the waste time, so CPU utilization will decrease. If size of quanta is too large: Larger time quanta will lead to Round robin regenerated into FCFS scheduling algorithm.

Starvation is not possible in _____.
FCFS scheduling
Priority based scheduling
SJF scheduling
Round Robin scheduling

Aging is used to
Reduce the waiting time of process
Avoid deadlock
Reduce scheduling time
Reduce context switching time

In aging, priority of the process will increase _____
If process waits longer
If burst time of process is short
If priority of process is low
Aging does not increase priority of process

Which of the following are not preemptive based scheduling algorithm
SRTF
SJF
Round Robin
None

The optimal scheduling algorithm is ________
FCFC
SJF
Round Robin
None


System Call
-----------pre test-------------------
System calls are executed in user mode
True
False

Which of the following is not a valid Unix system call
fork()
exit()
close()
console()

User can run some privileged instructions in user mode
True
False

When system boots up, it always starts in ____________.
User mode
Kernel mode
kernel mode only if safe boot is selected
None

Which of the following is false.
System call are used to obtain the services from operating system
System calls are executed in kernel mode
System calls can be invoked through user program
All of above

------------------post test-------------------------

open(), read(), write() functions are file management related system calls in Unix
True
False

System calls are usually invoked by using
A software interrupt
Polling
An indirect jump
A privileged instruction

Which of the following system calls does not return control to the calling point, on termination ?
Fork
Exec
Ioctl
Longjmp

Which of the following calls never returns an error ?
getpid
fork
exec
open

If a thread invokes the exec system call,
Only the exec executes as a separate process.
The program specified in the parameter to exec will replace the entire process
The exec is ignored as it is invoked by a thread.
None

If exec is called immediately after forking,
The program specified in the parameter to exec will replace the entire process
All the threads will be duplicated
All the threads may be duplicated
None

If a process does not call exec after forking,
The program specified in the parameter to exec will replace the entire process
All the threads should be duplicated
All the threads should not be duplicated
None
