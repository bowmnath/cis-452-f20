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

For the first four questions,
consider the page table:

```
010
101
111
000
```

and logical address `01010111`.

(Note: the page table is written out in binary for your convenience.
To make it look like the one in the slides,
you would simply convert the entries to decimal.)

1. How many pages of logical memory does the process have?

2. How many frames of physical memory can the machine have?

3. What is the size of a page in the given system? A frame?

4. What is the physical address corresonding to the given logical address?

5. Assume a process has 2 GB of virtual memory.
If it tries to access address 3,000,000,000, what will happen?

6. From a performance standpoint,
which would make virtual memory more appealing:
speeding up memory or speeding up disk access?
Or, would they have about the same effect?

7. A hypothetical process has eight entries in its page table.
Four of them are currently valid.
In general terms, what is the probability that the process will have a page
fault on its next memory access?
(much lower than 50%, a little lower, roughly 50%, a little higher,
much higher than 50%)

8. A page fault occurs, but there is already a free frame available,
so no pages need to be evicted from memory.
Can the OS save time by not updating the page table in this case?

9. You are in a library, and there are three books you need.
* One is a book you just put back on the shelf.
Thankfully, you saved an index card with the book's location.
* The second is a book you have not read before.
You need to go to the computer to find where it is shelved,
and then you can grab it from the shelf.
* The third is another book you have not read.
You go back to the terminal to find its location.
It turns out that the book is in another library,
so you need to wait for it to be delivered.

What does this story have to do with the difference between a TLB miss and a
page fault?

10. Which is more expensive -- TLB miss or page fault?

11. Is it true that a process's virtual memory must be no more than double the
size of physical memory?
Why or why not?

12. When choosing which page to remove from memory,
what is a possible upside to choosing one filled with code?
Is there a possible downside?

13. Assume the following memory accesses occur in a system that has four frames
of physical memory.
```
0 1 3 0 1 4 5 3 4 0
            ^
            |
```
Which element will be evicted from memory when the marked access occurs under

* OPT?
* FIFO?
* LRU?
