## Welcome to CIS 452!

This is the main website for the course.
The slides, schedule, and links to assignments, labs, and projects,
as well as the official course policies,
will be posted here.
The course also uses other websites for specific purposes.
* [Piazza](http://www.piazza.com) is a question-and-answer forum.
*All official announcements will be sent through Piazza*,
and you are responsible for monitoring Piazza to keep up to date with
announcements
(Piazza by default will send an email when an announcement is posted).
    * Signup link:
      [www.piazza.com/gvsu/fall2020/cis452](http://www.piazza.com/gvsu/fall2020/cis452).
    * You can read the following [Piazza FAQ](misc/piazza-faq.md) if you have
      questions.
* [Zoom](https://zoom.us) will be the video conferencing service for office
  hours and synchronous course meetings.
    * Course meetings and labs:
      [https://us02web.zoom.us/j/81970158199?pwd=WjExTXBlRk9oR1NtM01pZDI4TFl0dz09](https://us02web.zoom.us/j/81970158199?pwd=WjExTXBlRk9oR1NtM01pZDI4TFl0dz09)
    * Office hours:
      [https://us02web.zoom.us/j/86265634339?pwd=S2NmYjRkUFRsR3Jpb1JoU0VEQ2JtUT09](https://us02web.zoom.us/j/86265634339?pwd=S2NmYjRkUFRsR3Jpb1JoU0VEQ2JtUT09)
* [Prairielearn](https://prairielearn.engr.illinois.edu/pl/) is where you will
submit all of your assignments, labs, and projects.

Be sure to read through the [syllabus](syllabus.md) for course policies,
contact information, and other important info.

## Schedule

** Note: This is an estimated timeline and subject to change. **

| Week | Topics | Readings | Deliverables |
| ---- | ------ | -------- | ------------ |
|  1   | Course logistics <br>([video](https://drive.google.com/file/d/1t8NlwTP_hG1-gAitlwxBt21yqEguhdeE/view?usp=sharing))<br> Introduction <br>([slides](slides/what-is-os.pdf)) ([video](https://drive.google.com/file/d/1R9mOxVVKTCPM7uqQxqZFgtGq6s42eIQO/view?usp=sharing))<br> Multiprogramming motivation <br>([slides](slides/multiprogramming-basic.pdf)) ([video](https://drive.google.com/file/d/18XZ6-sYRGEftKa28TzYC8zSWro9-yS1H/view?usp=sharing))<br> Interrups <br>([slides](slides/interrupts.pdf)) ([video](https://drive.google.com/file/d/173gheGXEwumtcoRcz05E6jG10zSa-ISP/view?usp=sharing))<br> System calls <br>([slides](slides/system-calls.pdf)) ([video](https://drive.google.com/file/d/11Nhafd3IiNtUlDCN0Gj_TRG1ZQm1TxpV/view?usp=sharing)) | Chapter 1<br> Chapter 2 | **Friday 9/4** [Syllabus quiz](https://prairielearn.engr.illinois.edu/pl/) |
|  2   | Process concepts <br>([slides](slides/process-intro.pdf)) ([video](https://drive.google.com/file/d/1n3ilpQX8KyHDUtj87oX6cbP1IOJXr7bM/view?usp=sharing))<br> Process scheduling <br>([slides](slides/process-scheduling.pdf)) ([video](https://drive.google.com/file/d/1WYDnm95IEsfCfJ2kWcPE7scQuXizDVE9/view?usp=sharing))<br> Process lifecycle <br>([slides](slides/process-lifecycle.pdf)) ([video](https://drive.google.com/file/d/1tbuBorFMtNWtmOQeK16B1uJYTYGA-m5E/view?usp=sharing)) | 3.1 - 3.3 | **Wednesday 9/9** Lab 1 due<br> [Friday activity](activities/week-02-processes.md) (not due for credit) |
|  3   | Interprocess communication<br> ([IPC slides](slides/process-ipc.pdf)) ([IPC video](https://drive.google.com/file/d/1kCh0E5OL0bzsyNf-tJ2b0T-b6pefcgiW/view?usp=sharing)) <br>([POSIX shared mem slides](slides/process-shm-posix.pdf)) ([POSIX shared mem video](https://drive.google.com/file/d/1UJgfiO-1bPmN0R957kgd826nRffuzSTI/view?usp=sharing)) <br>([Message passing slides](slides/process-message.pdf)) ([Message passing video](https://drive.google.com/file/d/1SAjg6wOCz3pDTArkJRr-5BThE0BvgOfQ/view?usp=sharing)) <br>([Pipes slides](slides/process-pipes.pdf)) ([Pipes video](https://drive.google.com/file/d/1kgkfqmPMQwbrNShlMj08Zp8B-_ZZJ-7w/view?usp=sharing)) <br> Threads <br>([Thread overview slides](slides/thread-overview.pdf)) ([Thread overview video](https://drive.google.com/file/d/1Bw4N-N9reZm5dVCAGQXUJt9CKyWoonNN/view?usp=sharing)) <br>([Thread models slides](slides/thread-models.pdf)) ([Thread models video](https://drive.google.com/file/d/1e2McBk8x9BFVd2JELAEfStVPyYIovnPS/view?usp=sharing)) <br>([Thread issues slides](slides/thread-issues.pdf)) ([Thread issues video](https://drive.google.com/file/d/10_FU4IGDHknFeLEHF8X_iD59Gm3jzFEQ/view?usp=sharing)) | Chapter 3<br> Chapter 4<br> [Video errata](misc/errata-ipc.md) | **Wednesday 9/16** Lab 2 due<br> [Friday activity](activities/week-03-ipc.md) (not due for credit) |
|  4   | Process synchronization <br>([slides](slides/parallel-intro.pdf)) ([Synchronization intro](https://drive.google.com/file/d/1aWbPVoawujS2awtlIoS_bu4Dug6XQLy0/view?usp=sharing)) <br> Syncrhonization algorithms <br>([slides](slides/parallel-critical-section.pdf)) ([Synchronization algorithms](https://drive.google.com/file/d/1LhIMqdujkAiFuKegGND-1ltA3U5R0svl/view?usp=sharing))<br> File descriptors <br> ([slides](slides/file-descriptors.pdf)) ([File descriptor video](https://drive.google.com/file/d/1b7xdFDowZUFI5tnhgpW5C_24XYfYMin8/view?usp=sharing)) | 5.1 - 5.3 | **Wednesday 9/23** Lab 3 due<br> [Friday activity](activities/week-04-threads.md) (not due for credit) |
|  5   | Synchronization hardware <br>([slides](slides/sync-hardware.pdf)) ([video](https://drive.google.com/file/d/1g0XJ3pv6zoKa3Sn06idw3irdSDj7DYX8/view?usp=sharing)) <br> Mutex and Semaphores <br>([mutex slides](slides/sync-mutex.pdf)) ([mutex video](https://drive.google.com/file/d/19S_o5uhz9J-MKFVC32FhHzsg3peb7OFX/view?usp=sharing)) <br>([semaphore slides](slides/sync-semaphore.pdf)) ([semaphore video](https://drive.google.com/file/d/1tV0t2zItgIM5Zi4jZscnET5sYfWD8w7I/view?usp=sharing)) <br>([issues slides](slides/sync-issues.pdf)) ([issues video](https://drive.google.com/file/d/1crE7PdCYtMypb39DXv4WmWVjgvvLKa_X/view?usp=sharing)) <br> Classic problems of synchronization <br>([slides 1](slides/sync-classic.pdf)) ([video 1](https://drive.google.com/file/d/1qT1hJs_m2DVNj0NCnH1qDYAN70MyUa6q/view?usp=sharing)) <br>([slides 2](slides/sync-philosophers.pdf)) ([video 2](https://drive.google.com/file/d/19PtihgvsLgzl2zUDw9JSaOdpbJWg3ZAq/view?usp=sharing)) | 5.4 - 5.7 | **Wednesday 9/30** Lab 4 due<br> [Friday activity](activities/week-05-synchronization.md) (not due for credit) |
|  6   | Monitors <br>([intro slides](slides/sync-monitor-intro.pdf)) ([intro video](https://drive.google.com/file/d/16p3KPWMxOjjcxitI3krIeQ1Q_SzJ7-GJ/view?usp=sharing)) <br>([usage slides](slides/sync-monitor-philosophers.pdf)) ([usage video](https://drive.google.com/file/d/1r_CE8lQqJvD6NjRiu-opxd3NkudukZf1/view?usp=sharing)) <br>([implementation slides](slides/sync-monitor-implementation.pdf)) ([implementation video](https://drive.google.com/file/d/1J85TZO2lWbvx8Td7znXMpTDutgUX-JLp/view?usp=sharing)) <br> Deadlock <br>([deadlock criteria slides](slides/sync-deadlock-intro.pdf)) ([deadlock criteria video](https://drive.google.com/file/d/1EcH7-ZIcuUWR7cBwAsLucRq-g9agQri-/view?usp=sharing)) <br>([graphs slides](slides/sync-deadlock-graph.pdf)) ([graphs video](https://drive.google.com/file/d/14LEIj4VEvIZ9WplGnFIacK27NUdZpX9R/view?usp=sharing)) | 5.8, 5.11 | **Wednesday 10/7** Lab 5 due<br> [Friday activity](activities/week-06-monitors.md) (not due for credit) |
|  7   | CPU scheduling concepts<br> ([concepts slides](slides/scheduling-concepts.pdf)) ([concepts video](https://drive.google.com/file/d/1X5mier4bzHf960X8A5cR0VXnQevjBaIy/view?usp=sharing))<br> Scheduling criteria and metrics<br> ([criteria slides](slides/scheduling-criteria.pdf)) ([criteria video](https://drive.google.com/file/d/1ExZv2xl6E4dSWWU5zYlT9GClYW0IWnHD/view?usp=sharing)) <br> FCFS Scheduling<br> ([fcfs slides](slides/scheduling-fcfs.pdf)) ([fcfs video](https://drive.google.com/file/d/1pMk3BTlAY7OcwGKV7IKmoyZxvBlUiMKw/view?usp=sharing)) | 6.1 - 6.2 | **Wednesday 10/14** Lab 6 due<br> [Friday activity](activities/week-07-scheduling.md) (not due for credit) |
|  8   | Scheduling algorithms<br> ([SJF slides](slides/scheduling-sjf.pdf)) ([SJF video](https://drive.google.com/file/d/1IDv3MMHlB0HYV7jpXZN58vVEgvIe3DsZ/view?usp=sharing))<br> ([Burst time slides](slides/scheduling-bursts.pdf)) ([Burst time video](https://drive.google.com/file/d/1tXDcyA37V3c2vHVwq6567gE2xV48vqC9/view?usp=sharing))<br> ([Priority slides](slides/scheduling-priority.pdf)) ([Priority video](https://drive.google.com/file/d/1H8nPfEIBU3Us8Bywwad9EFCxBgDmY6Wj/view?usp=sharing))<br> ([Round-robin slides](slides/scheduling-rr.pdf)) ([Round-robin video](https://drive.google.com/file/d/15XC2N8jHRCSvRY9SdfDkRVl5za2JwYuR/view?usp=sharing))<br> ([Multilevel queue slides](slides/scheduling-multilevel.pdf)) ([Multilevel video](https://drive.google.com/file/d/14fYsFmYcRCy0uufRWrh9mMKhsyidMdsY/view?usp=sharing))<br> ([Feedback queue slides](slides/scheduling-feedback.pdf)) ([Feedback video](https://drive.google.com/file/d/1eqDsOLIuz73zqVt2O2ObzofbkUgdMR0q/view?usp=sharing))<br> ([Thread and multiprocessor slides](slides/scheduling-threads.pdf)) ([Thread and multiprocessor video](https://drive.google.com/file/d/13lJ9VVV5YIS58rcNt20ap3gU24qXfK7p/view?usp=sharing)) | 6.3 - 6.5 | **Thursday 10/22** Project 1 due<br> **Wednesday 10/21** Lab 7 due<br>[Friday activity](activities/week-08-more-scheduling.md) (not due for credit)<br> [Some activity answers](activities/limited-answers/week-08-more-scheduling.md) |
|  9   | Memory management<br> ([Memory intro](https://drive.google.com/file/d/1R455TxZT6Dv7nb99WxdUeI8A9bi9Hmtt/view?usp=sharing)) ([slides](slides/memory-intro.pdf))<br> ([Virtual addresses](https://drive.google.com/file/d/1b9vMK8q2t6edOSroRcUsiHXZve6K-7HN/view?usp=sharing)) ([slides](slides/memory-addresses.pdf))<br> ([Linking and Loading](https://drive.google.com/file/d/1m18nXvnE1iflFSMe3MOVrEP_cGMidgif/view?usp=sharing)) ([slides](slides/memory-loading-linking.pdf))<br> ([Swapping](https://drive.google.com/file/d/1BShDuDLly13ELjr6dlWvJ3opkfhgMeCY/view?usp=sharing)) ([slides](slides/memory-swapping.pdf)) <br> ([Contiguous allocation](https://drive.google.com/file/d/16z_ldlUuDyv5iDEKQZOZtV8KkEZxsXp4/view?usp=sharing)) ([slides](slides/memory-contiguous.pdf))<br> ([Fragmentation](https://drive.google.com/file/d/1hxEp9NI4RQM5riE37hvj2tTmPyfKVYLm/view?usp=sharing)) ([slides](slides/memory-fragmentation.pdf))  | 7.1 - 7.3 | **Midterm Exam** Friday, October 30 |
|  10  | Segmentation<br>([video](https://drive.google.com/file/d/1qqfDSZghsmlCanYOlgF9qTS6Dalb_AIR/view?usp=sharing)) ([slides](slides/memory-segmentation.pdf))<br> Paging<br>([intro video](https://drive.google.com/file/d/1vwapmHhPPs92xNWThaCODrpaNxem9Qgv/view?usp=sharing)) ([intro slides](slides/paging-intro.pdf))<br>([details video](https://drive.google.com/file/d/1EDLmTewIPg6xN7_Ajy6ln5--KrzyTobK/view?usp=sharing)) ([details slides](slides/paging-details.pdf))<br>([TLB video](https://drive.google.com/file/d/1PodEYDIrLmkY497QcgV3bAoWqxUNFx9b/view?usp=sharing)) ([TLB slides](slides/paging-tlb.pdf))<br>([table structure video](https://drive.google.com/file/d/1KrTgJ3tfYmlngMxakN0NqZwG4CxY8YaL/view?usp=sharing)) ([table structure slides](slides/paging-table.pdf)) | 7.4 - 7.6 | [Friday activity](activities/week-10-memory.md) (not due for credit)<br> [Some activity answers](activities/limited-answers/week-10-memory.md) |
|  11  | Virtual memory<br> ([intro](https://drive.google.com/file/d/1z276tibNOce4ayofCTIwpCHOZOxmnSPP/view?usp=sharing)) ([slides](slides/virtual-intro.pdf))<br>([Demand Paging](https://drive.google.com/file/d/1Hfiht-0J0UFOdKWL3dyiMmy5gqLZTQiH/view?usp=sharing)) ([slides](slides/virtual-demand-paging.pdf))<br>([Copy-on-Write](https://drive.google.com/file/d/1yVijXfVAXIDJCTTJwVUZTqSUNB-PtaC5/view?usp=sharing)) ([slides](slides/virtual-copy-on-write.pdf))<br> Memory performance<br>([Performance](https://drive.google.com/file/d/1oXq6rdaMT97_CNd9Dda8lk1BUtWfVJ4E/view?usp=sharing)) ([slides](slides/virtual-access-time.pdf))<br> Page replacement concepts<br>([Replacement](https://drive.google.com/file/d/1UmUq20SbK9MCCqiZzD8rM3xAYbEHBd1Q/view?usp=sharing)) ([slides](slides/virtual-replacement.pdf))<br> Page replacement algorithms<br>([FIFO](https://drive.google.com/file/d/1HwHqi1EioxlVYcQrJgEv1duttQbIhM_j/view?usp=sharing)) ([slides](slides/virtual-fifo.pdf)) <br>([OPT and LRU](https://drive.google.com/file/d/1eccbIBY2aU_tl8lMA-bHZSNRtWa1Z8t5/view?usp=sharing)) ([slides](slides/virtual-opt-lru.pdf)) <br>LRU Implementation<br>([Implementation](https://drive.google.com/file/d/1DXpbB0CYBFlxmSqp71-DZIEDleEc7gkR/view?usp=sharing)) ([slides](slides/virtual-lru-implement.pdf)) <br>([LRU approximation (more bits)](https://drive.google.com/file/d/1TUYg61wXh5eUwQgL0eunxp6S3Wnu4Bj2/view?usp=sharing)) ([slides](slides/virtual-lru-more-bits.pdf)) <br>([LRU approximation (second chance)](https://drive.google.com/file/d/1N3tCS71s_GmXyypnI_oe802lj7HWOsv_/view?usp=sharing)) ([slides](slides/virtual-lru-second-chance.pdf))<br>Page Buffering<br>([Page Buffering](https://drive.google.com/file/d/1dNnrJg4M0CfhGKiIf_ke49HdJXx3UdIv/view?usp=sharing)) ([slides](slides/virtual-page-buffering.pdf)) | 8.1 - 8.4 | **Wednesday 11/11** Lab 8 due<br>[Friday activity](activities/week-11-virtual.md) (not due for credit) |
|  12  | Frame allocation<br>([video](https://drive.google.com/file/d/1EYqRvlznDJACkJfdyULirZLjVM_OOACg/view?usp=sharing)) ([slides](slides/virtual-frame-allocation.pdf))<br> Thrashing<br>([video](https://drive.google.com/file/d/1tLP1zeJbLcK5VmYrkvIXQUfWwePiLgen/view?usp=sharing)) ([slides](slides/virtual-thrashing.pdf))<br>([avoidance](https://drive.google.com/file/d/104T1BkSU-Kw9ZrHHn4Q9w_rDgwW6EkcT/view?usp=sharing)) ([slides](slides/virtual-models.pdf))<br>Memory mapping<br>([video](https://drive.google.com/file/d/1f9cMEw_Zx0dudQE3RbzxkXL_ieQooiKT/view?usp=sharing)) ([slides](slides/virtual-mmap-files.pdf)) | 8.5 - 8.10 | **Wednesday 11/18** Lab 9 due<br>[Friday activity](activities/week-12-more-virtual.md) (not due for credit) |
|      | Virtual Memory Misc.<br>([video](https://drive.google.com/file/d/1MlicCx22tpR4Dd2T-tsbagD-o4bWvQYP/view?usp=sharing)) ([slides](slides/virtual-misc.pdf))<br>Thanksgiving break 11/25 - 11/29 | | **Tuesday 11/24** Project 2 due  |
|  14  | File system concepts<br>([files](https://drive.google.com/file/d/1M1eTB2E03EY9PVmYvFPMre_WaS7r38-h/view?usp=sharing)) ([slides](slides/storage-files.pdf))<br>([directories](https://drive.google.com/file/d/1Ug8539QIGVs9h3cebi5J8-e4bnzjD3Yv/view?usp=sharing)) ([slides](slides/storage-directories.pdf))<br>([links](https://drive.google.com/file/d/1hd4_zBtyBwE3YneOvkqQwuxmIf3Ngg_W/view?usp=sharing)) ([slides](slides/storage-links.pdf))<br>([directory implementation](https://drive.google.com/file/d/1e7dY3zZR0w6hVQyagTKaEtbdTO4tt-bN/view?usp=sharing)) ([slides](slides/storage-implement-directories.pdf))<br>File system allocation<br>([contiguous allocation](https://drive.google.com/file/d/1pgfhacm3hi06RfYqh0ARIVNhtf0YoSBD/view?usp=sharing)) ([slides](slides/storage-allocation-contiguous.pdf))<br>([linked allocation](https://drive.google.com/file/d/1KlXgQZknzA14x5m6pXHJN5rJSxOJvoE_/view?usp=sharing)) ([slides](slides/storage-allocation-linked.pdf))<br>([indexed allocation](https://drive.google.com/file/d/10nlWYa8_p7rzm5GLyfrENTiUHrxbaMaS/view?usp=sharing)) ([slides](slides/storage-allocation-index.pdf)) | Chapter 10<br>Chapter 11<br>Chapter 9 |**Wednesday 12/02** Lab 10 due<br> [Friday activity](activities/week-14-processes.md) (not due for credit) |
|  15  | Protection and security | | |
|  16  | **Final Exam** | | |
