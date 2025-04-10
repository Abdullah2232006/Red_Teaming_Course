Bash is the language that you can write scripts (programs ) in Linux.
You can create file `xyz.sh` and then write all commands you need then execute it with `bash xyz.sh`.


| Command                                      | Use / Explanation                              |
| -------------------------------------------- | ---------------------------------------------- |
| `#!/bin/bash`                                | Added at the first line in the code            |
| `file.sh`                                    | Bash file                                      |
| `bash file.sh`                               | To run the bash file                           |
| `name = "name"`                              | Create a variable called name                  |
| `echo $name`                                 | To print value of the variable name            |
| `$0`                                         | Argument - Name of the file                    |
| `$1`                                         | Argument - First argument after `bash file.sh` |
| `echo "File name : $0, first name : $1"`     | Argument code                                  |
| `for i in {1..10}; do echo "$i";done`        | For loop in bash                               |
| for i in `cat file.txt`; do echo $i; done    | For loop on a file to print word by word       |
| `for i in $(cat file.txt); do echo $i; done` | For loop on a file to print word by word       |
| for i in `command` ; do echo $i; done        | To get the output of a command ex : `ifconfig` |
|                                              |                                                |
