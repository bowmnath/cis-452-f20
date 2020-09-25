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

Give a few examples of when it might be useful for a program to catch SIGINT
(or another signal of your choosing).

Which is faster: context switching between threads or between processes?
Why? Be as specific as possible.

Give an example of when you might spawn a child process instead of a thread.

Give an example of when you might spawn a thread instead of a child process.

Examine the code snippet below.
For all examples in this activity,
assume the correct `include`s have been used and the variables declared, etc.
(Also, please don't use the code in this document as an example of how to code.
I expect *much* more error checking from you.)
```
int main() {
    ...
    int a = 5;
    pid = fork();
    if (pid == 0) {
        a = 10;
        exit(0);
    }
    wait(NULL);
    printf("%d\n", a);
    ...
```
What is printed?

Examine the code snippet below.
```
int main() {
    ...
    int a = 5;
    pthread_create(&tid, NULL, add_num, (void*) &a);
    pthread_join(tid, NULL);
    printf("%d\n", a);
    ...

void* add_num(void* inval) {
    int a;

    a = *(int*)inval;
    a += 1;
    return NULL;
}
```
What is printed?

Examine the code snippet below.
```
int a;
int main() {
    ...
    a = 5;
    pthread_create(&tid, NULL, add_num, NULL);
    pthread_join(tid, NULL);
    printf("%d\n", a);
    ...

void* add_num(void* inval) {
    a += 1;
    return inval;
}
```
What is printed?

Examine the code snippet below.
```
int a;
int main() {
    ...
    a = 5;
    pid = fork();
    if (pid == 0) {
        a = 10;
        exit(0);
    }
    wait(NULL);
    printf("%d\n", a);
    ...
```
What is printed?

What are the advantages of user-level threads compared to kernel-level threads?
What are the disadvantages?

Give a simple example of a way that you could make program performance *worse*
by using multithreaded code.
You do not need to actually write the code.

In a many-to-one threading system,
is it possible to schedule two threads from the same process to different
CPUs?
What about in a one-to-one threading system?

Which of the following are shared by threads within the same process?
(Textbook exercise 4.8)
* Register values
* Heap memory
* Global variables
* Stack memory

Examine the code snippet below.
```
fd = open(fname, O_RDONLY);
pid = fork();
if (pid == 0) {
    close(fd);
    exit(0);
}
wait(NULL);
read(fd, buf, BUF_SIZE);
```
Will the `read` succeed?
Why or why not?

Examine the code snippet below.
```
fd = open(fname, O_RDONLY);
pthread_create(&tid, NULL, close_file, (void*) &fd);
pthread_join(tid, NULL);
read(fd, buf, BUF_SIZE);
...

void* close_file(void* fd) {
    close(*(int*)fd);
    return NULL;
}
```
Will the `read` succeed?
Why or why not?


## Exploring

It has been mentioned in lecture that Linux does not intrinsically think in
terms of "processes" and "threads".
Instead, everything is a "task".
Some tasks share nothing,
so they are like processes,
and other tasks share a lot,
so they are like threads.

(To be clear -- you should still think at the level of processes and threads.
That is the level of abstraction presented to you by `pthreads`,
and it is nicer conceptually.
Think of tasks as an implementation detail.)

Tasks (both processes and threads) are created by the `clone` system call.
Both `fork` and `pthread_create` rely on this system call underneath.
Examine the differences in the calls to `clone` during process creation vs
thread creation,
especially the `flags`.

To do so, write a very simple program that spawns a thread.
Then, use `strace` to examine the `clone` system call.
The `-e` flag will be helpful.
Next, do the same for a very simple program that uses `fork`.

You can find out more about the arguments to `clone` using `man 2 clone`.
The flags themselves are defined in `/usr/include/linux/sched.h`.
