# LFS101 Chapter 8 — Finding Linux Documentation

Use this file for your own notes. Add to it as you learn.

## Key ideas

- The main sources of Linux documentation are
    - The man pages
    - GNU Info
    - The help command and --help option
    - Distribution -specific documentation

- 

## Documentation sources and lookup examples

- man
    - man ls
    - man -f <topic>: Lists available pages that match a name exactly. This is identical to the whatis command.
    - man -k <keyword>: Searches page descriptions for a keyword, finding related pages even when the word isn't in the command name. This one is identical to the apropos command.
    - man -a <topic>: Displays all pages matching a given name
    - man <section number> <topic>: Displays the specific section you want.

- GNU Info System
    - Run info without any arguments to open the top-level directory of all available topics
    - TYpe info followed by the command name to jump directly to a specific utility

- The --help Option
    - <command> --help
    - Unlike man and info, --help prints its output directly to the terminal and returns you straight to the prompt; there's no pager to scroll through or quit. That makes it the fastest way to jog your memory about a command's options.
    - help          # lists all the built-in commands
    - help cd        # shows usage for a specific built-in, e.g. cd

- Additional Documentation Sources
    - Just as in Windows and macOS, pressing F1 in many Linux desktop applications opens the app's help page directly. It is the fastest way to access an application's documentation, though support varies; so don't be surprised if F1 does nothing in certain programs.
    



## Questions to revisit

## Practical observations
