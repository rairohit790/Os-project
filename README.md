# Os-project
Consider a scheduling approach which is non pre-emptive similar to shortest job next in nature. The priority of each job is dependent on its estimated run time, and also the amount of time it has spent waiting. Jobs gain higher priority the longer they wait, which prevents indefinite postponement. The jobs that have spent a long time waiting compete against those estimated to have short run times. The priority can be computed as : Priority = 1+ Waiting time / Estimated run time Write a program to implement such an algorithm.

1.	Description: 

In priority scheduling if we have higher prior4ity with a very large burst time then other process which have less burst time had to wait for a very large time this is called starving.
Solution The priority is updated at the regular interval according to the waiting time and burst time so no process should starve.
Stravation or indefinite blocking is phenomenon associated with the Priority scheduling algorithms, in which a process ready to run for CPU can wait indefinitely because of low priority. In heavily loaded computer system, a steady stream of higher-priority processes can prevent a low-priority process from ever getting the CPU.
Solution to starvation:
Aging is a technique of gradually increasing the priority of processes that wait in the system for a long time.For example, if priority range from 127(low) to 0(high), we could increase the priority of a waiting process by 1 Every 15 minutes. Eventually even a process with an initial priority of 127 would take no more than 32 hours for priority 127 process to age to a priority-0 process.

2.	Algorithm for the solution

0->Take the input of no process and burst time of each process.
1->As the question is regarding priority scheduling so we would assing all the process with same priority i.e, 1
2->First process would execute which have the least burst time as it is also dependent on shortest job first scheduling non premptive scheduling(sorting complexity is (n^2) bubble sort)
3->Update waiting time, new priority, turn-around-time, completion time of each of the rest process.
4->Sort the remaining non executed process according to the highest priority.
5->Repeat line 3 until all the process had been executed.

3.	Boundary condition:

We have taken the array size of 100 so we can implement this coded for maximum 100 process.


4.

This must follow the non premptive concept no process can come under running state until previous had been executed
Priority scheduling is a method of scheduling processes based on priority. In this method, the scheduler chooses the tasks to work as per the priority, which is different from other types of scheduling, for example, a simple round robin.
Priority scheduling involves priority assignment to every process, and processes with higher priorities are carried out first, whereas tasks with equal priorities are carried out on a first-come-first-served (FCFS) or round robin basis. An example of a general-priority-scheduling algorithm is the shortest-job-first (SJF) algorithm.

Shortest Job First (SJF) is an algorithm in which the process having the smallest execution time is chosen for the next execution. This scheduling method can be preemptive or non-preemptive. It significantly reduces the average waiting time for other processes awaiting execution.

