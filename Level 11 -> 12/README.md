# OverTheWire Bandit — Level 11 → 12

## Objective

Decode the contents of `data.txt`, which has been encrypted using ROT13, to retrieve the password for the next level.

## Commands Used

```bash

ssh bandit11@bandit.labs.overthewire.org -p 2220

ls

cat data.txt

tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt

Command Explanation

ssh bandit11@bandit.labs.overthewire.org -p 2220
---Connects to Bandit Level 11 using SSH on port 2220.

ls
---Lists the files in the current directory.

cat data.txt
---Displays the encrypted contents of data.txt.

tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
---Converts each letter using ROT13 and displays the decoded text.

< data.txt
---Takes the contents of data.txt as input for the tr command.

Result

The decoded output contains the password for Level 12.

Password: [REDACTED]
