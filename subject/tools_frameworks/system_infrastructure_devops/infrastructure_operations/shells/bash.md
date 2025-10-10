---
title: bash
tags: ["terminal","sh","linux","ubuntu","cli","command line"]
---

## Commands

### Commonly Used

#### `source`

> A shell built-in command used to read and execute content of a file within the current shell environment. It is synonymous with the dot (.) command.

- syntax: `source filename [arguments]`
  - Syntax Explanation
    - filename: The path to the script or file containing the commands to be executed.
    - [arguments]: Optional arguments that become the positional parameters ($1, $2, etc.) within the sourced script. If no arguments are provided, the positional parameters of the current shell remain unchanged.
  - Examples
    - Consider a file named my_vars.sh with the following content:
  
      ```bash
      #!/bin/ bash
        MY_VARIABLE="Hello from sourced script  "
        my_function()   {
            echo "This is a function from the sourced script."
        }
      ```

    - To make MY_VARIABLE and my_function available in your current terminal session:
  
      ```bash

        source my_vars.sh
        echo $MY_VARIABLE
        my_function

      ```

    - This will be Ouptut

      ```bash

          Hello from sourced script
          This is a function from the sourced script. 

      ```

- Notes
  - Execute script in current shell: Unlike directly executing a script (e.g., ./myscript.sh), which creates and runs in a subshell, `source` executes the script's commands directly within the current shell session. This means any variables, functions, or aliases defined in the sourced script become available in the current shell.
  - Load configuration files: It is commonly used to load configuration files like .bashrc or .profile, .bash_profile, or .zshrc to set up environment variables, aliases, and functions for the user's shell session.
  - Activating virtual environments: In Python, it's used to activate virtual environments by sourcing the activate script, which modifies the PATH and other environment variables to point to the virtual environment's executables.
  - Share functions and variables: It allows you to define functions or variables in one file and then make them accessible in other scripts or directly in the terminal by sourcing that file.
  - `source` is not non-standard (POSIX) extension. 

### Rarely Used

## How to

### Script

#### Write all files in a directory to a file

1. Visible Files: `ls > input.txt` && Including hidden files (those starting with dot): `ls -a > input.txt`
   1. Explanation:
      1. `ls`: This command lists the contents of the current directory.
      2. `>`: This is the redirection operator, which sends the standard output of a command to a specified file. If the file already exists, its content will be overwritten.
      3. `input.txt`: This is the name of the file where the list fo files will be saved.
   2. Modifications
      1. Long Format: To list them in the long format (with details like permissions, size, modifications date) add `l` option/flag.
         1. Example: `ls -l > input.txt`
      2. To list files recursively (including files in subdirectories):
         1. Example: `ls -R > input.txt`

### Config

#### Change terminal editor mode

- By default bash terminal runs in Emacs settings, leading to the keybindings and shortcuts same like Emacs editor. If one wants, can switch to the Vi shortcuts instead
  - Set vi mode in bash:
    - set -o vi
  - Set Emacs Mode in bash:
    - set -o emacs

#### Bash POSIX Mode

> The --posix option in Bash forces the shell to adhere more closely to the POSIX standard. While Bash is largely POSIX-compliant, it includes extensions and default behaviors that can deviate from the standard.

- Activate POSIX Mode
  - `bash --posix` Or `set -o posix`

## Interesting Bit

### Why Bash shortcuts are like emacs editor shortcut?

> Because Bash's command-line editing is handled by the GNU Readline library, created by Brian Fox, who was also an Emacs hacker.

## Git - Bash

### Git-Bash Notes

1. Window commands work properly. Like in the case of wsl let's say start "" [file] won't work. But here it does and many others. So it extremely useful and convenient that you can work like bash use window like bash and be in the bash. Although in wsl also cmd or powershell command can be run after invoking them but not directly.


## Bash Keyboard Shortcuts (Emacs Settings)

### Moving

| command  | description                    |
|----------|--------------------------------|
| ctrl + a | Goto BEGINNING of command line |
| ctrl + e | Goto END of command line       |
| ctrl + b | move back one character        |
| ctrl + f | move forward one character     |
| alt + f  | move cursor FORWARD one word   |
| alt + b  | move cursor BACK one word      |
| ctrl + xx | Toggle between the start of line and current cursor position |
| ctrl + ] + x	 | Where x is any character, moves the cursor forward to the next occurance of x |
| alt + ctrl + ] + x  | Where x is any character, moves the cursor backwards to the previous occurance of x |

### Edit / Other

| command  | description                    |
|----------|--------------------------------|
| ctrl + d          | Delete the character under the cursor |
| ctrl + h          | Delete the previous character before cursor |
| ctrl + u          | Clear all / cut BEFORE cursor |
| ctrl + k          | Clear all / cut AFTER cursor |
| ctrl + w          | delete the word BEFORE the cursor |
| alt + d           | delete the word FROM the cursor |
| ctrl + y          | paste (if you used a previous command to delete) |
| ctrl + i          | command completion like Tab
| ctrl + l          | Clear the screen (same as clear command) |
| ctrl + c          | kill whatever is running |
| ctrl + d          | Exit shell (same as exit command when cursor line is empty) |
| ctrl + z          | Place current process in background |
| ctrl + _          | Undo |
| ctrl + x ctrl + u	| Undo the last changes. ctrl+ _ does the same |
| ctrl + t          | Swap the last two characters before the cursor |
| esc + t           | Swap last two words before the cursor |
| alt + t           | swap current word with previous |
| esc + .           | |
| esc + _           | |
| alt + [Backspace] | delete PREVIOUS word |
| alt + <           | Move to the first line in the history |
| alt + >           | Move to the end of the input history, i.e., the line currently being entered |
| alt + ?           | display the file/folder names in the current path as help |
| alt + *           | print all the file/folder names in the current path as parameter |
| alt + .           | print the LAST ARGUMENT (ie "vim file1.txt file2.txt" will yield "file2.txt") |
| alt + c           | capitalize the first character to end of word starting at cursor (whole word if cursor is at the beginning of word)|
| alt + u           | make uppercase from cursor to end of word |
| alt + l           | make lowercase from cursor to end of word |
| alt + n           | |
| alt + p           | Non-incremental reverse search of history. |
| alt + r           |Undo all changes to the line|
| alt + ctl + e     |Expand command line. |
| ~[TAB][TAB]       | List all users |
| $[TAB][TAB]       | List all system variables |
| @[TAB][TAB]       | List all entries in your /etc/hosts file |
| [TAB]             | Auto complete |
| cd -              | change to PREVIOUS working directory |

### History

| command  | description                    |
|----------|--------------------------------|
| ctrl + r          | Search backward starting at the current line and moving 'up' through the history as necessary |
| crtl + s          | Search forward starting at the current line and moving 'down' through the history as necessary |
| ctrl + p          | Fetch the previous command from the history list, moving back in the list (same as up arrow) |
| ctrl + n          | Fetch the next command from the history list, moving forward in the list (same as down arrow) |
| ctrl + o          | Execute the command found via Ctrl+r or Ctrl+s |
| ctrl + g          | Escape from history searching mode |
| !!                | Run PREVIOUS command (ie `sudo !!`) |
| !vi               | Run PREVIOUS command that BEGINS with vi |
| !vi:p             | Print previously run command that BEGINS with vi |
| !n		            | Execute nth command in history |
| !$		            | Last argument of last command |
| !^		            | First argument of last command |
| ^abc^xyz	        | Replace first occurance of abc with xyz in last command and execute it |