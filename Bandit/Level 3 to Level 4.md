# Level 3 → Level 4
### Description
_The password for the next level is stored in a hidden file in the inhere directory._
### Things to Know
In order to complete this level, you need two commands:
1. **cd**: This allows you to change directories by using the command name, followed by the directory name or path.
      1. If you are in the same directory as your chosen directory, you can simply write the directory name. (`cd [DIRECTORY NAME]`)
      2. If you know the full directory path, you can write the full path name. (`cd [DIRECTORY PATH]`)
2. **ls -a/ls -la**: These commands will list all files and directories in a given directory, including hidden ones. They list them in standard and long format respectively.
### Solution
1. (OPTIONAL) use `ls` to view the **inhere** directory
2. Navigate inside the **inhere** directory is the `cd inhere` command
3. Use the `ls -la` or `ls -a` command to view all files, including hidden ones. You should be able to see the hidden file in the folder.
4. Use the `cat` command to read the file. 
