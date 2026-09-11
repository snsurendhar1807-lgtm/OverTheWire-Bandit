# OverTheWire Bandit — Level 13 → 14

## Objective

Use the SSH private key provided in Level 13 to log in to Level 14 and retrieve its password.

## Commands Used

```powershell

scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private bandit14.private

ssh -i bandit14.private bandit14@bandit.labs.overthewire.org -p 2220

cat /etc/bandit_pass/bandit14

Command Explanation

scp -P 2220 ...
---Copies sshkey.private from the Bandit server to the local Windows computer.

bandit14.private
---Saves the downloaded private key with a new local filename.

ssh -i bandit14.private ...
---Uses the private key to authenticate as bandit14.

-i bandit14.private
---Specifies the SSH private key to use.

cat /etc/bandit_pass/bandit14
---Displays the password for Level 14.

Result
Successfully logged in to bandit14 using the SSH private key.

Password: [REDACTED]
