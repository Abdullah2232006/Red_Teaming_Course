# 3. Lecture 1.1 - introduction to linux OS

<aside> 💡

Permission denied ⇒ sudo

</aside>

<aside> 💡

Debian = kali

</aside>

| Command          | Explanation                                                               |
| ---------------- | ------------------------------------------------------------------------- |
| `sudo + command` | To perform commands as admin “root” instead of being a normal user “kali” |
| `sudo su`        | To always be sudo “super user”                                            |
| `exit`           | To exit the sudo mode                                                     |
| `whoami`         | To see the current user                                                   |
| `pwd`            | To see the current directory                                              |
| `ls`             | _list_ - To list all of the included folders and file in the directory    |
| `clear`          | To clear the terminal                                                     |
| ctrl + l         | same as clear but it doesn’t delete the data in the terminal              |
| `cd directory`   | _change directory_                                                        |
| `cd ..`          | _change directory_ - return back to the previous directory                |
| `cat file`       | To show the contents of a **file**                                        |

<aside> 💡

Directories are colored in blue, while files are colored in white.

</aside>

# 4. Lecture 1.2 - linux commands

|Command|Explanation|
|---|---|
|`nano file`|To create a file|
|Nano is a text editor, like the notepad||
|ctrl + O ⇒ `write out`|To save the edits inside NANO|
|ctrl + X|To exit the nano text editor|
|`cat fileName`|To show the contents of a file|
|`rm file`|To _remove_ a file|
|`rm -r directoryName`|To _remove_ a directory|
|`mkdir`|To _make directory_|
|`rmdir directoryName`|To _remove_ a directory|
|`/`|The root path|
|`cp file or dirName destination Folder InThe Same DirPath`|To copy a file to a directory located in the same directory|
|`mv file or dirName destination Folder Path`|To move a to a directory located in the same directory or to another directory using the absolute path|
|`mv fileName newname`|To rename a file|
|`echo "text" > fileName`|To **Write** (add new text and remove the old ones) in a file|
|`echo "text" >> fileName`|To **Append** (add new text while keeping the old ones) in a file|

## Types of Paths

1. Absolute path
    1. Starts with `/`
    2. The complete path
2. Relative path
    1. A part of the path

# 5. Lecture 1.3 - linux commands (Network)

| Command                             | Explanation                                                                       |
| ----------------------------------- | --------------------------------------------------------------------------------- |
| `ifconfig`                          | Displays some information about the network (IP address, etc…)                    |
| `df -h`                             | Displays some information about the hard disk                                     |
| `free`                              | Displays some information about the memory space                                  |
| `ps aux`                            | Displays some information about the processor                                     |
| `kill PID`                          | To kill a working operation after doing `ps aux`                                  |
| `apt install toolName`              | To install an application (a store)                                               |
| `snap install toolName`             | To install an application (a store) (should be installed firstly using apt)       |
| `dpkg -i toolName`                  | To _download a package._ To install a downloaded package with an extension `.deb` |
| `snap list`                         | Displays contents of snap                                                         |
| `sudo !!`                           | To repeat the previous command with sudo permissions                              |
| `ls -lah`                           | To see the permissions of files and folders                                       |
| `chmod 777 test.txt`                | To change the permissions of a file or a folder                                   |
| `chmod +x test.txt`                 | To add execute permission to a file xyz.txt                                       |
| \|                                  | To redirect the output to another command use                                     |
| `cat test.txt \| grep "text"`       | To get a word from a file                                                         |
| `cat test.txt \| wc`                | To get the number of lines, words and characters in a file                        |
| `more`                              | can be used instead of `cat`                                                      |
| `.` before the file name            | To hide a file or a folder                                                        |
| `name *` or `name ./*`              | To know the type of files                                                         |
| `du DIRECTORYNAME`                  | To know the size of a directory                                                   |
| `ssh -p PORTNUMBER USERNAME@DOMAIN` | ssh                                                                               |


## Permissions for files

1. Execute → 1 → x
2. Write → 2 → w
3. Read → 4 → r

If you need Read and Write ⇒ 2 + 4 = 6, and so on.
- x + r = 5
- w + e = 3
- r + w = 6
- x + w + r = 7

![[-rw-rw-r--.png]]

## Find 
`find [STARTINGDIRECTORY] [options] [expression]`
`find inhere -type f -size 1033c -readable ! -executable`

==find inhere== → Search inside the inhere directory.

==-type f== → Look for files only.

==-size 1033c== → Find files that are exactly 1033 bytes (c stands for bytes).

==-readable== → Ensure the file is human-readable.

==! -executable== → Exclude executable files.