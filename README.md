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
|  2   | Process concepts ([video](https://drive.google.com/file/d/1n3ilpQX8KyHDUtj87oX6cbP1IOJXr7bM/view?usp=sharing)) <br>([slides](slides/process-intro.pdf))<br> Process scheduling ([video](https://drive.google.com/file/d/1WYDnm95IEsfCfJ2kWcPE7scQuXizDVE9/view?usp=sharing)) <br>([slides](slides/process-scheduling.pdf))<br> Process lifecycle ([video](https://drive.google.com/file/d/1tbuBorFMtNWtmOQeK16B1uJYTYGA-m5E/view?usp=sharing)) <br>([slides](slides/process-scheduling.pdf)) | 3.1 - 3.3 | **Wednesday 9/9** Lab 1 due<br> [Friday activity](activities/week-2-processes.md) (not due for credit) |
|  3   | Interprocess communication<br> ([IPC video](https://drive.google.com/file/d/1kCh0E5OL0bzsyNf-tJ2b0T-b6pefcgiW/view?usp=sharing)) <br>([IPC slides](slides/process-ipc.pdf))  ([POSIX shared mem video](https://drive.google.com/file/d/1UJgfiO-1bPmN0R957kgd826nRffuzSTI/view?usp=sharing)) <br>([POSIX shared mem slides](slides/process-shm-posix.pdf)) ([Message passing video](https://drive.google.com/file/d/1SAjg6wOCz3pDTArkJRr-5BThE0BvgOfQ/view?usp=sharing)) <br>([Message passing slides](slides/process-message.pdf)) ([Pipes video](https://drive.google.com/file/d/1kgkfqmPMQwbrNShlMj08Zp8B-_ZZJ-7w/view?usp=sharing)) <br>([Pipes slides](slides/process-pipes.pdf))<br> Threads ([Thread overview video](https://drive.google.com/file/d/1Bw4N-N9reZm5dVCAGQXUJt9CKyWoonNN/view?usp=sharing)) <br>([Thread overview slides](slides/thread-overview.pdf)) ([Thread models video](https://drive.google.com/file/d/1e2McBk8x9BFVd2JELAEfStVPyYIovnPS/view?usp=sharing)) <br>([Thread models slides](slides/thread-models.pdf)) ([Thread issues video](https://drive.google.com/file/d/10_FU4IGDHknFeLEHF8X_iD59Gm3jzFEQ/view?usp=sharing)) <br>([Thread issues slides](slides/thread-issues.pdf))<br> | Chapter 3<br> Chapter 4<br> [Video errata](misc/errata-ipc.md) | **Wednesday 9/16** Lab 2 due<br> [Friday activity](activities/week-3-ipc.md) (not due for credit) |
|  4   | Process synchronization ([Synchronization intro](https://drive.google.com/file/d/1aWbPVoawujS2awtlIoS_bu4Dug6XQLy0/view?usp=sharing)) <br>([slides](slides/parallel-intro.pdf))<br> Syncrhonization algorithms ([Synchronization algorithms](https://drive.google.com/file/d/1LhIMqdujkAiFuKegGND-1ltA3U5R0svl/view?usp=sharing)) <br>([slides](slides/parallel-critical-section.pdf))<br> File descriptors ([File descriptor video](https://drive.google.com/file/d/1b7xdFDowZUFI5tnhgpW5C_24XYfYMin8/view?usp=sharing)) <br>([slides](slides/file-descriptors.pdf)) | 5.1 - 5.3 | **Wednesday 9/23** Lab 3 due<br> [Friday activity](activities/week-4-threads.md) (not due for credit) |
|  5   | Synchronization hardware ([video](https://drive.google.com/file/d/1g0XJ3pv6zoKa3Sn06idw3irdSDj7DYX8/view?usp=sharing)) <br>([slides](slides/sync-hardware.pdf))<br> Mutex and Semaphores ([mutex video](https://drive.google.com/file/d/19S_o5uhz9J-MKFVC32FhHzsg3peb7OFX/view?usp=sharing)) <br>([mutex slides](slides/sync-mutex.pdf)) ([semaphore video](https://drive.google.com/file/d/1tV0t2zItgIM5Zi4jZscnET5sYfWD8w7I/view?usp=sharing)) <br>([semaphore slides](slides/sync-semaphore.pdf)) ([issues video](https://drive.google.com/file/d/1crE7PdCYtMypb39DXv4WmWVjgvvLKa_X/view?usp=sharing)) <br>([issues slides](slides/sync-issues.pdf))<br> Classic problems of synchronization ([video 1](https://drive.google.com/file/d/1qT1hJs_m2DVNj0NCnH1qDYAN70MyUa6q/view?usp=sharing)) <br>([slides 1](slides/sync-classic.pdf)) ([video 2](https://drive.google.com/file/d/19PtihgvsLgzl2zUDw9JSaOdpbJWg3ZAq/view?usp=sharing)) <br>([slides 2](slides/sync-philosophers.pdf)) | 5.4 - 5.7 | **Wednesday 9/30** Lab 4 due<br> [Friday activity](activities/week-5-synchronization.md) (not due for credit) |
|  6   | Monitors ([intro video](https://drive.google.com/file/d/16p3KPWMxOjjcxitI3krIeQ1Q_SzJ7-GJ/view?usp=sharing)) <br>([intro slides](slides/sync-monitor-intro.pdf)) ([usage video](https://drive.google.com/file/d/1r_CE8lQqJvD6NjRiu-opxd3NkudukZf1/view?usp=sharing)) <br>([usage slides](slides/sync-monitor-philosophers.pdf)) ([implementation video](https://drive.google.com/file/d/1J85TZO2lWbvx8Td7znXMpTDutgUX-JLp/view?usp=sharing)) <br>([implementation slides](slides/sync-monitor-implementation.pdf))<br> Deadlock ([deadlock criteria video](https://drive.google.com/file/d/1EcH7-ZIcuUWR7cBwAsLucRq-g9agQri-/view?usp=sharing)) <br>([deadlock criteria slides](slides/sync-deadlock-intro.pdf)) ([graphs video](https://drive.google.com/file/d/14LEIj4VEvIZ9WplGnFIacK27NUdZpX9R/view?usp=sharing)) <br>([graphs slides](slides/sync-deadlock-graph.pdf)) | 5.8, 5.11 | **Wednesday 10/7** Lab 5 due |
|  7   | CPU scheduling concepts, criteria, and metrics | | |
|  8   | Scheduling algorithms | | |
|  9   | Memory management | | **Midterm Exam** Friday, October 30 |
|  10  | Paging<br> Virtual memory<br> Memory performance | | |
|  11  | Page replacement concepts and algorithms | | |
|  12  | Frame allocation<br> Memory system design | | |
|      | Thanksgiving break 11/25 - 11/29 | | |
|  14  | File system concepts and implementation | | |
|  15  | Protection and security | | |
|  16  | **Final Exam** | | |
