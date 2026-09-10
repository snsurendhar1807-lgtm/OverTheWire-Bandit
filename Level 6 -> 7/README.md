# OverTheWire Bandit — Level 6 → 7 
 
## Objective 
 
Retrieve the password for the next level from a file located somewhere on the server with specific ownership and size requirements. 
 
## Commands Used 
 
```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220

find -user bandit7 -group bandit6 -size 33c

find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null

cat /var/lib/dpkg/info/bandit7.password

Command Explanation

ssh bandit6@bandit.labs.overthewire.org -p 2220
---Connects to the Bandit server as bandit6 using SSH on port 2220.

find -user bandit7 -group bandit6 -size 33c
---Searches for a file owned by user bandit7, belonging to group bandit6, and having a size of exactly 33 bytes.
---This first search starts from the current directory, so it does not find the required file.

find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
---Searches the entire filesystem for a regular file matching the required conditions.

find / → Searches from the root directory.
-type f → Searches only for regular files.
-user bandit7 → File must be owned by bandit7.
-group bandit6 → File must belong to the bandit6 group.
-size 33c → File must be exactly 33 bytes.
2>/dev/null → Hides permission-denied error messages.

The command found:

/var/lib/dpkg/info/bandit7.password

cat /var/lib/dpkg/info/bandit7.password

Displays the contents of the identified file, which contains the password.

Result

Level 6 → 7 completed successfully.

Password: [REDACTED]
