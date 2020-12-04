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

1. Would it be possible to run a computer without any secondary storage
(i.e., with memory only)?
Why or why not?

2. Is the page table backed up in secondary storage before a system powers off?

3. Instead of allowing users to specify disk locations directly,
the OS provides a file system.
Would it be possible to run without a file system?
If so, give some upsides and downsides to using a file system.
If not, explain why not.

4. When writing a new filesystem,
you realize file creation and access would be faster if all inodes were
in memory instead of being written to disk.
Explain why this idea will not work.

5. In your next attempt at improving file system access,
you decide to read an entire page worth of data from disk every time a disk
read is required,
even if much less data is actually requested.
Explain any benefits or drawbacks that would come from this idea.

6. Why is it expensive to simulate direct access when only sequential access is
available?

7. When running `cat /usr/local/include/stdio.h`,
how many directories must be read to locate the file on disk?

8. Each process has a current working directory associated with it.
Keeping track of this requires extra overhead for the OS.
Is there any performance benefit to this compared to requiring users to
specify the full path each time a file is opened?

9. Explain why allowing hard links complicates the process of deleting a file
for the OS?

10. Assume that scheduling algorithms that take longer can make better
predictions about future behavior.
Which of the below scheduling algorithms should be allowed to run for longer?
Why?
    * Scheduling the next process on the CPU
    * Scheduling disk reads

11. Order the following from least to greatest amount of storage overhead:
    * indexed allocation
    * linked allocation
    * contiguous allocation

12. Assume you have the inode of a file in memory but have yet to access any
blocks of the file.
For each of the above schemes,
how many disk accesses are required to read the 10th block of the file?

13. In the above situation,
how many disk accesses would be required if the linked allocation used a FAT?

14. What is the downside to contiguous allocation?

15. For which of the following systems would indexed allocation result in more
wasted storage overhead?
    * One where most files are of moderate size
    * One with mostly small files and a few large files

Why?
Assume the characteristics of the stored files are known when the file system
is designed.

16. Consider a UNIX-style inode containing 15 block pointers with
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
