#CompSci 

# Operating System (OS)
## Functions of an Operating System
- File handling
- Input/Output control
- System security
- Interrupt Handling Routines
- Real-time Processing
- Memory Management
- Processor Management
- Human-Computer Interface
- Multitasking
- Multiprogramming
- Batch Processing
- Error Handling
- Loading/Running Software
- Managing User Accounts

## Layers
Operating systems are structured in the form of layers.
![[Pasted image 20220920101919.png]] #Todo draw diagram.

Each layer only communicates to adjacent, connected layers.

## Types of Operating Systems
### Distributed Operating System
Offers a parallel processing system by sharing the load over multiple servers that are interlinked.

A jobs is vided into simple tasks and each task is sent to a computer in the network.

For a user, it appears as if the job is processed on a single system.

### Multi-user, multi-tasking
Each user is allocated a time slice in a [[Operating System#Round Robin|Round Robin]]. The number of time slices may vary in some systems depending on the priority of tasks.

### Embedded Operating System
No permanent storage is provided. Embedded systems accept input from the sensors, processes and it sends output to control devices.

### Real-time Operating System (RTOS)
Critical systems are systems that must be highly reliable, as their failure may have a great impact on human lives.

Fault tolerance is a property that enables a system to operate properly even if the system undergoes one or more failures.

This type of operating system implements redundancy. Critical parts of a computer system are duplicated to improve reliability. If the primary system fails, the backup or reserve system steps in.

## Human-Computer Interface (HCI)
![[Pasted image 20220920102600.png]]
### Graphical User Interface (GUI)
Users are provided with an interactive, graphical environment based on icons and menus.

Smartphones typically use GUIs that users interact with via a touchscreen.

## BIOS (Basic Input/Output System)
Software that is responsible for executing a Power On Self Test (POST).

A BIOS chip will be present in the motherboard of a computer. BIOS setup can be modified once the computer is turned on.

## Managing the [[Central Processing Unit|CPU]]
1. Program is found in the secondary storage.
2. Section of [[Random Access Memory|RAM]] is allocated for the program and its data.
3. Program is copied form the storage drive to RAM.
4. [[Program Counter]] is now set to the memory location.
5. Program is executed.

## Multitasking
An operating system can execute multiple programs concurrently. Multiple programs may be copied to RAM but only one will be process at a particular instant (unless [[Parallelization|parallelization]] is introduced).

These programs could be in any of the following three states:
- Running.
- Waiting.
- Ready (runnable).

![[Pasted image 20220920103632.png]] #Todo draw diagram.

## Processor Scheduling
A module in an operating system that ensures that processor time is used efficiently.

In a multi-user network, the task of the scheduler is complex because multiple users can be running multiple programs.

### Algorithms
#### First Come, First Served (FCFS)
FCFS works as if all jobs are placed in a [[Queue|queue]]. The jobs are processed in the order of their arrival.

#### Shortest Job First
The job that is expected to be completed in the lowest amount of time is executed first. Thereafter, jobs are processed in the order of execution time.

#### Round Robin
Jobs are considered on a first in, first out basis. Each jobs is allocated a time slice which is a limited amount of CPU time.

If a job is not completed within a time slice, the next jobs is processed.

An interval timer is responsible for generating interrupts at specific time intervals to put the current job on hold and process the next one in queue at the end of each time slice.

A job is put on hold if a higher priority interrupt occurs.

Some systems are designed to process high-priority tasks with additional time slices in each round.

![[Pasted image 20220920104407.png]] #Todo Draw Diagram.

#### Shortest Remaining Time
The process which is expected to be completed in the shortest remaining time is executed next.

#### Multiple-Level Feedback Queues
Processes are separated into different categories based on their need for the processor and the jobs are placed in different queues.

Jobs may be transferred between queues.

This algorithm gives greater importance short jobs and jobs that require interaction with I/O devices.

Speed of I/O devices is slower than that of a processor, thus, this algorithm tries to keep the I/O devices as busy as possible.

When a job is using an output device, the other jobs requiring that output device may complete their processing with the processor.

## Memory Allocation
Operating systems may use both of the following methods to manage memory.
### Segmentation
Instructions and related data for a process are stored in memory in chunks coherent with the total memory requirement for that process. **RAM is split up unevenly**.

### Paging
Memory can be split into equally sized blocks called pages.

The information regarding which page is allocated to which process is maintained in a table.

Some space can be lost. However, data is read more efficiently.

## Virtual Memory
When a computer has too many processes running concurrently and the capacity of RAM is not sufficient, a section of secondary storage is allocated as the paging file for virtual memory.

### Swapping
The process by which the operating system moves data between RAM and virtual memory.

![[Pasted image 20220920113758.png]] #Todo draw diagram.

## Interrupt Service Routine (ISR)
![[Pasted image 20220920114908.png]]