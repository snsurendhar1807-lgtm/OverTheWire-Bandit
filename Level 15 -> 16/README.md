# OverTheWire Bandit — Level 15 → 16

## Objective

Send the Level 15 password through an SSL/TLS connection on port `30001` to retrieve the password for Level 16.

## Commands Used

```bash
ssh bandit15@bandit.labs.overthewire.org -p 2220

cat /etc/bandit_pass/bandit15

openssl s_client -connect localhost:30001 -quiet

After the secure connection is established, paste the Level 15 password and press Enter.

Correct!
[REDACTED]

Then close the connection:

Ctrl + C
---Exit the SSH session:

exit
---Log in to Level 16:

ssh bandit16@bandit.labs.overthewire.org -p 2220

Command Explanation
cat /etc/bandit_pass/bandit15
---Reads the password for Level 15.

openssl s_client -connect localhost:30001 -quiet
---Creates an SSL/TLS connection to the service running on port 30001.

localhost
---Refers to the current Bandit server.

30001
---The port running the SSL/TLS service.
---Ctrl + C

Closes the OpenSSL connection.
exit
---Closes the current SSH session.
ssh bandit16@bandit.labs.overthewire.org -p 2220

Connects to Level 16 using the password obtained from the SSL/TLS service.

Result

Successfully retrieved the password for Level 16 using an SSL/TLS connection.

Password: [REDACTED]
