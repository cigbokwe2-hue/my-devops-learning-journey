# Lab: First Push

## Goal
Push my repo to github using ssh instead of https to learn the basics of ssh

## What I did
- I searches for existing keys and decided to create a new key for github so as to not link the existing keys with that of github.
- I created an ssh key using a new file name so as not to conflict it with my existing keys
```bash
ssh-keygen -t ed25519 -C "label" -f "key path"
```
- I created a config file in .ssh to point github's ssh to that key with;
```bash
Host github.com
#sets the host as github.com
    IdentityFile "file path"
    #points to my private key's path
    IdentitiesOnly yes
    #Let's it use only this key, and not to offer GitHub my other keys
```
- I made the config file private with;
```bash
    chmod 600 "file path"
    # 6 means to read and write for me
    # the two 0s removes the permissions for groups and others
```
- I added the public key to github not the secret private key
- I created the empty repo
- I added the repo as remote with:
```bash
    git remote add origin "ssh address"
```
- I pushed with;
```bash
    git push -u origin main
    # -u means it remembers the link for following pushes
```




## What broke and how I fixed it
- I tried to cp into a folder that doesn't exist and got an error, then I tried mkdir with the same non-existent directory and got the same error. I fixed it by adding the -p option to create parent directory where the don't exist.

## What I learned
- Difference between public and private keys
- How to use the man command to view documentations
