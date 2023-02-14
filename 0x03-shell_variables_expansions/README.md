# 0x03. Shell, init files, variables and expansions

## Task 0
Create a script that creates an alias.
* Name: `ls`
* Value: `rm *`
```bash
alias ls="rm *"
```
## Task 1 
 Prints `hello user`, where user is the current Linux user.
```bash
echo "hello "$USER
```
## Task 2
Add `/action` to the `PATH`. `/action` should be the last directory the shell looks into when looking for a program.
```bash
PATH=$PATH:/action
```
## Task 3
Count the number of directories in the `PATH`.
```bash
echo $PATH | tr ':' '\n' | wc -l
```
## Task 4
Lists environment variables.
```bash
printenv
```

## Task 5
 List all local variables and environment variables, and functions.
```bash
set
```
## Task 6	
Create a new local variable.
* Name: `BEST`
* Value: `School`
```bash
BEST="School"
```
## Task 7
Create a new global variable.
* Name: `BEST`
* Value: `School`
```bash
export BEST="School"
```
## Task 8
Print the result of the addition of 128 with the value stored in the environment variable `TRUEKNOWLEDGE`, followed by a new line.
```bash
echo $((TRUEKNOWLEDGE + 128))
```
## Task 9
Print the result of `POWER` divided by `DIVIDE`, followed by a new line.
* `POWER` and `DIVIDE` are environment variables
```bash
echo $((POWER / DIVIDE)
```
## Task 10
Write a script that displays the result of `BREATH` to the power `LOVE`
* `BREATH` and `LOVE` are environment variables
* The script should display the result, followed by a new line
```bash
echo $((BREATH ** LOVE))
```
## Task 11
Write a script that converts a number from base 2 to base 10.
* The number in base 2 is stored in the environment variable `BINARY`
* The script should display the number in base 10, followed by a new line
```bash
echo "$((2#$BINARY))"
```
## Task 12
 prints all possible combinations of two letters, except `oo`.
* Letters are lower cases, from `a` to `z`
* One combination per line
* The output should be alpha ordered, starting with `aa`
* Do not print `oo`
* Your script file should contain maximum 64 characters
```bash
echo {a..z}{a..z} | tr " " "\n" | grep -v "oo"
```
## Task 13
Print a number with two decimal places, followed by a new line.
The number will be stored in the environment variable `NUM`.
```bash
printf "%.2f\n" $NUM
```
## Task 100
Convert a number from base 10 to base 16.
* The number in base 10 is stored in the environment variable `DECIMAL`
* The script should display the number in base 16, followed by a new line
```bash
printf '%x\n' $DECIMAL
```
## Task 101
Encode and decode text using the rot13 encryption. Assume ASCII.
```bash
tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
## Task 102
Print every other line from the input, starting with the first line.
```bash
paste -d, - - | cut -d, -f1
```
## Task 103
Add the two numbers stored in the environment variables `WATER` and `STIR` and prints the result.
* `WATER` is in base `water`
* `STIR` is in base `stir`
* The result should be in base `bestchol`
```bash
printf "%o\n" $(( $((5#$(echo $WATER | tr water 01234))) + $((5#$(echo $STIR | tr stir. 01234))) )) | tr 01234567 bestchol
```

