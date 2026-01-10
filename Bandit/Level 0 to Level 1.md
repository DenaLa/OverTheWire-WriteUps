# Level 0 → Level 1
### Description
_The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game._
### Things to Know
When you log into bandit0, you will automatically be in its home directory. Since you are in its home directory, you can easily access the file for the password.

There are two commands that will come in handy here:
1. **ls**: This command lists the things in either the current directory or a specified directory (Typing `ls [DIRECTORY PATH]`). There are additional flags to modify its behavior, notable `-l` (use long listing format), `-a` (show all, including hidden files), and `-la` (use long listing format and show all, including hidden files).
2. **cat**: This command concatonates files and prints a standard output, but is mostly used for prinitng the contents of a file.

Another helpful thing to note is that you can use the TAB key to autocomplete file and directory names.

### Solution
1. (OPTIONAL) Use the `ls` command to view the file name.
2. The command to obtain the password is as follows:
  `cat readme`
