# OverTheWire Bandit — Level 3 → 4 
 
## Objective 
 
Retrieve the password for the next level from a hidden file inside the `inhere` directory. 
 
## Commands Used 
 
```bash
ssh -p 2220 bandit.labs.overthewire.org -l bandit3

ls

cd inhere

ls -la

cat ...Hiding-From-You

###Command Explanation

ssh -p 2220 bandit.labs.overthewire.org -l bandit3

Connects to the Bandit server as bandit3 using SSH on port 2220.

ls
Lists the files and directories in the current directory.

The inhere directory contains the required file.

cd inhere
Moves into the inhere directory.

ls -la
Lists all files, including hidden files.
The -a option shows hidden files, while -l displays detailed information.

cat ...Hiding-From-You
Displays the contents of the hidden file, which contains the password.

./ specifies that the file is located in the current directory.

Result

Level 3 → 4 completed successfully.

Password: [REDACTED]
