# UNIX Journey Workshop:

### Table of Content:
- [1. What is UNIX?](#1-what-is-unix-?)
- [2. History of UNIX?](#2-history-of-unix)
- [3. UNIX Architecture](#3-unix-architecture)
  - [3.1 Kernel](#31-kernel)
  - [3.2 shell](#32-shell)
  - [3.3 Programs](#33-programs)
- [4. Why use UNIX?](#4-why-use-unix)
- [5. UNIX File system](#5-unix-file-system)
  - [5.1 Quick notes](#51-quick-notes)
  - [5.2 The File system Hierarchy](#52-the-file-system-hierarchy)
- [6. Basic commands](#6-basic-commands)
  - [6.1 Command Structure](#61-command-structure)
  - [6.2 Common commands](#62-common-commands)
- [7. process](#7-process)
  - [7.1 what is a process?](#71-what-is-a-process)
  - [7.2 what processes are running?](#72-what-processes-are-running-now)
  - [7.3 multitasking](#73-multitasking)
  - [7.4 kill process](#74-kill-processes)
  - [7.5 top](#75-top)
- [8. Jobs](#8-jobs)
- [9. Packages](#9-packages)
  - [9.1 compression](#91-compression)
  - [9.2 install Packages](#92-install-packages)

# 1. What is UNIX?
  - Unix is on of the first widely-used operating systems.

  - Is the basis for many modern Operating systems.

  - Helped set a standard for the multi-tasking multi-user systems

# 2. History of UNIX
- 1969 Ken Thompson, Dennis Ritchie start working on a file
system, and name their system UNICS, which is later changed
to [UNIX](https://www.youtube.com/watch?v=JoVQTPbD6UY).

- 1973 Thompson and Ritchie rewrote UNIX in C (while most of the
operating systems at that time were written in assembly)

- 1991 Linux, GNU, and others: similar to UNIX, but their source
code rewritten, very popular and widespread, free.
__<sub>(Many Linux Distributions: Ubuntu, Fedora, Debian, ...)<sub>__

# 3. UNIX Architecture
### 3.1 Kernel:
The part manages and controls the machine and takes care of scheduling of various computer Programs

### 3.2 Shell:
A command interpreter that looks after the communication between the user and the system.

### 3.1 Programs:
various utility Programs which performs a number of tasks (editing a file,  sorting numbers or drawing a plot, .....)


# 4. Why use UNIX?
- Allows you to accomplish and automate complicated tasks that would usually require huge manual labor.

- A rich set of small commands and utilities that can be
combined in unlimited ways to perform complex custom tasks.

- __It is fun!__

- Not limited to pre-configured combinations or menus, as in
personal computer systems.

- Extremely useful computer skill that will be relevant many years from now.

# 5. UNIX File system

## 5.1 Quick notes:
-  the unix file system consists of one single global root directory that encapsulates everything of the machine. no matter how many disks or volumes are there.

- Files and directories names are case sensitive.

- The way to separate directories is with a forward slash "/".


## 5.2 The File system Hierarchy:
- __Root__ : Main & parent Directory

- __/home__: contains all the users and the user data and files

- __/dev__ : Access to hardware devices

- __/lib__ : Stores the libraries

- __/mnt__ : is used to mount disk drives

- __/usr__ : user installed Programs and files

- __/etc__ : system Settings


# 6. Basic commands:

#### 6.1 Command Structure:
Command [opt1] [opt2]

#### 6.2 Common commands:

- print working directory __*(pwd)*__:
  - Prints the full path of the current directory

  - Very handy when you get lost in the directories jungle

  - A useful variable for the strings


-  list _**(ls) [flags] <file\>**_ :
  - Lists the content of the current directory.

  ##### common options:

  **' - l '** => List a detailed file/folder information.

  **' - lh '** => List a detailed file/folder information.

  **' - a '** => list hidden files.

  **' - ls '** => sort files by size.

- change directory _**(cd) <directory name\>**_:
  - goes from the current directory to the specified one.

  - defaults to the _**home**_ directory if not given a destination.

  - can take both absolute or relative paths.

  **relative:**
  the location of a file or a folder that beginning at the current directory.

  ```shell
  cd csc1101
  ```

  **absolute:**
  the location of a file or a folder starting at  <sub>__*(home directory)*__<sub>
  ```shell
  cd /home/user1/csc1101
  ```

  ##### shortcuts:
  **' ~ '** => Current user's home directory.

  **' . '** => The current directory.

  **' .. '** => The parent of the current directory.

  **' - '** => The previous directory.

- Make a file __*(touch) [flag] <file\>*__:
  - creates a new file with the name <file>
  - Adjusts the timestamp of <file>

- Make Directory __*(mkdir) [flags] <directory\>*__ :

  - makes a new directory with the name <directory>

  - can use relative and absolute paths to make directories outside the current directory.

  ##### common options:
  **' - p '** => creates parent folders as well.

- Remove File __(rm) [flags] <file\>__
  - removes the file called <file>
  - Using wildcards you can remove multiple files.

  ##### common options:
  **' - i '** => prompt before removal.

  **' - f '** => force remove.

  **' - r '** => recursively remove all files in a directory.

- Remove Directory __(rmdir) [flags] <directory\>__
  - removes an empty directory <directory\>.
  - Throws error if the directory is not empty.

  ##### common options:
    **' - p '** => removes folder and its ancestors.

- Copy __(cp) [flags] <file\> <destination\>__
  - copies <file> from location to <destination\>

  - to copy multiple files you can use wildcards (such as * )

- Move __(mv) [flags] <file\> <destination\>__
  - Moves a file or directory from one place to another

  - Also used for renaming, just move from <oldname\> to
<newname\>

- File type __(file) <file\>__
  - will show you a description of the file’s contents.

- Find File __(find) <starting point\> <type\> <name\>__
  - looks through any sub-directory to find a file

- Locate File __(locate) [flag] <name\>__
  - similar to find
  - no need to specify a starting directory (it searches the system)

  ##### common options:
    **' - n '** => limit the result to 20 entries.

    **' - c '** => count the number of results.

- current user __(whoami)__
  - prints the name of the current user.

- __(which)__
  - used to locate the executable file associated with the given command.


# 7. Process
### 7.1 What is a process?
- An instance of a running program.

- More specific than a program

- Each process is given a unique id (PID)

### 7.2 What processes are running now?
- process screenshot __(ps) [flags]__
  - Reports a snapshot of the current running processes, including
PIDs
  - Lists the processes created by the user in the current terminal

  ##### common options:
    **' - e '** => every process currently running.

    **' - u user'** => processes created by this user.

### 7.3 Multitasking
- Quick switching back and forth between processes makes it
seem as though they are all running simultaneously.

- Each process has a priority that can be set and changed by the user.

- priorities range from -20(highest) to 19(lowest), if process is started with out a priority defaults to 0

- nice process __(nice) [flags] <command\>__
  - starts a process with the set priority.

  - if priority is not set default is 10

  - only root user can set priority below 0


  ##### common options:
  **' - n '** => priority.


- renice process __(renice) [flags] <PID\>__
  - changes the priority of a running process.

  - can change the processes created by this user only

  - only root user can set priority below 0
  ##### common options:
  **' - n '** => priority.

### 7.4 Kill processes
- kill process __(kill) <PID\>__
  - Kills the process with this ID.

- kill all processes __(killall) [flag] <Process name\>__
  - Kills all the processes of the current program.

  ##### common options:

  **' - TERM '** => Terminates execution (default).

  **' - HUP '** => Hang-up (restarts the program).

  **' - KILL '** => Like bleach, can kill anything.

### 7.5 TOP
- running processes __(top)__
  - All in one stop for process management

##### common options:

**' h '** => Help menu.
**' Z '** => Set colors.
**' k/K '** => Kill a Process.
**' r '** => renice.

# 8. Jobs
- Check jobs __(jobs)__
- Prints the current jobs with details and job id.

- resume job __(bg) <ID\>__
  - Restart a stopped background process.

- foreground __(fg) <ID\>__
  - Bring a background process to the foreground.

- kill job __(kill) %<ID\>__
  - kills the job with the given id.

# 9. Packages

### 9.1 Compression
- compress file __(gzip) <file\>__
  - can compress a single file.
  -  doesn't create a new compressed file
  - compresses the file into a ".gz" archive.

- decompress file __(gunzip) <file\>__
  - decompresses the file.

- compress file __(tar) cvf <file name\> <source file\>__
  - compress as full directories.
  - creates a new copy that is compressed.
  - compresses the file into a ".tar" archive.

  - "c" => create
  - "v" => verbose / show progress
  - "f" => file name

- decompress file  __(tar) xvf <file\>__
  - decompresses the file.

  - "x" => extract
  - "v" => verbose / show progress
  - "f" => file name

### 9.2 install packages
- Debian package management __(apt) [option] <package name>__
  - manages the packages on the device.

  #### options:
    - "install" => installs a package
    - "remove" => removes a package
    - "show"  => shows the details of a package
