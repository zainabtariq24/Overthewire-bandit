# Bandit Level 0 → 1 (Easy)
## What was the goal?
Log into the game using the username,hostname and password given and find the password stored in a file called `readme`.

## Protocol i used
SSH

## Commands I used
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls -alph
cat readme
```

## What each command did
- `ssh` -> connected me to the remote server
- `cat` -> read and printed the file contents
- `la-alph`-> shows every single file in detail ,including the hidden files as well, in a readable way.

## What I learned
- How to connect to a server using SSH
- How to read a file using cat