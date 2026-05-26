# Level 9 → Level 10

## Description
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Things to Know
- The `strings` command finds human readable text in files. It's used to find printable strings in a file. It's useful for identifying useful objects in a file
- `grep` can be used to filter results by looking for certain words, phrases, characters, otherwise known as **regular expressions** (regex)

## Solution
1. Data will be right in the home directory when you log in.
2. Using `strings data.txt` you will print out the human readable text in the file
3. Next, pipe a grep onto the `strings data.txt` command that looks for several '=' characters
4. Your final command should resemble `strings data.txt | grep "====" `
5. This will give you the password needed for the next level.
