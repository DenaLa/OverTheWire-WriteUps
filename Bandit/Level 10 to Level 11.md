# Level 9 → Level 10

## Description
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Things to Know
- **Base64** is a binary-to-text encoding scheme. It often has an equal sign at the end of the data, but that's not always the case
- We can use the `base64` command that comes with linux
	- `base64` encodes or decodes a file, or standard input, to standard output
	- For our purposes, we will use the `-d` flag, which decodes base64 files
		- Additionally., there is the `-i` flag, which tells the command line to ignore non-alphabet characters when decoding (the alternate command is called `--ignore-garbage`)
## Solution
1. `data.txt` will be in the home directory when you log in. if you use `cat`, you can see that it is in a state that is difficult for a human to parse
2. We want to use `base64 -d` in order to decode the data. Or command would be `base64 -d data.txt`
3. This should decode the data and give you the password.
