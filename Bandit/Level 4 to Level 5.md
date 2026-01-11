# Level 4 → Level 5
### Description
_The password for the next level is stored in the only human-readable file in the inhere directory. 
Tip: if your terminal is messed up, try the “reset” command._
### Things to Know
1. **file**: The file command tells you the file type of what you ask of it. It can also be used to identify directories if you use a wildcard with it (`file *`)
2. **\***: The wildcard symbol (\*) is used to denote "everything". It will give you every single result of what you are asking for. It is not a command, so you cannot use it by itself. You can use it with other commands. It is a special character.

With a problem like this, we do not want to try and brute force it. While it can be manageable with a few files, it quickly becomes unmanageable once the amount of files grows.
### Solution
_NOTE: This solution will be written in a bit more detail in order to illustrate a point_
1. Navigate into the **inhere** directory with the command `cd inhere`.
2. (OPTONAL) use the `ls` command to view the files in the directory
3. Use the `file ./*` command to view the types of every file in the directory.
4. There will be two file types listed when you use this command, **data** and **ASCII text**. **ASCII text** is human readable text. Read the contents of that file with the `cat` command.
