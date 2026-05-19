# Level 7 → Level 8
## Description

The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Things to Know
- This level is very easily be solved using `grep`
- in order to use `grep`, first you need to pipe it with `|`
## Solution
1. Once you log in, `data.txt` will be right in the home directory
2. Our command is `cat data.txt | grep millionth`
	- You can chose to type `millionth` or `"millionth"`
3. This will give you the password for the next level
