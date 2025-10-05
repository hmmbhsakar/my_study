---
title: "POSIX"
canonical_path: "subject/computer_science/operating_systems/standards_specifications/posix.md"
tags: [os, posix, unix, api, standard]
related: ["ISO C", "Filesystems", "Threads (pthreads)"]
---
# POSIX — TL;DR

One-sentence summary...

## Scope

- system calls, libc interfaces, shells & utilities, file semantics, signals

## Key topics

- process model, fork/exec, file descriptors, signals, pthreads, shell behavior

## Known deviations (Linux, macOS, *BSD)

-

## Commands

### dot (.) command

> The dot (.) command in a Unix-like shell, such as Bash or Zsh, is a built-in command used to execute a script or function within the current shell environment. This means any changes made by the script, such as setting environment variables (export), changing the current directory (cd), or defining functions, will persist in the current shell session after the script finishes.
> No new process: Unlike executing a script with ./, the dot command does not create a new child process. This makes it more efficient for tasks where you need the script's effects to directly impact the parent shell.
> Relationship to source: In many shells, the `source` command is an alias or a more readable equivalent of the dot command. They perform the same function. But `source` isn't POSIX complaint

- Execution in the current environment: When you use . filename, the commands within filename are executed as if you typed them directly into the current interactive shell.
- References
  - [Dot Command Wiki](https://en.wikipedia.org/wiki/Dot_(command))