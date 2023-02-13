# 0x02 Shell, I/O Redirections and filters

## Task 0
Print "Hello, World", followed by a new line to the standard output
```bash
echo Hello, World
```
## Task 1 
Display a confused smiley `"(Ôo)'`
```bash
echo "\"(Ôo)'"
```
## Task 2
Display the content of the `/etc/passwd` file
```bash
cat /etc/passwd
```
## Task 3
Display the content of `/etc/passwd` and `/etc/hosts`
```bash
cat /etc/passwd /etc/hosts
```
## Task 4
Display the last 10 lines of `/etc/passwd`
```bash
tail -n 10 /etc/passwd 
```

## Task 5
Display the first 10 lines of `/etc/passwd`
```bash
head -n 10 /etc/passwd
```
## Task 6	
Display the third line of the file `iacta`
```bash
head -n 3 iacta | tail -n 1
```
## Task 7
Create a file named exactly `\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)` containing the test `Best School` ending by a new line
```bash
echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)
```
## Task 8
Write into the file `ls_cwd_content` the result of the command `ls -la`
```bash
ls -la > ls_cwd_content
```
## Task 9
Duplicate the last line of the file `iacta`
```bash
tail -n 1 iacta >> iacta
```
## Task 10
Delete all the regular files with a `.js` extension that are present in the current directory and all its subfolders
```bash
find . -type f -name "*.js" -delete
```
## Task 11
Count the number of directories and sub-directories in the current directory
```bash
find . -type d -not -name '.' | wc -l
```
## Task 12
Display the 10 newest files in the current directory
```bash
ls -t1 | head -n 10
```
## Task 13
Takes a list of words as input and prints only words that appear exactly once
```bash
sort | uniq -u
```
## Task 14
Displayes lines containing the pattern "root" from the file `/etc/passwd`
```bash
grep -i "root" /etc/passwd
```
## Task 15
Displays the number of lines that contain the pattern "bin" in the file `/etc/passwd`
```bash
grep -c -i "bin" /etc/passwd
```
## Task 16
Display lines containing the pattern "root" and 3 lines after them in the file `/etc/passwd`
```bash
grep -i "root" -A 3 /etc/passwd
```
## Task 17
Displays all the lines in the file `/etc/passwd` that do not contain the pattern "bin"
```bash
grep -i -v "bin" /etc/passwd
```
## Task 18
Display all lines of the file `/etc/ssh/sshd_config` starting with a letter
```bash
grep -i "^[a-z]" /etc/ssh/sshd_config
```
## Task 19
Replace all characters `A` and `c` from input to `Z` and `e` respectively
```bash
tr "A" "Z" | tr "c" "e"
```
## Task 20
Remove all letters `c` and `C` from input
```bash
tr -d "cC"
```
## Task 21
Reverse input
```bash
rev
```
## Task 22
Display all users and their home directories, sorted by users
```bash
cut -d ':' -f 1,6 /etc/passwd | sort
```
## Task 100
Find all empty files and directories in the current directory and all sub-directories
```bash
find . -empty | rev | cut -d '/' -f 1 | rev
```
## Task 101
List all the files with a `.gif` extension in the current directory and all its sub-directories
```bash
find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f
```
## Task 102
Decode acrostics that use the first letter of each line
```bash
cut -c 1 | paste -s -d ''
```
## Task 103
Parse web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests
```bash
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev
```
