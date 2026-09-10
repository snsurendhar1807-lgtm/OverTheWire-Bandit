# OverTheWire Bandit — Level 9 → 10 
 
## Objective 
 
Retrieve the password for the next level from `data.txt`. The password is stored in a human-readable string preceded by several `=` characters. 
 
## Commands Used 
 
```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220

ls

strings data.txt

strings data.txt | grep "="

###Command Explanation

ssh bandit9@bandit.labs.overthewire.org -p 2220
---Connects to the Bandit server as bandit9 using SSH on port 2220.

ls
---Lists the files in the current directory.
---The file data.txt is present.

strings data.txt
---Extracts and displays readable text from the binary file.

Since data.txt contains mostly binary data, strings helps identify human-readable text inside it.

strings data.txt | grep "="
---Filters the readable strings and displays only the lines containing =.

| → Sends the output of strings to grep.
grep "=" → Searches for lines containing the = character.

The output reveals the line containing the password.

Result

Level 9 → 10 completed successfully.

Password: [REDACTED]
