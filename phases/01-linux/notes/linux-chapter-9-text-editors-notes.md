# Linux — LFS101 Chapter 9: Text Editors

Use this file for your own notes. Add to it as you learn.

## Key ideas

- Text editors are essential tools for editing configuration files, scripts, and code from the shell.
- Terminal-based editors such as `vi`/`vim` and `nano` are common in Linux because they work in a command-line environment.
- A text editor may be modal or non-modal; understanding the editing model matters for efficient use.
- Editors differ in their learning curves, keyboard shortcuts, and suitability for quick fixes vs. larger file edits.
- Knowing how to save, quit, search, and navigate inside an editor is necessary for troubleshooting and system administration.

## Editors and commands

- `nano` — simple text editor with menu shortcuts for new users
- `vi` / `vim` — powerful standard editor commonly available on Linux systems
- `ed` — classic line-oriented editor; useful for understanding Linux history and editing fundamentals
- `cat > file` / here-docs — useful for quick file creation, though not a full editor
    - cat << EOF > myfile
    > line one
    > line two
    > line three
    > EOF
- Using echo with Redirection
    - echo line one > myfile

    - echo line two >> myfile

    - echo line three >> myfile
- nano 
    - To open an existing file or create a new one, pass a filename to nano:
        - nano notes.txt : If notes.txt exists, nano opens it for editing; if it doesn't, nano starts a new empty file with that name, ready for you to type.

