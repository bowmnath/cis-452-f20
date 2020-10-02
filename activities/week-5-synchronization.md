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

***

Let's start off with a small game.
(I know this is silly -- please humor me.)
Nominate one person in your group to be "memory".
Everyone else is a thread.

The threads are all executing the following code:
```
// global variable x
x = x + 2;
x = x + 2;
```
You can do addition in your head.
However, the only way you can get or set the value of `x` is by sending one of
the following messages (privately) to "memory":
```
get x
set x = [num]
```

Whoever is memory:
    * pick a small random number for the initial value of `x`.
    * when sent a `set` message, set the value of `x` and respond `ok`
    * when sent a `get` message, respond `x = [num]`
Remember, your job as memory is not to do math or be sensible --
just do exactly as you are asked by the threads in the exact order you
receive the requests.

Discuss what happened.
It may be helpful for memory to copy and paste their chat publicly once
the exercise is over.

***

Next, a similar game.
(We'll skip this if the first one was not helpful.)
Whoever in your group is memory is now also the OS.
Everyone else is a thread.

Run the same code, but add mutex lock(s) and unlock(s).
It's up to your group where you want to add them --
some options may be more efficient than others.

Everything is the same as before,
except threads can request the mutex from OS/memory with `mutex please` and
return it with `done with mutex`.
Whenever waiting for the mutex, a thread is idle.

Whoever is OS/memory has the same job as before,
except they now also respond to mutex requests.
Send back `mutex granted` once the mutex is granted and `mutex released` when
the thread is done with the mutex.

Discuss what happened.
How was it better than the first time?
How was it worse?

***

1. State in general terms what can go wrong if we are not very careful with how
we access shared memory.

2. In lab from last week,
we needed to keep a running total of file requests.
Try to think of one advantage and one disadvantage to doing this in the worker
threads vs having the main thread keep track.

3. Explain what happens when a thread calls `pthread_detach`.
How is it different from `pthread_join`?

4. What is wrong with the following?
How would you add a mutex or semaphore to fix it?
(Pseudocode is fine)
```
int a = 5;
int main() {
    ...
    pthread_create(&tid, NULL, add_num, NULL);
    pthread_create(&tid2, NULL, add_num, NULL);
    pthread_join(tid, NULL);
    pthread_join(tid2, NULL);
    printf("%d\n", a);
    ...

void* add_num(void* inval) {

    a *= 5;
    return NULL;
}
```

**Note:** several of these questions about efficiency are quite open-ended.
Use it as an opportunity for discussion.

5. Several threads are running identical code with shared variable `num`.
```
for (int i = 0; i < 10; i++) {
    num = num*5;
    ... // code not involving num
}
```
Where would it be best to put mutex lock and unlock calls?
(There is not necessarily one right answer --
think in terms of mutual exclusion *and* efficiency)

6. Could you rearrange the above code to add your mutex in a way that makes the
program more efficient?

7. We introduced [the ideas](https://github.com/bowmnath/cis-452-f20/blob/master/slides/parallel-critical-section.pdf)
of mutual exclusion, progress, and bounded waiting in lecture.
Briefly explain what each of these means and why it is important.

8. Assume the variable `access` protects a critical section.
Would the following C function be effective for synchronization?
Why or why not?
```
int access_by_id(int tid, int *access) {
    if (*access == -1) {
        *access = tid;
        return 1;
    } else {
        return 0;
    }
}
```

9. What does it mean for something to execute **atomically**?

10. Assume there is a read-only database that can accept up to 5 requests at a
time without issue.
If more than 5 requests are active at once,
the database will try to keep running but will start returning incorrect
values unbeknownst to the readers.
Describe how processes could synchronize access to this database.
(Hint: one of the synchronization tools you know will be much easier here than
others.)

<!--
11. Semaphores are implemented with a waiting queue rather than busy waiting,
as discussed in lecture.
Pretend we have a semaphore that can use either type of waiting --
it has a `dizzy_wait` for spinlocking and a `sleepy_wait` that yields the CPU.

The `dizzy_wait` and corresponding `dizzy_signal` routines do not require a
system call,
so each takes just 1 ms on its own.
However, `dizzy_wait` holds the CPU while waiting.

The `sleepy_wait` and `sleepy_signal` routines each require a system call.
(Actually, they may not require system calls if the semaphore is already
available, but we will make this simplifying assumption.)
So, each takes 10 ms.
However, a `sleepy_wait`ing thread will not be scheduled again until it is
`signal`ed.

Study the following code.
```
A                       B

dizzy_wait()            sleepy_wait()

// 100 ms of code       // 100 ms of code

dizzy_signal()          sleepy_signal()
```

If two threads are going to reach the critical section at the same time,
is it more efficient if they implement code `A` or code `B`?
What would be the approximate difference in CPU time used?
This difference can depend heavily on random chance associated with the
scheduler,
so feel free to make some simplifying assumptions.
-->

11. Briefly describe the concept of *starvation* in a synchronization scenario.

12. Many synchronization problems would have a trivial solution if we did not
concern ourselves with starvation. Why?
This is not a particularly helpful realization from a practical perspective,
though. Why?

13. Review the solution to the
[Readers-Writers Problem](https://github.com/bowmnath/cis-452-f20/blob/master/slides/sync-classic.pdf).
Could you make the solution substantially simpler if there were only one writer
(but still an arbitrary number of readers)?
If so, how?
If not, why not?

14. Some of you may have noticed that we started talking about threads a while
back,
but the lectures on synchronization have revolved around communicating
processes.
The truth is,
it doesn't make much difference in the instances we are discussing.
Why?
(Hint: how have our processes been communicating?)

## Note about lectures

The lectures on classic synchronization problems are relatively brief,
but these problems are important for understanding how these concepts can be
applied to typical situations.
It would be difficult to internalize the patterns for these problems after
seeing them just once.

I encourage you to either rewatch those videos a few times or find a written or
other video source that gives an explanation that makes intuitive sense to you.
It is also helpful to go through the examples and try to find ways to "break"
them --
ways that mutual exclusion could fail if the scheduler was particularly
unlucky.
You shouldn't be able to find any,
but the exercise will help you understand what is happening.
On a similar note,
it can be useful to rearrange the code in small ways or change one thing and
try to see whether your updated code works or how it fails.
Working in safely parallel is **hard** and requires practice.
