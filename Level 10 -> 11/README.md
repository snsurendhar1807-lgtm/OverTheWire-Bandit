# OverTheWire Bandit — Level 10 → 11

## Objective

Decode the Base64-encoded contents of `data.txt` to retrieve the password for the next level.

## Commands Used

```bash
ssh bandit10@bandit.labs.overthewire.org -p 2220

ls

cat data.txt

base64 -d data.txt

#Command Explanation
ssh bandit10@bandit.labs.overthewire.org -p 2220
---Connects to Bandit Level 10 using SSH on port 2220.

ls
---Lists the files in the current directory.

cat data.txt
---Displays the contents of data.txt.

base64 -d data.txt
---Decodes the Base64-encoded content of data.txt.

Result

The decoded output contains the password for Level 11.

Password: [REDACTED]
