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

* Describe a few ways a process can get put in the ready queue
(i.e., where did the process come from and what changed?)

* Which of these typically results in a process waiting somewhere *other* than
the ready queue?
    * reading from disk
    * calling a function
    * prompting a user in the terminal
    * reading a variable from memory
    * reading input from the terminal
    * process interrupted because time slice expired

* In a system with all compute-bound processes,
in what sense would scheduling be easy?
How might it be hard?

* Most processes follow a CPU-I/O burst cycle.
Briefly describe what that means and give a few examples of programs that
follow that pattern.
Can you think of any programs that do not?

* In which of the following cases will a nonpreemptive scheduler schedule a
new process? The running process calls...
    * `fopen()`
    * `x = arr[5]` where `arr` is on the stack
    * `x = arr[5]` where `arr` is in shared memory
    * `printf()` where `arr` is in shared memory
    * A file read finishes for a higher-priority process

* Nonpreemptive scheduling can help avoid some types of race conditions. Why?
Try to think of a simple race-condition example we have seen that would be
avoided by nonpreemptive scheduling.

* Most modern OSes use preemptive scheduling. One upside to nonpreemptive
scheduling is that it does not require a hardware timer.
Another is that it can help avoid race conditions.
Can you think of another upside to nonpreemptive scheduling?

* Recall that throughput is the number of processes completed in a set time.
Can you think of a simple scheduling algorithm that maximizes throughput?

* Why might waiting time be a more appropriate measure of a CPU scheduling
algorithm than turnaround time?

* (Textbook 6.11) Describe how the following pairs of scheduling criteria
conflict in certain settings.
    * CPU utilization and response time
    * Average turnaround time and maximum waiting time
    * I/O device utilization and CPU utilization
