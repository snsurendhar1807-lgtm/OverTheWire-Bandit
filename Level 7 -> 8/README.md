# OverTheWire Bandit — Level 7 → 8 
 
## Objective 
 
Retrieve the password for the next level from `data.txt`. The password is located on the same line as the word `millionth`. 
 
## Commands Used 
 
```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220

ls

grep "millionth" data.txt

Command Explanation
ssh bandit7@bandit.labs.overthewire.org -p 2220
---Connects to the Bandit server as bandit7 using SSH on port 2220.

ls
---Lists the files in the current directory.
---The file data.txt is present.

grep "millionth" data.txt
---Searches for the word millionth inside data.txt and displays the matching line.

grep → Searches for specific text inside files.
"millionth" → The text we want to find.
data.txt → The file being searched.

The matching line contains the password for the next level.

Result

Level 7 → 8 completed successfully.

Password: [REDACTED]
