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

1. What is the difference between a logical address space and a physical
address space?
If the CPU requests address `0x00400000`,
is it requesting that logical or that physical address?

2. Assume the system is using a base-register limit-register pair to protect
memory.
If the base register is set to `50000` and the limit register is set to
`45000` (less than the base register),
is this a problem?
Why or why not?

3. If the limit register could be changed in user mode,
but only to decrement it,
would this be problematic?

4. I used `objdump` to look at the symbol table for an executable I compiled
with `gcc`.
According to the symbol table,
the variable `mynum` is stored at address `0x4028`.
```
nate@msi:~/temp$ objdump -t a.out | grep mynum
0000000000004028 g     O .data	0000000000000004              mynum
```
Is this a physical or a logical address?
What problems could arise if it were the other kind?

5. Assume all of memory is split into four evenly-sized chunks.
One of the chunks stores the OS.
The other three chunks can each be used by a single process.
(This was one of our early, simple attempts at implementing multiprogramming.)
Describe a simple way for the MMU to map logical addresses to physical
addresses in this setup.
You may add other elements,
such as registers,
to the system if necessary.

6. Process A and Process B both link to the `pthreads` library.
If both processes are running at once,
rank these scenarios from least memory usage to most memory usage:
* both are statically linked to `pthreads`
* both are dynamically linked to `pthreads`
* one is dynamically linked to `pthreads` and the other is statically linked

7. Describe at a high level the difference between contiguous memory allocation
schemes and non-contiguous memory allocation schemes.
Try to avoid using the word contiguous in your explanation.

8. Managing memory will generally be simpler in a contiguous scheme. Why?

9. Can external fragmentation occur in a fixed-size partition scheme?

10. How is paging similar to variable-partition memory? How do they differ?
Consider how the memory is stored, not how it is kept track of.

For the next few questions,
consider the page table:

```
0010
0001
0111
0101
```

and logical address `0010111`.

(Note: the page table is written out in binary for your convenience.
To make it look like the one in the slides,
you would simply convert the entries to decimal.)

11. Determine the page size for the given system.
(Note: it is relevant here that the given table is the **entire** page table
for the process.)

```
Answer: The page table has four rows.  So, two bits of the logical address
must be dedicated to specifying the page (because 2^2 = 4).  The full logical
address given above had seven bits. That leaves 5 (= 7 - 2) bits to specify the
offset into a page. Thus, a page holds 32 (= 2^5) bytes.

Note that the number of bits in the **frame number** is irrelevant here. Each
frame address stored in the page table has four bits. So, there must be
16 (= 2^4) frames in the system. But, the number of pages and the number of
frames can be different, as they are here. The address we were given was a
logical address, not a physical one, so it had nothing to do with the number of
frames.
```

12. What is the physical address corresonding to the given logical address?
(Careful!)

```
Answer: We first map the page number to the frame number, then append the
offset. We already know that there are two bits to specify the page number,
and the rest specify the offset. The breakdown is

00       10111
--       -----
page #   offset

Looking at the table, page 0 is frame 0010. So, the overall address is

0010      10111
----      -----
frame #   offset

or, more simply,

001010111
```

13. Given that some process has the above page table,
Is it possible for another process to have the following page table?
Why or why not?

```
1111
1110
1010
0001
```

```
Answer: There is more than one possible answer here depending on the
assumptions you make.

If we assume there is no sharing of memory (no POSIX shared memory, no
dynamically-linked libraries, etc.), then no two processes should have access
to the same frame. (Remember -- frame, not page. All processes will have a
page 0, page 1, and so on.)

The frame 0001 appears in both tables, so the two processes would have access
to the same memory, which is not allowed under our above assumption. Thus, it
would not be possible for another process to have this page table.

However, if we assume the processes are sharing memory in some OS-approved way,
then there is no problem with the given table.
```

14. In a system with a page size of 1024 KB,
which of the following will lead to more internal fragmentation?
* Process A with 10239 KB of memory
* Process B with 2560 KB of memory

```
Answer: Internal fragmentation occurs when a process is assigned more memory
than it actually uses. In this example, memory is assigned in chunks of
1024 KB. Each process will always be given as much memory as it needs --
that is, a process may be given more memory than it requires, but it will not
be given less.

Process A requires 9 (= 10239 / 1024) full pages of memory and has 1023 KB left
in its 10th page. Thus, process A has internal fragmentation of
1 KB (= 1024 in page - 1023 used).

Process B requires 2 (= 2560 / 1024) full pages of memory and has 512 KB left
in its 3rd page. Thus, process B has internal fragmentation of
512 KB (= 1024 in page - 512 used).

Process B has more internal fragmentation.
```

15. Try to come up with a system that does not suffer from interal or external
fragmentation.
Is it possible?
If so, why is the system not used in real OSes?
If it is not possible, why not?

```
Answer: The variable-partition contiguous memory scheme does not suffer from
internal fragmentation if we allocate memory down to the byte. If we were to
compact memory every time a process exits (for example, by moving all processes
to the lowest address possible), there would also be no external fragmentation.
All of the available memory would always be in a single hole.

The system described is not used because it would be impractical. For one, as
was described in lecture, variable-partition schemes typically do not track
memory down to the individual byte. Much more important, however, is the fact
that the OS would not want to waste the time to rearrange large amounts of
memory every time a process exited.
```
