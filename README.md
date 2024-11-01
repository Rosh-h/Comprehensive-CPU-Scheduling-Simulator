# Comprehensive-CPU-Scheduling-Simulator
This project implements multiple CPU scheduling algorithms used in operating systems to manage process execution and optimize CPU performance. The algorithms implemented include:

First Come First Serve (FCFS)
Round Robin (RR) with varying time quantum
Shortest Process Next (SPN)
Feedback (FB)
Aging
Overview
In operating systems, CPU scheduling algorithms determine the order of process execution on the CPU to optimize performance metrics like waiting time, turnaround time, and CPU utilization. Each algorithm has unique strengths, and this project demonstrates the differences by implementing several popular scheduling techniques.

Algorithms
First Come First Serve (FCFS)
Description: The FCFS algorithm schedules processes in the order they arrive in the queue. It operates in a non-preemptive manner, meaning once a process starts execution, it will complete before any other process can start.
Advantages: Simple to implement, and predictable.
Drawbacks: Can lead to high average waiting times, especially when longer processes arrive first (resulting in the "convoy effect").
Round Robin with Varying Time Quantum (RR)
Description: The RR algorithm assigns a fixed time quantum to each process in the queue. When a process's time quantum expires, it returns to the back of the queue if it's not finished, allowing other processes a turn.
Varying Time Quantum: This project explores the effects of using different time quantum values, as choosing an optimal quantum is key to balancing throughput and responsiveness.
Advantages: Fairer to all processes, reduces waiting time for shorter processes.
Drawbacks: Choosing the wrong quantum size can lead to either high context-switching overhead (if too small) or long waiting times (if too large).
Shortest Process Next (SPN)
Description: The SPN algorithm selects the process with the shortest expected processing time. It’s a non-preemptive algorithm, meaning once a process starts, it runs to completion before the next is chosen.
Advantages: Minimizes average waiting time by always selecting the shortest job.
Drawbacks: Can cause "starvation" for longer processes if there’s a constant influx of shorter ones.
Feedback (FB)
Description: Feedback scheduling dynamically adjusts process priority based on its behavior and usage, often moving longer-running tasks to lower priority queues.
Advantages: Adapts to process needs, favoring shorter processes but allowing longer processes to complete over time.
Drawbacks: Complexity in implementation and tuning for optimal performance.
Aging
Description: Aging is an enhancement to other algorithms (such as Priority Scheduling) where the priority of a process gradually increases as it waits, preventing starvation for low-priority tasks.
Advantages: Ensures fairness by preventing starvation.
Drawbacks: Adds complexity and may reduce response times for higher-priority processes if aging increments are too aggressive.
