# OverTheWire Bandit — Level 14 → 15

## Objective

Send the current level's password to a service running on localhost port `30000` to retrieve the password for Level 15.

## Commands Used

```bash
ssh bandit14@bandit.labs.overthewire.org -p 2220

echo "aaWecNkG4FhxJQxz07uiwzVP6bJiYS65" | nc localhost 30000

Command Explanation

ssh bandit14@bandit.labs.overthewire.org -p 2220
---Connects to Bandit Level 14 using SSH on port 2220.

echo "..."
---Prints the current level's password.

|
---Pipes the password as input to the next command.

nc localhost 30000
---Connects to the service running on port 30000 on the local machine.

localhost
---Refers to the current Bandit server.

30000
---The port where the password-checking service is running.

Result
The service responded with:

Correct!
[REDACTED]
