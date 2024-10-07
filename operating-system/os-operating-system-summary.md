
# Operating System - Key Concepts Summary

## 1. Memory Management:
- Memory management involves managing the system's primary memory, ensuring efficient allocation and deallocation.
- **Paging:** Divides memory into fixed-size pages to eliminate external fragmentation. Each process is divided into pages, and these pages are loaded into available memory frames.
- **Segmentation:** Divides memory into segments of varying sizes, based on the logical structure of a program. Each segment can be loaded into different parts of memory, but this can lead to external fragmentation.
- **Virtual Memory:** Virtual memory extends physical memory by using disk space, allowing larger programs to run on systems with limited physical memory.
- **Demand Paging:** Pages are loaded into memory only when they are needed, reducing memory usage but introducing some delays due to page faults.

## 2. Process Management:
- A process is a program in execution, and process management is responsible for creating, scheduling, and terminating processes.
- **Process States:** New, Ready, Running, Blocked, and Terminated.
    - **New:** The process is being created.
    - **Ready:** The process is waiting for CPU time.
    - **Running:** The process is currently executing.
    - **Blocked:** The process is waiting for some event (e.g., I/O completion).
    - **Terminated:** The process has finished execution.
- **Process Control Block (PCB):** Contains information about the process, including its state, program counter, memory usage, and register values.

## 3. CPU Scheduling:
- CPU scheduling ensures that multiple processes can be executed efficiently, sharing CPU time.
- **Scheduling Algorithms:**
    - **Round Robin:** Each process is given an equal time slice of CPU time before switching to the next process.
    - **Priority Scheduling:** Processes with higher priority are scheduled before lower-priority processes.
    - **Shortest Job First:** The process with the shortest CPU burst time is executed first.
    - **First-Come, First-Served (FCFS):** Processes are executed in the order they arrive.

## 4. Synchronization and Deadlock:
- **Process Synchronization:** Ensures that multiple processes can access shared resources safely, avoiding race conditions.
    - **Semaphores:** A synchronization primitive that controls access to shared resources.
    - **Mutexes:** A lock that ensures mutual exclusion, where only one process can access a resource at a time.
- **Deadlock:** A situation where two or more processes are unable to proceed because they are each waiting for the other to release a resource.
    - **Deadlock Prevention:** Ensures that at least one of the necessary conditions for deadlock cannot occur (mutual exclusion, hold and wait, no preemption, circular wait).

## 5. Memory Allocation Strategies:
- **First Fit:** Allocates the first block of memory that is large enough for the process.
- **Best Fit:** Allocates the smallest block that fits the process to reduce wasted space.
- **Worst Fit:** Allocates the largest available block of memory to leave the most space for future processes.

## 6. Page Replacement Algorithms:
- **Page Replacement:** When memory is full, the operating system must replace a page to load a new one.
    - **FIFO (First-In-First-Out):** Replaces the oldest page.
    - **LRU (Least Recently Used):** Replaces the page that hasn’t been used for the longest time.
    - **Optimal:** Replaces the page that will not be used for the longest time in the future (theoretical).

## 7. File Systems:
- **File System Management:** Manages how data is stored and retrieved on storage devices like hard drives and SSDs.
    - **File Allocation Table (FAT):** A simple file system where a table is used to track the location of each file’s data on disk.
    - **NTFS (New Technology File System):** A more advanced file system used in Windows, supporting larger files, file compression, encryption, and better error recovery.
    - **Inode:** A data structure used in UNIX-like systems to store information about files and directories.

## 8. I/O Management:
- **I/O Management:** Responsible for controlling all input/output devices (e.g., keyboard, mouse, printer) and coordinating communication between the CPU and I/O devices.
    - **Buffering:** Temporarily storing data in memory while waiting for an I/O device to become available.
    - **Spooling:** Used in print management, where print jobs are queued in a buffer and processed sequentially.
    - **Device Drivers:** Software that allows the operating system to communicate with hardware devices.

## 9. Security and Protection:
- **Security Mechanisms:** Ensure that unauthorized users cannot access system resources or data.
    - **Authentication:** Verifying the identity of a user before granting access.
    - **Authorization:** Granting or denying access to system resources based on user permissions.
    - **Encryption:** Protecting data by converting it into a secure format that can only be read by authorized users.

## 10. Virtualization:
- **Virtualization:** The creation of virtual machines that run multiple operating systems on a single physical machine. It allows better utilization of hardware resources by sharing them among different virtual machines.
    - **Hypervisor:** A software layer that creates and runs virtual machines. Examples include VMware and KVM.