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

Is it possible for two processes to communicate without OS intervention?
If so, how?
If not, why not?

Name a few reasons a process might benefit from spawning another process to
perform some work even if the system has just one processor.

Which method of IPC generally requires more system calls:
message passing or shared memory?
Why?

Using POSIX shared memory,
can more than two processes communicate at once?
Why or why not?

The ideas of buffering and synchronous vs. asynchronous communication are
intertwined.
Explain how/why.

Why is an asynchronous send, if available,
often preferable to a synchronous send?

Can you think of a situation in which synchronous communication would be
preferred even if asynchronous communication were possible?

Take a look at the following (edited) snippet from your textbook
(also shown in the lecture video):
```
	/* create the shared memory segment */
	shm_fd = shm_open(name, O_CREAT | O_RDWR, 0666);

	/* configure the size of the shared memory segment */
	ftruncate(shm_fd,SIZE);

	/* now map the shared memory segment in the address space of the process */
	ptr = mmap(0,SIZE, PROT_READ | PROT_WRITE, MAP_SHARED, shm_fd, 0);

	sprintf(ptr,"%s",message0);
	ptr += strlen(message0);
	sprintf(ptr,"%s",message1);
	ptr += strlen(message1);
	sprintf(ptr,"%s",message2);
	ptr += strlen(message2);
```
How could you write this without using the call to `mmap`?
You can explain in generic terms,
or try to actually modify the code.

Why does an ordinary pipe require a parent-child relationship to function,
whereas a named pipe does not?

What is the output of the following code?
```
#include <stdio.h>
#include <unistd.h>
#include <sys/wait.h>
#include <stdlib.h>

int main()
{
    pid_t pid;
    char *msg;
    FILE *infile;

// BEGIN BLOCK A
    if ((infile = fopen("message.txt", "r")) == NULL) {
        perror("could not open");
        exit(1);
    }
// END BLOCK A

    pid = fork();

    if (pid < 0) {
        perror("fork failed");
        exit(1);
    }

// BLOCK B GOES HERE

    if (pid == 0) {
        fscanf(infile, "%ms", &msg);
        printf("%s\n", msg);
        free(msg);
        exit(0);
    }

    wait(NULL);

    fscanf(infile, "%ms", &msg);
    printf("%s\n", msg);
    free(msg);

    fclose(infile);

    return 0;
}
```
You can assume that `message.txt` contains the message `hello world`.

Does the output change if `BLOCK A` is moved to immediately after the fork?

Assume the code above is back to its original form.
What happens if the following code is inserted as `BLOCK B`?
```
    if (pid > 0) {
        fclose(infile);
        if ((infile = fopen("mensaje.txt", "r")) == NULL) {
            perror("could not open");
            exit(1);
        }
    }
```
Assume the file `mensaje.txt` contains the message `hola mundo`.
What is the output?
Does it depend on whether the parent or child runs first?

## Exploring

Regarding the shared memory code snippet above,
we said it was possible to use `shm_open` without `mmap`.
The reverse is also possible --
you can create a shared memory space without passing a corresponding file
descriptor.
Look in the `man` pages to figure out how this could be done.

How could it ever be useful to do so?
That is, why bother creating a shared memory segment if you are not giving it a
name in the filesystem that other processes can access?

## Coding

You saw in lecture that the producer-consumer problem is very easy to solve
with synchronous message passing.
Pipes give us a form of message passing,
but it is not synchronous.
How could you solve the producer-consumer problem using pipes?
(Hint: You will most likely want more than one pipe.)

In addition to the usual `man 2 pipe` or `man 3 pipe`,
you may also find `man 7 pipe` helpful for understanding general pipe behavior.
