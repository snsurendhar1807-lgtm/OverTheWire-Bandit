# OverTheWire Bandit — My Linux & Cybersecurity Learning Journey

## About This Repository

This repository contains my solutions, commands, explanations, and key learnings from the **OverTheWire Bandit** wargame.

The goal is to build practical Linux and cybersecurity skills by solving challenges step by step.

> **Note:** Passwords, private keys, and other sensitive challenge information are intentionally redacted.

## What I Am Learning

- Linux command line
- SSH
- File and directory navigation
- Linux file permissions
- Hidden files
- Searching files with `find`
- Text processing with `grep`, `sort`, `uniq`, and `tr`
- File encoding and decoding
- Compression and archiving
- Netcat (`nc`)
- SSL/TLS with OpenSSL
- SSH keys and authentication
- Basic cybersecurity concepts

## Levels Completed

| Level | Main Concept |
|---|---|
| 0 → 1 | SSH and reading files |
| 1 → 2 | Filenames beginning with `-` |
| 2 → 3 | Filenames containing spaces |
| 3 → 4 | Hidden files |
| 4 → 5 | Identifying file types |
| 5 → 6 | Finding files by size |
| 6 → 7 | Finding files by owner, group and size |
| 7 → 8 | Searching text with `grep` |
| 8 → 9 | `sort` and `uniq` |
| 9 → 10 | Extracting readable strings |
| 10 → 11 | Base64 decoding |
| 11 → 12 | ROT13 decoding |
| 12 → 13 | Multiple compression and archive layers |
| 13 → 14 | SSH private key authentication |
| 14 → 15 | Netcat and network services |
| 15 → 16 | SSL/TLS with OpenSSL |

## Repository Structure

```text
OverTheWire/
│
├── README.md
│
├── LEVEL 0-LEVEL 1.md
├── LEVEL 1-LEVEL 2.md
├── LEVEL 2-LEVEL 3.md
├── LEVEL 3-LEVEL 4.md
├── LEVEL 4-LEVEL 5.md
├── LEVEL 5-LEVEL 6.md
├── LEVEL 6-LEVEL 7.md
├── LEVEL 7-LEVEL 8.md
├── LEVEL 8-LEVEL 9.md
├── LEVEL 9-LEVEL 10.md
├── LEVEL 10-LEVEL 11.md
├── LEVEL 11-LEVEL 12.md
├── LEVEL 12-LEVEL 13.md
├── LEVEL 13-LEVEL 14.md
├── LEVEL 14-LEVEL 15.md
└── LEVEL 15-LEVEL 16.md

'''bash
Quick Command Reference
SSH
ssh bandit0@bandit.labs.overthewire.org -p 2220
List Files
ls
ls -la
Read a File
cat filename
Search for Text
grep "keyword" filename
Find Files
find . -type f
Check File Type
file filename
Extract Readable Strings
strings filename
Sort and Find Unique Lines
sort filename | uniq -u
Base64 Decode
base64 -d filename
ROT13 Decode
tr 'A-Za-z' 'N-ZA-Mn-za-m' < filename
Netcat
echo "password" | nc localhost 30000
SSL/TLS Connection
openssl s_client -connect localhost:30001 -quiet
Secure Copy
scp -P 2220 user@host:file destination
SSH Using a Private Key
ssh -i private_key user@host -p 2220
Important Security Practice

Passwords and private keys used during the challenges are not stored in this repository.

Sensitive information is represented as:

[REDACTED]

Private SSH keys such as sshkey.private or bandit14.private should never be committed to GitHub.

Key Takeaways

Through these challenges, I am learning how to:

Work confidently in a Linux terminal.
Navigate files and directories.
Search for specific files and information.
Understand different file formats and compression methods.
Decode encoded data.
Work with network services.
Use SSH and SSH keys.
Understand basic secure communication using SSL/TLS.
Solve cybersecurity problems using command-line tools.
