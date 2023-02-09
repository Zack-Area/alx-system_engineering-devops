# 0x01 Shell_permissions

## Task 0
Switch the current user to the user `betty`.
```bash
su betty
```
## Task 1 
Print the effective username of the current user.
```bash
whoami
```
## Task 2
Print all the groups the current user is part of.
```bash
groups
```
## Task 3
Change the owner of the file hello to the user `betty`.
```bash
sudo chown betty hello
```
## Task 4
Create an empty file called `hello`.
```bash
touch hello
```

## Task 5
Add execute permission to the owner of the file `hello`.

(Note: The file `hello` will be in the working directory)
```bash
chmod u+x hello
```
## Task 6
Add execute permission to the owner and the group owner, and read permission to other users, to the file `hello`.

The file `hello will be in the working directory
```bash
chmod +114 hello
```
## Task 7
Add execution permission to the owner, the group owner and the other users, to the file `hello`.

The file `hello` will be in the working directory.

(Note: You are not allowed to use commas for this script)
```bash
chmod ugo+x hello
```
## Task 8
Set the permission to the file `hello`.

* Owner: no permission at all
* Group: no permission at all
* Other users: all the permissions
The file `hello` will be in the working directory

(Note: You are not allowed to use commas for this script)
```bash
chmod 007 hello
```
## Task 9
Set the mode of the file `hello` to this :
```bash
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
```
* The file hello will be in the working directory

(Note: You are not allowed to use commas for this script)
```bash
chmod 753 hello
```
## Task 10
Set the mode of the file `hello` the same as `olleh`'s mode :
```bash
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
```
* The file `hello` will be in the working directory
* The file `olleh` will be in the working directory
```bash
chmod --reference=olleh hello
```
## Task 11
Add execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.
```bash
chmod  a+x */
```
## Task 12irectories
Create a directory called `my_dir` with permissions `751` in the working directory.
```bash
mkdir -m 751 my_dir
```
## Task 13
Changes the group owner to `school` for the file `hello`

The file `hello` will be in the working directory.
```bash
chgrp school hello
```
## Task 100
Change the owner to `vincent` and the group owner to `staff` for all the files and directories in the working directory.
```bash
chown vincent:staff *
```
## Task 101
Changes the owner and the group owner of `_hello` to `vincent` and `staff` respectively.

* The file `_hello` is in the working directory
* The file `_hello` is a symbolic link
```bash
chown -h vincent:staff _hello
```
## Task 102
Change the owner of the file `hello` to `betty` only if it is owned by the user `guillaume`.

The file `hello` will be in the working directory.
```bash
chown --from=guillaume betty hello
```
## Task 17
Play the StarWars IV episode in the terminal.
```bash
telnet towel.blinkenlights.nl
```
