---
title: "Portable Operating System Interface (POSIX)"
canonical_path: "subject/computer_science/operating_systems/standards_specifications/posix.md"
tags: [os, posix, unix, api, standard]
related: ["ISO C", "Filesystems", "Threads (pthreads)"]
---
## POSIX — TL;DR

POSIX: Portable Operating System Interface, is a family of standards for defining a standard operating system interface and environment, including a command interpreter (shell) and common utility programs, to ensure source code level portability of applications across different operating systems, particularly those derived from Unix.

## Important Info

- [IEEE POSIX Standard Documentation](https://pubs.opengroup.org/onlinepubs/9799919799/)

## Scope

- system calls, libc interfaces, shells & utilities, file semantics, signals

## Key topics

- process model, fork/exec, file descriptors, signals, pthreads, shell behavior

## Commands

### Control Operators

- Using  `|` (pipe)
  - Called: pipe
  - Expressed by a vertical bar `|`
  - Use: Pass the output of the command on the left side of the pipe to the command on the right side of the pipe through a special connection.
  - Example
    - `who | wc -l`: counts the number of users currently logged into the system
      - `who`: This command being on the left of the pipe executes first. It prints a list of all users currently logged into the system, with each user on a new line. 
      - `|`(pipe): redirects the standard output of the command on the its left (the `who` here) to the standard input of the command on its right (the `wc` command).
      - `wc -l`: The `wc` command, which stands for "word count" reads form its input and, with `-l` option/flag, counts the number of lines. In this case, it receives the output of the `who` command and counts each line. 
  - Using `||` (or) 
    - Called: or
    - Expressed by two vertical bars `||`
    - Use: If the command on the left side of a `||` works, the one on the right side won't be run at all.
    - Notes
      - two vertical lines do not represent a double pipe. In fact they don't represent piping at all. 

### dot (.) command

> The dot (.) command in a Unix-like shell, such as Bash or Zsh, is a built-in command used to execute a script or function within the current shell environment. This means any changes made by the script, such as setting environment variables (export), changing the current directory (cd), or defining functions, will persist in the current shell session after the script finishes.
> No new process: Unlike executing a script with ./, the dot command does not create a new child process. This makes it more efficient for tasks where you need the script's effects to directly impact the parent shell.
> Relationship to source: In many shells, the `source` command is an alias or a more readable equivalent of the dot command. They perform the same function. But `source` isn't POSIX complaint

- Execution in the current environment: When you use . filename, the commands within filename are executed as if you typed them directly into the current interactive shell.
- References
  - [Dot Command Wiki](https://en.wikipedia.org/wiki/Dot_(command))

### `who` command

- Prints a list of all users currently logged into the system, with each user on a new line. 

### `awk ` command

### `sort` command

### `uniq` command

### `head` command

## Known deviations (Linux, macOS, *BSD)

-

## Interesting Bit

- Initially POSIX full form was Portable Operating System Interface for Unix, but now I saw just till interface almost everywhere. 
- 
