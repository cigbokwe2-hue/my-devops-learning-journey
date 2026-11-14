# Lab: Archiving (Backing Up) the Home Directory

## Goal
create a compressed backup of my home directory (~) into a single archive file, verifying its contents, and performing a test restoration.

## What I did
- I navigated to the /tmp directory to make the lab temporary
    ```Bash
    cd /tmp
    ```
- Created a gzip-compressed archive (backup.tar.gz) of my home directory.
    ```Bash
    tar zcvf backup.tar.gz ~
    ```
- Listed the contents of the archive I created, without extracting it, to confirm it worked.
    ```Bash
    tar ztvf backup.tar.gz
    ```
- Created a new empty directory under /tmp (/tmp/restore) and extracted the backup into it.
    ```Bash
    mkdir /tmp/restore
    ```
    ```Bash
    cd /tmp/restore
    ```
    ```Bash
    tar xzvf /tmp/backup.tar.gz
    ```
- Verified that my files are present in the restore directory.
    ```Bash
    ls -lha /tmp/restore
    ```


## What broke and how I fixed it
Nothing

## What I learned
- How compression works in linux
