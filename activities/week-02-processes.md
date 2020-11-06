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

# General Questions

* Describe what happens during a context switch.
Be as precise as you can.

* Assume there is a simple tree of processes: a -> b -> c -> d -> e.
In this diagram, "->" represents a parent-to-child relationship.
If c dies before d finishes,
how are resources collected for *each* processs
(i.e., b, c, d, and e)?

* Give two examples of I/O-bound and two examples of CPU-bound processes.

* If you log in as `root` on a Linux system,
is the system running in user mode or kernel mode?

* What is the difference between a system call and a call to a `libc` routine?

* Given the following snippet,
and assuming the correct imports were used,
how many processes would be created?
Sketch a simple process tree for the code.
```
int main() {
    fork();
    fork();
    fork();
    return 0;
}
```

* Given the following snippet,
and assuming the correct imports were used,
how many processes would be created?
Sketch a simple process tree for the code.
```
int main() {
    int i;
    for (i = 0; i < 4; i++) {
        fork();
    }
    return 0;
}
```

* A running process needs to accomplish some task.
What are the advantages and disadvantages of spawning a child to complete
the task vs doing it without spawning the child?

* Look up the call to wait for a *specific* child.
What happens if you try to wait for PID 1?

* What would happen if a parent:
    * spawned a lot of children,
    * never waited on them, and
    * never exited?

* Does `exec` create a new process?
How could demonstrate this using a C program and system utilities?
(You do not need to actually do so,
though feel free if you have time).

* In our examples so far, the child has been the one to `exec`.
Can the parent `exec` instead?
Would there be substantial benefits or drawbacks?

* What is one example of a change to hardware or OS design that can make
a context switch faster? slower?

* Explain the purpose of keeping device queues from a CPU scheduling
perspective.

* Imagine a simple CPU scheduler that went through every existing PID in a
round-robin fashion and assigned them equal CPU time.
    * Would there be any benefits to this?
    * Any drawbacks?

## Exploring

* Linux source code is available on GitHub.
In Linux, a PCB is (essentially the same as) a `task_struct`.
Have a look in `sched.h`:
[https://github.com/torvalds/linux/blob/master/include/linux/sched.h](https://github.com/torvalds/linux/blob/master/include/linux/sched.h)
Find the `task_struct` definition and look around a little.
    * How big is the definition (how many lines)?
    * Where does it store, for example, information about open files?

* Read the first few paragraphs of the manual page for `errno`.
Also read the NOTES section at the bottom.
`errno` is what allows the `perror` function you saw in the lab
(`man perror` for details)
to work.
    * What is one advantage of `errno` compared to returning the error value
    directly?
    * What is one disadvantage?

I would recommend reading more about `perror` and `errno` on your own to ensure
you understand how they work.
For example,
using `errno`,
could you write a program that correctly detected when the system did not have
enough memory to fulfill a `malloc`,
printed a message to warn you,
and exited?
That is outside the scope of this discussion section, however.

## Coding

* Write a program that results in a zombie process
(look it up if you do not recall what a zombie process is).
View the zombie process in `ps`.
You may need to use a `sleep` call to ensure the process stays a zombie long
enough for you to view it.
