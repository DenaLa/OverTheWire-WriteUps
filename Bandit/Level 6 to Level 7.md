# Level 6 → Level 7

### Description

*The password for the next level is stored **somewhere on the server** and has all of the following properties:
```
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size 
```

### Things to Know
- The file is somewhere on the server. This means it can be anywhere, not just in bandit6's home directory
- The file is owned by the **user** bandit7, and is owned by the **group** bandit6.
- The file is **33 bytes** in size.
- We can use the `find` command to help us with this problem.
	- The flag `type -f` will filter for files
	- The `-user` flag will specify user owners
	- The `-group` flag will specify group owners
	- The `-size` flag is still viable to use, and will specify the size.

### Solution
1. Since the file is **somewhere on the system**, we need to expand the range of our search. Navigate to the root of the system by using the `cd ..` command twice.
2. We want to use the `find` command to find the file we are looking for. In order to do so, we need to use the following flags:
	- `- type f` to specify files
	- `-user bandit7` to specify that it belongs to **bandit7**
	- `-group bandit6` to specify that it belongs to **bandit8**
	- `-size 33c` to specify that the file needs to be **33 bytes**.
	- The command that we want to type is `find -type f -user bandit7 -group bandit6 -size 33c`. 
3. You will notice that typing this command will give you many entries with the statement `Permission Denied`. This clogs our search, so we want to append `2>/dev/null` to the end of our command
	- `2` serves as our file descriptor. In linux, 2 defines a standard error.
	- `>` is a sign that sends output to a location. Conversely, `>>` appends output to a location
	- `/dev/null` is a location in the operating system that is ignored.
	- In total, we are appending a command that tells the operating system to send all Error outputs to the location that it will ignore
4. Our final command will be `find -type -f -user bandit7 -group bandit6 -size 33c 2>/dev/null`. The full path to the file with our password will be printed to the console. You can then `cat` that file path and receive the password to the next level.
