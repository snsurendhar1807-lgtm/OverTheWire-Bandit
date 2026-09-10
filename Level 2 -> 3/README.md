# OverTheWire Bandit — Level 2 → 3 
 
## Objective 
 
Retrieve the password for the next level from a file whose name contains spaces and begins with `--`. 
 
## Commands Used 
 
```bash
ssh -p 2220 bandit.labs.overthewire.org -l bandit2

ls

cat "./--spaces in this filename--"

###Command Explanation

ssh -p 2220 bandit.labs.overthewire.org -l bandit2
---Connects to the Bandit server as bandit2 using SSH on port 2220.

ls
---Lists the files in the current directory.
   The file is named --spaces in this filename--.

cat "./--spaces in this filename--"
---Displays the contents of the file.

./ → Specifies that the file is in the current directory.
"..." → Keeps the spaces in the filename together as one argument.
--spaces in this filename-- → The actual filename.

The ./ is also important because the filename starts with --, which can be interpreted as a command-line option.

Result
Level 2 → 3 completed successfully.

Password: [REDACTED]


Level 2 → 3 completed successfully.

Password: [REDACTED]
