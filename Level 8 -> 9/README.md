# OverTheWire Bandit — Level 8 → 9 
 
## Objective 
 
Retrieve the password for the next level from `data.txt`. The password is the only line that appears exactly once in the file. 
 
## Commands Used 
 
```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220

sort data.txt | uniq -u

Command Explanation

ssh bandit8@bandit.labs.overthewire.org -p 2220
---Connects to the Bandit server as bandit8 using SSH on port 2220.

sort data.txt
---Sorts all the lines in data.txt alphabetically.

Sorting is required because uniq only detects duplicate lines when they are next to each other.

uniq -u
Displays only the lines that appear exactly once.

sort data.txt | uniq -u
The | (pipe) sends the output of sort directly to uniq.

The command identifies the unique line, which contains the password for the next level.

Result

Level 8 → 9 completed successfully.

Password: [REDACTED]
