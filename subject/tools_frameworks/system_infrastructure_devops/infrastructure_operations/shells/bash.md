---
title: bash
tags: ["terminal","sh","linux","ubuntu","cli","command line"]
---

## Bash Keyboard Shortcuts (Emacs Settings)

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

### Change terminal editor mode

- By default bash terminal runs in Emacs settings, leading to the keybindings and shortcuts same like Emacs editor. If one wants, can switch to the Vi shortcuts instead
  - Set vi mode in bash:
    - set -o vi
  - Set Emacs Mode in bash:
    - set -o emacs

### Bash POSIX Mode

> The --posix option in Bash forces the shell to adhere more closely to the POSIX standard. While Bash is largely POSIX-compliant, it includes extensions and default behaviors that can deviate from the standard.

- Activate POSIX Mode
  - `bash --posix` Or `set -o posix`

## Interesting Bit

### Why Bash shortcuts are like emacs editor shortcut?

> Because Bash's command-line editing is handled by the GNU Readline library, created by Brian Fox, who was also an Emacs hacker.
