# OverTheWire Bandit — Level 1 → 2 
 
## Objective 
 
Retrieve the password for the next level from a file named `-`. 
 
## Commands Used 
 
```bash
ssh -p 2220 bandit.labs.overthewire.org -l bandit1

ls

cat ./-


###Command Explanation
ssh -p 2220 bandit.labs.overthewire.org -l bandit1
Connects to the Bandit server as bandit1 using SSH on port 2220.

ls-Lists the files in the current directory.
The output shows a file named -.

cat ./-
Displays the contents of the file named -.

Here, ./ means the current directory.
So ./- tells Linux that - is the filename, not a command option.

Normally, cat - has a special meaning because - can be interpreted as an option or standard input.
Using ./- clearly specifies that we want to read the file named -.

Result

Level 1 → 2 completed successfully.

Password: [REDACTED]
