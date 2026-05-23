# Bandit Level 4 → 5 (Easy)

## What was the goal?
Find the password in the only human-readable file inside the `inhere` 
directory.

## Commands I used
```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
cd inhere
ls -alph
file ./-file00
cat ./-file07
file ./*
```

## What each command did
- `ssh` → connected to the server as bandit4
- `cd inhere` → moved into the inhere directory
- `ls -alph` → listed all the files
- `file ./-file00` → checks what type of data is in a file. I used this 
on each file until I found the one that said "ASCII text" meaning human readable
- `cat ./-file07` → read the human readable file to get the password

## What I learned
- `file` command tells you what type of data a file contains
- Human readable files show as "ASCII text"
- Binary/data files show as "data" and print garbage to the terminal
- `./` before a filename starting with `-` prevents the terminal 
from thinking it's a flag
- After finding the password by opening files one by one, I learned 
a smarter way: `file inhere/*` checks all files at once and shows 
their type, so you can spot the human-readable one instantly without 
opening each file manually