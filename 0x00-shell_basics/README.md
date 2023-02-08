# 0x00_Basic_Shell_Scripts


## Task_0

 Print the absolute path name of the current working directory.

```bash
pwd
```

## Task_1
Display the contents list of your current directory.

```bash
ls
```
## Task_2
Change the working directory to the user’s home directory.
```bash
cd ~
```
## Task_3
Display current directory contents in a long format.
```bash
ls -l 
```
## Task_4
Display current directory contents, including hidden files (starting with `.`). Use the long format.
```bash
ls -la 
```           
## Task_5
Display current directory contents.
* Long format
* With user and group IDs displayed numerically
* And hidden files (starting with `.`)
```bash
ls -lan
```
## Task_6
Create a script that creates a directory named `my_first_directory` in the `/tmp/` directory.
```bash
mkdir /tmp/my_first_directory/
```
## Task_7
Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`.
```bash
mv /tmp/betty /tmp/my_first_directory
```
## Task_8
Delete the file `betty`.
* The file `betty` is in `/tmp/my_first_directory`
```bash
rm /tmp/my_first_directory/betty
```
## Task_9
Delete the directory `my_first_directory` that is in the `/tmp` directory.
```bash
rm -r /tmp/my_first_directory
```
## Task_10
Change the working directory to the previous one.
```bash
cd -
```
## Task_11
List all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the `/boot` directory (in this order), in long format.
```bash
ls -al . .. /boot
```
## Task_12
Print the type of the file named `iamafile`. The file `iamafile` will be in the `/tmp`.
```bash
file /tmp/iamafile
```
## Task_13
Create a symbolic link to `/bin/ls`, named `__ls__`. The symbolic link should be created in the current working directory.
```bash
ln -s /bin/ls __ls__
```
## Task_14
Copy all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
You can consider that all HTML files have the extension `.html`
``` bash
cp -un *.html ../ 
```
## Task_15
Move all files beginning with an uppercase letter to the directory `/tmp/u`.
You can assume that the directory `/tmp/u` will exist when we will run your script.
``` bash
mv [[:upper:]]* /tmp/u
```

## Task_16
Delete all files in the current working directory that end with the character `~`.
```bash
rm *~
```
## Task_17
Creates the directories `welcome/`, `welcome/to/` and `welcome/to/school` in the current directory.
(Note : You are only allowed to use two spaces (and lines) in your script, not more.)
```bash 
mkdir -p welcome/to/school
```
## Task_18
Write a command that lists all the files and directories of the current directory, separated by commas (`,`).
* Directory names should end with a slash (`/`).
* Files and directories starting with a dot (`.`) should be listed.
* The listing should be alpha ordered, except for the directories `.` and `..` which should be listed at the very beginning.
* Only digits and letters are used to sort; Digits should come first.
* You can assume that all the files we will test with will have at least one letter or one digit.
* The listing should end with a new line.
```bash
ls -amvp
```

## Task_19
Create a magic file `school.mgc` that can be used with the command `file` to detect `School` data files. `School` data files always contain the string `SCHOOL` at offset 0.
```bash 
0 string SCHOOL School data
!:mime School
```


