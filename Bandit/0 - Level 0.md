# Level 0
### Description
_The goal of this level is for you to log into the game using SSH. The host to which you need to connect is bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in, go to the Level 1 page to find out how to beat Level 1._
### Things to Know
_**NOTE**: If you are on a windows machine, I reccomend using a virtual machine to virtualize a linux distribution. This is more consistent than using a terminal like cygwin, which was servicable up until file creation and using git was needed._

This level is just to let you log in. The command to log into a given ssh server is `ssh [USERNAME]@[IP ADDRESS/SERVER ADDRESS]`. if you need a specific port, you use the `-p` flag, and give the port number in the format `-p [PORT NUMBER]`.
### Solution
1. Command is as follows:
  `ssh bandit0@bandit.labs.overthewire.org -p 2220`.
