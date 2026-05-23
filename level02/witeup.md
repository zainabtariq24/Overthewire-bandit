# Bandit Level 2 → 3
## What was the goal?
Find the password stored in a file called `--spaces in this filename--` 
located in the home directory.

## Commands I used
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
ls -alph
cat "--spaces in this filename--"
cat --\ spaces\ in\ this\ filename--
```

## What each command did
- `ssh` → connected to the server as bandit2
- `ls -alph` → listed all files to confirm the filename
- `cat "filename"` → wrapping the filename in quotes tells the terminal 
to treat everything inside as one single filename, including spaces
- `cat --\ spaces...` → backslash before each space does the same thing, 
it "escapes" the space so the terminal doesn't treat it as a separator

## What I learned
- Filenames can contain spaces which confuse the terminal
- Two ways to handle spaces in filenames: quotes or backslash escaping
- `\` before a character is called escaping — it removes the special 
meaning of that character