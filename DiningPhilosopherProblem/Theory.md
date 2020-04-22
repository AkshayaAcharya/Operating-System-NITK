## INTRODUCTION<br>

 In Multitasking Operating system multiple processes can be executed simultaneously and it has ability to preempt the currently running process. In order to execute multiple processes parallelly, OS should provide mechanism for Inter Process Communication(IPC). Lack of synchronization in IPC causes the problems like Inconsistency, Data loss, Deadlock.

 These synchronization problems really occur because of:
* **Critical Section**: Critical section is that part of the program where shared resources are accessed and non-critical section is that part of the program which does not access any shared resource. Program may have series of critical and non-critical sections.
* **Race Condition**: Processes must be racing to access the Critical section and the end result will depend on the order in which the processes finish their updates.
* **Preemption**: Running process will be suspended/preempted and another process will be scheduled on CPU.

**Deadlock - Waiting Forever Problem**:

 Deadlock is a situation where a process is waiting for getting access to a resource which is already allocated to some other process and that other process is waiting for resource whose access is held by first process. At this situation both the processes will prevent each other from getting access to the resource they want hence resulting in a deadlock where none of the process can complete execution.

Consider P1 and P2 are two processes. P1 requests for resource R1 and acquires it, P2 request for resource R2 and acquires it.
For further execution P1 need resource R2 for execution and P2 need resource R1 for execution.

<center>
  <img src="images/deadlock.png" height="253" width="250">
</center>

At such a situation, both the processes will wait until resource is set free. They will remain in wait state for ever and hence leading to a deadlock.

To proceed, operating system won't understand what action to take. Only way is to abort or stop one or more processes which will release the resource, which results in complete the execution of remaining processes releasing all the resources so that the first process can complete its execution.

 **Following are necessary conditions that will hold if there is deadlock**:
  * **Mutual Exclusion**: Resources are non-sharable. At a time only one process can use resource.
  * **Hold and Wait**: Process holds a at least one resource and waits for a resource held by another process.
  * **Non Preemption**: Process does not release the resource.
  * **Circular Wait**: A set of processes are waiting for a resource held by each other in circular form.

**Following are the strategies of handling deadlock**:
  * **Deadlock Avoidance and prevention**: Do not let the system go in deadlock. [Popular algo is Banker's Algo.]
  * **Detection and Recovery**: Let deadlock occur, then do preemption or abort the processes to handle it if occurred. [Doctor's Algorithm]
  * **Deadlock Ignorance**: If deadlock is very rare, then let it happen and reboot the system if it occurs. This is the approach used in today's operating systems like Windows and Linux. [Ostrich Algorithm].

**Dining Philosopher's Problem**:
  Dinning Philosopher problem is an example that is normally considered when considering about deadlock.
  <center>
  <img src="images/philosopher.png">
  </center>
1. Five philosophers sit around a round table with bowls of spaghettis and forks are placed between each pair of adjacent philosophers.<br>
2. Each philosopher can be in either of two states: Thinking and Eating.<br>
3. When a philosopher wants to eat, he uses two chopsticks.<br>
4. When a philosopher wants to think, he keeps down both the chopsticks.<br>
5. Infinite supply and infinite demand is assumed.<br>
6. It must be ensured that no philosopher will starve. If all the philosophers wants to eat at same time, due to unavailability of chopsticks all of them will not be able to eat together and this leads to a situation called 'Deadlock'.<br><br>

**Following are the possible solutions for Dining philosopher's Problem**:
1. A philosopher is allowed to eat by picking up left chopstick first and then the right chopstick.
  <code>

     do{
       wait(chopsticks[i]);
       wait(chopsticks[(i+1)%5]);

       //Critical section
       eat

       signal(chopsticks[i]);
       signal(chopsticks[(i+1)%5]);

       think
     }while(true);
  </code>

  Problem with above solution is that if all five philosophers become hungry at same time then they pick up their left chopstick first which will make all chopstick value to 0 hence they will wait forever for the right chopstick. If any two philosophers are faster in both eating and thinking, then all the only these two philosophers will occupy forks.

  <center>
  <img src="images/solution1.png">
</center>


2. Every philosopher allowed to pick left chopstick first then right accept one who is allowed to pick right chopstick first then left.

<center>
<table style="text-align:center;padding:10px;width:650px;">
<tr>
	<th style="text-align:center;width:150px;">Lefty</th>
	<th style="text-align:center">Righty</th>
</tr>
<tr>
  <td style="text-align:justify">
    <code>

     do{
       wait(chopsticks[i]);
       wait(chopsticks[(i+1)%5]);

       //Critical section
       eat

       signal(chopsticks[i]);
       signal(chopsticks[(i+1)%5]);

       think
     }while(true);
  </code>
  </td>
  <td style="text-align:justify">
    <code>

     do{
       wait(chopsticks[(i+1)%5]);
       wait(chopsticks[i]);

       //Critical section
       eat

       signal(chopsticks[(i+1)%5]);
       signal(chopsticks[i]);

       think
     }while(true);
  </code>
  </td>
</tr>
</table>













<!-- 3. Each fork can be held by only one philosopher and a philosopher can use another fork only if it is not being used by another philosopher.<br>
4. A philosopher can eat spaghettis when they have both left and right forks.<br>
5. After an individual philosopher finishes eating, they need to put down both forks so that forks can be used by others.<br>
6. Infinite supply and infinite demand is assumed.<br> -->
