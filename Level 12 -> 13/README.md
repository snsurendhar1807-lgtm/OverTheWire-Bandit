# OverTheWire Bandit — Level 12 → 13

## Objective

Recover the password from a file containing multiple layers of compression and archiving.

## Commands Used

```bash
ssh bandit12@bandit.labs.overthewire.org -p 2220

mkdir /tmp/bandit12
cp data.txt /tmp/bandit12/
cd /tmp/bandit12

file data.txt
xxd -r data.txt data.bin

file data.bin
mv data.bin data.gz
gunzip data.gz

file data
mv data data.bz2
bunzip2 data.bz2

file data
mv data data.gz
gunzip data.gz

file data
tar -xf data

file data5.bin
tar -xf data5.bin

file data6.bin
mv data6.bin data6.bz2
bunzip2 data6.bz2

file data6
tar -xf data6

file data8.bin
mv data8.bin data8.gz
gunzip data8.gz

file data8
cat data8

Command Explanation

mkdir /tmp/bandit12
---Creates a temporary working directory.

cp data.txt /tmp/bandit12/
---Copies data.txt to the working directory.

cd /tmp/bandit12
---Enters the working directory.

file data.txt
---Identifies the type of the file.

xxd -r data.txt data.bin
---Converts the hexadecimal dump back into binary data.

mv data.bin data.gz
---Renames the file with the .gz extension.

gunzip data.gz
---Decompresses the gzip file.

mv data data.bz2
---Renames the file with the .bz2 extension.

bunzip2 data.bz2
---Decompresses the bzip2 file.

tar -xf data
---Extracts the tar archive.

file data5.bin / file data6.bin / file data8.bin
---Identifies the compression or archive format of each file.

tar -xf data5.bin and tar -xf data6
---Extract the tar archives.

cat data8
---Displays the final text containing the password.
Result

The final password for Level 13 was successfully recovered.

Password: [REDACTED]
