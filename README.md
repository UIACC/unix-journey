# UNIX Journey Workshop:

### Table of Content:
[1. What is UNIX?](#1-what-is-unix-?)

# 1. What is UNIX?
  - Unix is one of the first widely-used operating systems.

  - Is the basis for many modern Operating systems.

  - Helped set a standard for the multi-tasking multi-user systems

# 2. History of UNIX
- 1969 Ken Thompson, Dennis Ritchie (et al.) start working on a file
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

- Not limited to preconfigured combinations or menus, as in
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

- print working directory __*(pwd)*__:
  - Prints the full path of the current directory

  - Very handy when you get lost in the directories jungle

  - A useful variable for the strings


-  list __*(ls) [flags] [file] *__ :
  - Lists the content of the current directory.

  ##### common options:

  **' - l '** => List a detailed file/folder information.

  **' - lh '** => List a detailed file/folder information.

  **' - a '** => list hidden files.

- change directory _**(cd) [directory name]**_:
  - goes from the current directory to the specified one.

  - defaults to the _**home**_ directory if not given a destination.

  - can take both absolute or relative paths.

  **relative:**
  the location of a file or a folder that beginning at the current directory.

  ```shell
  cd csc1101
  ```

  **absolute:**
  the location of a file or a folder starting at /  <sub>__*(home directory)*__<sub>
  ```shell
  cd /home/user1/csc1101
  ```

  ##### shortcuts:
  **' ~ '** => Current user's home directory.

  **' . '** => The current directory.

  **' .. '** => The parent of the current directory.

  **' - '** => The previous directory.

- Make a file __*(touch) [flag] [file]*__:
  - creates a new file with the name [file]
  - Adjusts the timestamp of [file]

- Make Directory __*(mkdir) [flags] \<directory\>*__ :

  - makes a new directory with the name <directory>

  - can use relative and absolute paths to make directories outside the current directory.

  ##### common options:
  **' -p '** => creates parent folders as well.

- Remove File __(rm) [file]__
