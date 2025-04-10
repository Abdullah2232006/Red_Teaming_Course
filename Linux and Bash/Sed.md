![[Pasted image 20250408220010.png]]

### `sed 's/oldWord/newWord/flags' < inputFile > outputFile`


| Command                                                                  | Explanation                                                                               |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| `sed 's/OldWord/NewWord/flags' < InputFile > OutputFile`                 | To change / replace a word in a file                                                      |
| `sed 's/OldWord/NewWord/;s/OldWord1/NewWord1/' < InputFile > OutputFile` | To change / replace more than one word in a file                                          |
| `sed 's/OldWord/NewWord/g' < InputFile > OutputFile`                     | - To change each / all of the `OldWord` in a file.<br>- `g` means global and it is a flag |
| `sed -i 's/OldWord/NewWord/flags' < InputFile > OutputFile`              | To save the result of `sed` in the original file                                          |
| `sed '/Word/d' file.txt`                                                 | To delete a word from a file                                                              |
| `sed -i '/Word/d' file.txt`                                              | To save the file after deleting a word                                                    |
|                                                                          |                                                                                           |
### Notes

1. `sed`  doesn't change the value of the original file.
2. If there is multiple number of `OldWord` the replacement will happen for the first `OldWord` in each file -> when using the normal `sed` without the`/g`.