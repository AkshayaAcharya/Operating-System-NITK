INTRODUCTION

One of the strategies to handle deadlock is Deadlock Avoidance, in which the request for any resource will be granted if the resulting state of the system doesn't cause deadlock in the system. The state of the system will continuously be checked for safe and unsafe states.

Banker's Algorithm is mainly used for deadlock avoidance. Implementation of the algorithm is as follows: Ref[1]

Let 'n' be the number of processes and 'm' be the number of resource types in the system.

1. Allocation:
    * Is a 2D array of size 'n*m' representing how many instances of each resource is allocated to each the process.
    * Allocation[ i, j ] = k means process Pi is currently allocated ‘k’ instances of resource type R<sub>j</sub>
2. Maximum:
    * Is a 2D array of size 'n*m' representing maximum demand of each process for resources in the system.
    * Maximum[ i, j ] = k means process Pi may request at most ‘k’ instances of resource type R<sub>j</sub>
3. Need:
    * Is a 2D array of size 'n*m' representing number of resources of each type currently allocated to processes.
    * Allocation[ i, j ] = k means process Pi is currently allocated with ‘k’ instances of resource type R<sub>j</sub>
4. Available:
    * Is a 1D array representing number of available resources of each type
    * Available[ j ] = k means there are ‘k’ instances of resource type R<sub>j</sub>



The algorithm for finding out whether or not a system is in a safe state can be described as follows:

    1) Let Work and Finish be vectors of length ‘m’ and ‘n’ respectively.
    Initialize: Work = Available
    Finish[i] = false; for i=1, 2, 3, 4….n

    2) Find an i such that both
    a) Finish[i] = false
    b) Needi <= Work
    if no such i exists goto step (4)

    3) Work = Work + Allocation[i]
    Finish[i] = true
    goto step (2)

    4) if Finish [i] = true for all i
    then the system is in a safe state

Resource-Request Algorithm

Let Requesti be the request array for process Pi. Requesti [j] = k means process Pi wants k instances of resource type R<sub>j</sub>. When a request for resources is made by process Pi, the following actions are taken:

    1) If Requesti <= Needi
    Goto step (2) ; otherwise, raise an error condition, since the process has exceeded its maximum claim.

    2) If Requesti <= Available
    Goto step (3); otherwise, Pi must wait, since the resources are not available.

    3) Have the system pretend to have allocated the requested resources to process Pi by modifying the state as
    follows:
    Available = Available – Requesti
    Allocationi = Allocationi + Requesti
    Needi = Needi– Requesti
