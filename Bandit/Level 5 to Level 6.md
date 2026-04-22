# Level 5 → Level 6

### Description

_The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:_

```
human-readable
1033 bytes in size
not executable
```

### Things to Know

We are looking for three things:

- **The file has to be human readable**. Meaning, there is a good chance the file we are looking for is ASCII text.
- **The file needs to be 1033 bytes in size**. We will need to use a command that can tell us the size of a file in bytes
- **The file needs to be a non-executable**. This means the file needs to be unable to execute, with no execute permissions for the owner, the group, or everyone.
- The `find` command can be used for finding non-executable files with the `-executable` flag by placing a `!` before it. Other flags include:
	- `size <BYTES>` finds the size in bytes. You must put a `c` at the end of the number. (For example, 1033c for 1033 bytes)
	- `type f` gives you only files, meaning there will be no directories or executables
	- `readable` finds files you have permission to read
	- `exec <COMMAND>` makes a command that will be executed on a file. If we combine this with `{}` (With `{}` meaning all files), it will be executed on all files. `-exec` can be used to execute another command, like file. (ex. `-exec file`)

It is again, possible to brute force the solution, but given how wide our range of search is, it is better to narrow things down.

### Solution
1. We can use the `find` command with `-exec` in order to find what we need with one command.
	* `! -executable` tells `find` to exclude executables
	* `-size 1033c` will denote to look for files that are 1033 bytes
	* `-type f` will produce only files
	* `-exec file '{}' \;` will execute the file command and get the file's data type
		* Use `|` to pipe `grep ASCII` in order to filter it further to only return files that are ASCII files
2. The command is then: `find . -type f -size 1033c ! -executable -exec file '{}' \; | grep ASCII`
3. Once the file name is given, you can `cat` and get your password.
