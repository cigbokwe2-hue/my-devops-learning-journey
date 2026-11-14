# Linux — LFS101 Chapter 10: File Operations

## Notes
### Filesystems

- On Linux, all of your files and directories are organized into a single tree. Starting from a single point at the top called the root directory, represented simply by a forward slash (/).

- A partition is a section of a physical disk that has been set aside to be used as a self-contained unit. A single hard drive or SSD can be divided into several partitions, and, in most cases, each partition holds one filesystem.
    - EFI System Partition (ESP): A small partition mounted at /boot/efi, required so that UEFI-based computers can boot the system.
    - The root partition: This is the main partition holding the operating system, applications and system files.
    - Swap space: This is the virtual memory overflow. The system moves less active data to swap when memory is filled up.

- Mount points: This is the place where a filesytem is attached to the tree. A mount point is a normal directory which takes you to the mounted filesytem when you navigate to it. 

- Mounting and Unmounting: To mount a partition, we use the mount command by giving two arguments, the device node and the mount point, eg: sudo mount /dev/sda5 /home. THis mounts the sda5 partion to /home.  
    - sudo mount /dev/sda5 /home
    - sudo umount /home
    - df -Th : this shows each mounted filesystem along with its type and how much space is used and available

- NFS (Network Filesystem): Network filesystems let separate machines share the same files seamlessly, all within the familiar single-tree model.

### Important directories
- /home: This contains each user's personal directory to store their personal files
- /root: This is the root user's personal home directory
- /bin: This holds essential command programs, including commands like; cat, cp, ls, etc
- /sbin: This holds essential programs for system administration
- /usr: This is where the user-facing programs and their supporting files live.
- /usr/local: This holds manually insatlled softwares
- /usr/lib: This holds supporting code libraries that system programs need
- /etc: This holds system wide configuration files
- /var: holds variable files that are expected to grow and change as the system runs.
- /proc: A psuedo-filesystem that exposes live system information generated on the fly by the kernel, in memory and presented as files.
    - /proc/cpuinfo — details about the CPU
    - /proc/meminfo — current memory usage
    - /proc/version — the running kernel and OS release information
    - /proc/mounts — the filesystems currently mounted (you used this in Lab 10.1)
    - /proc/<PID> — a directory for every running process, named by its process ID (the same PIDs you saw in ps and top sections in the previous chapter), containing live details about it
- /dev: This contains files that represent devices and hardware attached to the system (device nodes)
- /boot: This contains all the computer's boot-files
- /media: This is where removable media like usb, sd-cards, etc are mounted automatically by the desktop
- /run: This is a memory-based area for runtime data that programs need while the system is running 
- /mnt: This is a traditional, generic spot for temporarily mounting a filesystem by hand.
- /tmp: For temporary files that can be deleted automatically on reboot
- /opt: For optional, self-contained third-party software, often commercial applications that install everything in one place.
- /sys: Like /proc, this is a pseudo-filesystem exposing information about devices and the kernel.

### Working with files
- diff - This is the tool for comparing two textfiles and track changes.
- patch - This updates an older file to match the newer one
- diff3 - This compares three files at once
- file - This examines a file and tells what type of file it is.

### Backup and compression
- cp - Used for creating simple local duplicate
- rsync - Used for synchronizing directory trees or backing up over a network.
