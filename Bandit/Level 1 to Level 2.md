# Level 1 → Level 2
_The password for the next level is stored in a file called - located in the home directory_
### Things to Know
`-` is a special character. It is used for other things, so attempting to use the command `cat -` will not work. In order to refer to files with special characters in their name, you need to append `./` to the beginning of them.
### Solution
1. The file is in the home directory. Thus, the command is as follows:
  `cat ./-`
