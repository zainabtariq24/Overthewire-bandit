# Bandit Level 1 → 2
## What was the goal?
Find the password stored in a file called `-` located in the home directory.

## Commands I used
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
ls -alph
cat -- "-"
```

## What each command did
- `ssh` → connected to the server as bandit1
- `ls -alph` → listed all files to confirm the `-` file existed
- `cat -- "-"` → read the file called `-`. Using just `cat -` didn't work because the terminal thought `-` was a flag/option for the command, not a filename. `--` tells the command "everything after this is a filename, not a flag"

## What I learned
- Files can be named special characters like `-`
- `--` is used to separate command flags from filenames
- You can't always access files the straightforward way