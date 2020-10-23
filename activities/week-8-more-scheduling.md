In your groups, answer the following questions.
No need to report the answers to me --
this is just for practice.
There are a lot of questions here,
and I don't necessarily expect us to finish them all.

I will be dropping in and out of rooms to facilitate to the discussions and in
case you have any questions.
Think of it like me walking around the classroom and listening to different
groups.
Again, this isn't meant to be for a grade,
so don't be concerned about giving a wrong answer even if I am in the room.
You can also flag me down in Zoom if you have a question even if I'm not in the
room
(I think the button in Zoom looks like a question mark).

Note: some questions are taken entirely or in part from your textbook.

## General Questions

* Explain in general terms the difference between preemptive and nonpreemptive
scheduling.

*Note:* When answering the scheduling questions,
you would ideally create a Gantt chart for many of them.
However, that may be difficult to share with your classmates over Zoom
depending on how you do it.

* How would the following processes be scheduled under SJF scheduling if the
scheduling is
    * nonpreemptive?
    * preemptive?

```
Process   | Arrival Time | Burst Time
---       | ---          | ---
P1        | 0            | 6
P2        | 2            | 5
P3        | 3            | 2
P4        | 4            | 6
```

* What is the average waiting time in each scenario?

* Using an exponential average with $\alpha = 0.5$,
fill in the table with the predicted burst times that could be used for SJF.
(This will look similar to the table in the
[slides](https://github.com/bowmnath/cis-452-f20/blob/master/slides/scheduling-bursts.pdf).
Look for the slide with the big graph on it.
The equation on the next slide will also be helpful.)

```
Burst number ($i$) | Actual duration ($t_i$) | Predicted duration ($\tau_i$)
---                | ---                     | ---
0                  | --                      | 10
1                  | 5                       |
2                  | 5                       |
3                  | 10                      |
4                  | 10                      |
```

* Assume a system uses priority scheduling.
The OS has a daemon (A) running that runs once every 5 ms for a duration
of 3 ms.
Another daemon (B) runs once every 5 ms for a duration of 2 ms.
Both daemons have a priority of 1.

A user submits a process of priority 2 with a duration of 3 ms.
How long will it be before the user process gets to run?

What mechanism can we use to allow the user process to run sooner?

* Four processes arrive in the ready queue at approximately the same time.
Their burst times are given below.
Assuming round-robin scheduling with a time quantum of 4 ms,
what is the turnaround time for each process?

Recall that turnaround time is the entire time from when a process enters the
ready queue to when it finishes running.

```
Process | Burst Time
---     | ---
P1      | 6
P2      | 5
P3      | 2
P4      | 9
```

* In multilevel queue scheduling,
processes are assigned to queues and those queues are (often) assigned
different priorities.
How is this different from simply using priority scheduling and applying
priorities to the processes directly?

* What is the benefit of using a multilevel queue algorithm rather than a
single algorithm for every process on the system?
Give a simple example of a possible multilevel queue setup and why it would be
beneficial.

* Recall the multileve feedback queue from lecture (reproduced below).
Note that, for this particular setup,
there are no arrows from lower-priority to higher-priority queues.
Given the following sets of burst times,
in which queue would each process end up?

* A: 9, 16, 2
* B: 16, 9, 2
* C: 3, 3, 4
* D: 30, 8, 7

![Feedback queue](images/multilevel-feedback.png)

* Process A uses a lot of memory.
Process B does not use much memory.
For which one is processor affinity more important?

* What is the goal of load balancing in multiprocessor scheduling.
How are the goals of load balancing and processor affinity in conflict?
