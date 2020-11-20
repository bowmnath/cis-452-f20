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

1. Why is it infeasible to implement true LRU page replacement?

2. Two ways of implementing true LRU were discussed in lecture:
with a stack, or with a counter.
(Remember -- we discussed these as possibilites,
but neither is efficient enough to work in practice.)
Briefly describe the stack method.
Why did the "stack" method not actually use a stack underneath for storage?

3. Would it be feasible to use true LRU if information about access order were
kept in registers instead of memory?

4. Recall the additional-reference-bits approximation to LRU.
Assume the OS is keeping a 3-bit counter for each page.
Consider the following memory access history, where
    * each number represents access to the corresponding page
    * the vertical bars represent timer interrupts for the OS to update the
      counters

`0 1 0 1 1 | 1 0 0 | 2 |`

```
Page    Counter
---     ---
0
1
2
```

Be careful -- this is an approximation.
You cannot just count accesses.

---

Consider approximating LRU using the second-chance algorithm.
Use the following table for the next few questions.
Also, this is not explicitly stated in the slides,
but you may assume that the reference bit is set when a page is read in.

```
Queue:          4   0   1   5   2   3
Reference bit:  1   0   1   1   0   0
```

---

5. Which page will be evicted if a page fault occurs?

6. What will the table look like after a single page fault?
Assume page `6` is read in.

7. What will the table look like after two page faults?
Assume pages `6` and `7` are read in.

8. Assume 1024 1KB frames are available on a system and the OS uses 24 frames.
There are three processes on the system with the following memory requirements:

```
Process     Memory (KB)
---         ---
0           800
1           800
2           400
```

How many frames would each process be assigned using equal allocation?
Using proportional allocation?

9. Consider the following scenario:
Process A requires 20 frames of memory but has been allocated 50 frames.
Process B requires 80 frames of memory but has als been allocated 50 frames.
Clearly, this situation could be improved.
Which would do a better job of getting frames to where they are needed:
local replacement or global replacement?
Briefly explain.

10. Briefly explain how one thrashing process can be trouble for the entire
system when using global replacement.

11. When a process is in function `foo`,
it primarily accesses 2 frames of stack space containing local variables.
When it leaves `foo` and goes to `bar`,
it primarily accesses 8 frames of heap space containing an array.
What idea from lecture is this an example of?
Why does it matter when considering frame allocation?

12. Consider the following memory accesses,
where each number represents a page access.

```
2   3   3   4   1   3   3   1   1   2
```

What is the working set at the end if the size of the working set window is 5?
How many frames would the process that generated these accesses be alloted?


13. Identify any localities in the following set of memory accesses.
This is not an exact science.

```
2 3 3 2 1 2 3 3 2 4 1 3 4 1 1 1 4 5 4 3 1 2 5 1 3 4 2
```

14. Given what you found above,
what would be an appropriate size for the working set window on the system?
In other words,
what size working set window would do a good job capturing the localities?
This is very much not an exact science.

15. What advantage(s) does monitoring the page fault rate directly have over
using a working-set model?
