# Level 8 → Level 9

## Description

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Things to Know
- There are two commands we can use here, `sort`, `uniq`
	- `sort` will sort the contents of a file in alphabetical and numerical order
	- `uniq` stands for "unique", will print or omit repeated lines. Using `uniq` by itself will print lines that have been repeated. If you add the `-u` flag, it will print the lines that only occur once.
## Solution
1. Once again, `data.txt` is right in the directory when you log in
	 - If you `cat` the data, you'll see how it is a bunch of lines of different characters put together
2. If you use `sort` on `data.txt`, it will arrange all of the lines in alphabetical order. We want to pipe `uniq -u` onto that output.
3. Our command will then be `sort data.txt | uniq -u`
4. This will give you the password for the next level
