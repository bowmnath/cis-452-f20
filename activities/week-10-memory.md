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

12. What is the physical address corresonding to the given logical address?
(Careful!)

13. Given that some process has the above page table,
Is it possible for another process to have the following page table?
Why or why not?

```
1111
1110
1010
0001
```

14. In a system with a page size of 1024 KB,
which of the following will lead to more internal fragmentation?
* Process A with 10239 KB of memory
* Process B with 2560 KB of memory

15. Try to come up with a system that does not suffer from interal or external
fragmentation.
Is it possible?
If so, why is the system not used in real OSes?
If it is not possible, why not?
