# Learning Bash Shell Scripting

## Introduction

- A **Shell** is "A Program that interprets the commands you type in your terminal and passes them on to the operating system."
- The Purpose of the shell is to make it more convenient for you to issue commands to your computer.
- There are many different types of Shell: The Bourne Shell(sh), The GNU Bourne-Again Shell(bash), The C Shell(csh), The Korn Shell (ksh), The Z Shell(zsh), etc..
- **Bash**
  - It is arguably the most commonly used Linux shell today.
  - It is feature-rich.
  - It is fast.
- A **Shell Script** is a file containing commands for the shell. A Bash script is a file containing commands for the bash shell.
- Scripts allow automation.

### The Core Components of a Bash Script.

- Structure of a Bash Script: There are three core parts of a Bash Script—A Beginning, A Middle and An End.
- A Bash Script always begin with **Shebang line(#!)**. It basically tells the shell, what interpreter should be used to read the file.
- Shebang line is followed by the path of the interpreter.
- The Middle part consist of the series of commands to run.
- The end part is the Exit Statement(0 = successful;1-255 = unsuccessful)
- Below is an example of a sample Bash Script.
```
#!/bin/bash

echo "This is my first script"
exit 0
```
- Use the command: `chmod +x <script-file-name>` to grant execution access to the file.
- To run the script: `./<script-file-name>` from the same directory in Bash.

### File Permissions

- In Linux, 10 characters represent file permissions. The first characters is a standalone, the remaining nine are broken down in 3 sets of 3 characters.
- The first character is either "-" or "d". "-" represents a file, "d" represents directory.
- The next set of three characters represents permission the file owner has for the file. 
  - The first character is for read permission. If there is a read permission, there will be "r" else "-".
  - The second character is for write permission. If there is a write permission, there will be "w", else "-".
  - The third character is for execute permission. If there is an execute permission, there will be "x", else "-".
- The next two sets follow same patterns and are for User groups and every other user in the system.
- Command: `chmod 744 <script-file-name>` grants only the file owner all access (read, write, execute) and only read access to all other users.
- `744` is called Octo-number. Refer to https://chmod-calculator.com/ to get relevant Octo-number.

## Example 1

**Write a Bash Script that can back up all files in the home directory.**


```shell
#!/usr/bin/env bash

tar -cvf ~/mlops_session/my_backup_"$(date +%d-%m-%Y_%H-%M-%S)".tar ~/* 2>/dev/null
exit 0
```
- Run command `chmod 754 <script-file-name>` for relevant permissions.