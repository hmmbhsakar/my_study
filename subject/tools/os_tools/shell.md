# Shell

An interface that allows users to interact with an operating system by interpreting commands and executing them. It acts as a bridge between the human user and the system's core (the kernel), accepting human-readable instructions and translating them into actions the computer can understand. Shells can be command-line interfaces (CLIs) for typing commands or graphical user interfaces (GUIs) for point-and-click interaction.

## POSIX

POSIX: Portable Operating System Interface, is a family of standards for defining a standard operating system interface and environment, including a command interpreter (shell) and common utility programs, to ensure source code level portability of applications across different operating systems, particularly those derived from Unix.

### POSIX Commands

1.

### Notes

1. POSIX-compliant shell: A command-line interpreter that adheres to the Portable Operating System Interface (POSIX) standards.

## Bash

### Bash Commands

1. POSIX Mode
   1. bash --posix : initiates the Bash shell in a mode that strives for closer adherence to the POSIX standard for shell behavior.
2. Make Directory
   1. mkdir
      1. Options:
      2. -p  Or --parents: Create intermediate directories as needed.
3. Remove Directory
   1. rmdir
      1. Options:
      2. -r :

## Git- Bash

Since Most of the things of the git-bash and bash would be same so only the differentiation would be noted. Top Hirarcy is for POSIX, if a command is POSIX complaint command then it would be listed in the POSIX, eventually meaning that all the POSIX complaint shell would surely follow it.

### Git-Bash Commands

### Git-Bash Notes

1. Window commands work properly. Like in the case of wsl let's say start "" [file] won't work. But here it does and many others. So it extremely useful and convinient that you can work like bash use window like bash and be in the bash. Although in wsl also cmd or powershell command can be run after invoking them but not directly.

## CMD

### CMD Commands

1. Make directories
   1. mkdir
2. Delete directories
   1. rmdir
      1. Options:
      2. /s : All subdirectories and files within the specified directory in addition to the directory itself. Confirm deletion (if prompted): The system will typically ask for confirmation before proceeding with the deletion.
      3. /q : switch for "quiet mode" to suppress the confirmation prompt:
