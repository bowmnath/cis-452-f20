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

1. Consider a UNIX-style inode containing 15 block pointers with
    * 12 of them to direct blocks
    * 1 to single indirect block
    * 1 to double indirect block
    * 1 to triple indirect block

All indirect blocks also hold 15 pointers.
(Remember -- some of those pointers are directly to blocks,
but others are to other index blocks.
The distinction depends on the level of indirection.)

What is the maximum number of blocks that can be stored in a single file on
the described system?

* For the next few questions, assume there are 1000 cylinders on a hard disk and
use the following sequence of cylinder requests:
400 600 650 410 350 370 680

2. Give the order in which the requests will be satisfied using
FCFS scheduling.
How far must the disk head travel (in cylinders) to satsify the requests?

3. Give the order in which the requests will be satisfied using
SSTF scheduling.
How far must the disk head travel to satsify the requests?

4. Give the order in which the requests will be satisfied using
SCAN scheduling.
How far must the disk head travel to satsify the requests?

5. How much travel would have been saved if LOOK had been used instead of SCAN?

6. Give the order in which the requests will be satisfied using
C-SCAN scheduling.
How far must the disk head travel to satsify the requests?

7. C-SCAN results in more overall disk-head travel than SCAN.
What advantage does C-SCAN have?

8. Give a few examples of security *policies* and a few examples of security
*mechanisms*.

* For the next few questions, use this output:

```
$ ls -l
total 0
-rwxrwxrwx 1 nate class 0 Dec  8 00:23 grader.out
-rw-rw-rw- 1 nate class 0 Dec  8 00:23 messages.txt
-rw------- 1 nate nate 0 Dec  8 00:23 solution-code.c
-rw-rw---- 1 nate team 0 Dec  8 00:24 roster.csv
```

9. If user `chewie` is a member of `team`,
what access rights does `chewie` have for each of the files?

10. Assume some team members are clumsy and can be given read access to the
roster but not write access.
They are removed from `team` and added to group `clumsy`.
Is there any way to use `chmod` to give these people read access to
`roster.csv` without changing other permissions?
If so, how?
If not, what could be done to accomplish the same goal?

11. A long listing of `/bin/bash` looks something like

```
-rwxr-xr-x 1 root root 928016 Nov 20 15:25 /bin/bash*
```

What would happen if the `setuid` bit were set for `/bin/bash`?

12. You carefully set your file access permissions to ensure the important
files in directory `/home/me/documents/harry-potter-fanfic` are accessible only
to `me`.
Someone who boots your laptop from another OS and wants to steal this
information.
What do they need to do to circumvent your protections?

13. If a Nigerian prince needs your password to deposit money into your bank
account,
should you give it to him?
