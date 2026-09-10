# OverTheWire Bandit — Level 5 → 6 
 
## Objective 
 
Retrieve the password for the next level from a file with a specific size of 1033 bytes. 
 
## Commands Used 
 
```bash
ssh -p 2220 bandit.labs.overthewire.org -l bandit5

ls

cd inhere

ls

ls -la

find . -type f -size 1033c

cat ./maybehere07/.file2

Command Explanation

ssh -p 2220 bandit.labs.overthewire.org -l bandit5
---Connects to the Bandit server as bandit5 using SSH on port 2220.

ls
---Lists the files and directories in the current directory.
---The inhere directory contains the files we need to search.

cd inhere
---Moves into the inhere directory.

ls
---Lists the directories inside inhere.

ls -la
---Displays all directories and files, including hidden files, with detailed information.

find . -type f -size 1033c
---Searches for a regular file with exactly 1033 bytes.

find . → Searches from the current directory.
-type f → Searches only for regular files.
-size 1033c → Finds files exactly 1033 bytes in size.
c → Means bytes.

The command found:
./maybehere07/.file2

cat ./maybehere07/.file2
Displays the contents of the identified file, which contains the password.
Result

Level 5 → 6 completed successfully.

Password: [REDACTED]
