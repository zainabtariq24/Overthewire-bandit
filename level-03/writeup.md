# Bandit Level 3 → 4

## What was the goal?
Find the password stored in a hidden file inside the `inhere` directory.

## Commands I used
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
ls -alph
cd inhere
ls -alph
cat .hidden
```

## What each command did
- `ssh` → connected to the server as bandit3
- `ls -alph` → listed files in home directory, found `inhere` folder
- `cd inhere` → moved into the inhere directory
- `ls -alph` → revealed the hidden file (hidden files start with `.`)
- `cat .hidden` → read the hidden file to get the password

## What I learned
- Hidden files in Linux start with a `.` (dot)
- `ls` alone won't show them — you need the `-a` flag to reveal them
- You have to `cd` into a directory before you can see what's inside it