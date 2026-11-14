# Linux Foundations — Class Notes

Use this file for your own notes. Add to it as you learn.

## 

## Key ideas
- ssh - Secure SHell

- Absolute Pathname: An absolute pathname begins with the root directory (/) and follows the tree, branch by branch, until it reaches the desired directory or file. Absolute paths always start with /.

- Relative Pathname: A relative pathname starts from the present working directory. Relative paths never start with /.

- stdin, stdout, stderr 

- plocate

- find (find -name "*.mp4" -ok rm {} ';') (find -name "*.mp4" -exec rm {} ';')

- A low-level tool (such as dpkg or rpm) handles the details of unpacking individual packages, running their installation scripts, and getting the software installed correctly.

- A high-level tool (such as apt, dnf, or zypper) works with groups of packages, downloads them from the software repositories, and resolves dependencies.

- 

## Commands and examples
- cat: displays a file's contents (or combines/concatenates multiple files together)

- less: Used to view larger files

- head: displays the first few lines of a file

- tail: displays the last few lines of a file

- man: opens a command’s documentation page (man page)

- which shows the full path to a program

- whereis is a good alternative. It is a broader tool that locates the binary, its source code, and its manual pages.

- type is a shell built-in that tells you what a command actually is

- pushd: change directory and keep track of visited directory (popd to go back.dirs to show directory history)

- touch: edits existing files or creates new files

- mv: moves or renames files and directories

- rm: deletes files

- 


## Questions to revisit

## Practical observations
