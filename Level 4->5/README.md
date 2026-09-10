# OverTheWire Bandit — Level 4 → 5 
 
## Objective 
 
Retrieve the password for the next level from the only human-readable file inside the `inhere` directory. 
 
## Commands Used 
 
```bash
ssh -p 2220 bandit.labs.overthewire.org -l bandit4

ls

cd inhere

ls

file ./*

cat ./-file02

Command Explanation
ssh -p 2220 bandit.labs.overthewire.org -l bandit4
---Connects to the Bandit server as bandit4 using SSH on port 2220.

ls
---Lists the files and directories in the current directory.
cd inhere
---Moves into the inhere directory.

ls
---Lists the files inside the inhere directory.
---Several files are present, but we need to find the human-readable one.

file ./*
---Checks the type of every file in the directory.
   The ./* means all files in the current directory.
   The file command identifies which file contains human-readable ASCII text.

cat ./-fileXX
---Displays the contents of the identified human-readable file.

./ is used because the filename starts with -, preventing it from being interpreted as a command option.

Result

Level 4 → 5 completed successfully.

Password: [REDACTED]
