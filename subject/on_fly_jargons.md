# Jargons noted on Fly

- Git submodule
  - Note: Provide a mechanism to embed one Git repository within another Git repository as a subdirectory. This allows a project to incorporate and track the version history of external code, such as a third-party library or a shared component, while keeping the external code's history separate from the main project's history

- Systems Programming
  - Note: Seems like Programming the infra (operating system or bios or such).
- symlinks: Symbolic link
  - Note: A special type of file that functions as a shortcut, pointing to another file or directory (the "target") on the file system. It acts as a transparent redirection, allowing users and applications to access the target file or folder as if it were in the link's location. Symlinks are a common feature in operating systems like Linux and Windows and are used for tasks such as migrating applications, maintaining file version control, and managing cloud synchronization. 
- glibc: GNU C Library
  - A fundamental collection of C and C++ library functions that serves as a core component of the GNU/Linux operating system and many other Linux-based systems. It provides a portable and high-performance interface for applications to access system resources like files, memory, and network services by acting as a wrapper around system calls to the Linux kernel. Essential functions include file operations (open, read, write), memory management (malloc), and I/O functions (printf),
- musl
  - An efficient, lightweight, standards-conformant C standard library (libc) designed for Linux-based systems, known for its strong emphasis on simplicity, correctness, and security, making it ideal for static linking and resource-constrained environments like containers. It contrasts with glibc by minimizing abstractions, allowing for very small statically-linked binaries, and providing robust failure guarantees. 
- 