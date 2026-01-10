# Level 2 → Level 3
### Description
_The password for the next level is stored in a file called --spaces in this filename-- located in the home directory._
### Things to Know
File names with spaces in them need to be surrounded with either single quotes or double quotes ('' or ""), or else the spaces will be read as delineations.
### Solution
1. The command is as follows:
    `cat ./"--spaces in this filename--"`
### Trivia
_This problem was changed from its initial version, which asked you to read from a file named "spaces in this filename". It was given special characters to deter individuals from following a guide. I remember solving the initial problem, and having a good chuckle seeing it's revised form._
