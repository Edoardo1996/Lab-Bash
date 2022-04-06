![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Bash

## Introduction

In this lab we are going to practice with [`bash`](<https://en.wikipedia.org/wiki/Bash_(Unix_shell)>), a shell and command-line language!

## Setup

1. Fork the repo in your git hub account and then clone the folder "lab-bash" to your machine and navigate to it folder.

2. Check the contents of the folder using the "ls" command

```shell
$ ls
```

and you should see the following:

```shell
exercises  inputs  lorem  lorem-copy  modules  outputs  README.md
```

3. Stay in the same directory/folder and complete the following exercises.

## Exercises

1. Using the echo command print in console "Hello World". Here is some info about echo command [https://discuss.codecademy.com/t/what-are-practical-uses-of-the-echo-command/394788]
echo <smth_to_print>
Print a string (also files?) to console, but also environment variables

2. Create a new directory called `new_dir`.
- mkdir <new_dir>
Create a new directory in working directory

3. Delete/Remove the directory `new_dir`.
- rm -d <dir>
Remove an existing directory

4. Copy the file `sed.txt` from the `lorem` folder and paste it to the folder `lorem-copy` folder.
- cp <path_file_to_copy> <path_in_which_to_copy>
Copy a file to another location

5. Copy the other two files from the `lorem folder` to `lorem-copy` folder in just one line using semicolon `;`.
It is possible to concat statements with semicolon ;

6. Show the `sed.txt` file content from the `lorem` folder.
There are multiple commands:
- cat <filename>
Visualize a text file (only .txt?) in bash shell.

- less <filename>
Visualize a cut-content of a long (.txt?) file
With flag -FX behaves like cat

7. Show the `at.txt` file and `lorem.txt` file contents from `lorem` folder.
We can simply concatenate the statements
cat <filename1> <filename2> 

8. Print the first 3 rows in `sed.txt` file from lorem-copy folder.
- head -<n> <filename>
Print in the shell the firs <n> rows of <filename>

9. Print the last 3 rows in `sed.txt` file from lorem-copy folder.
- tail -<n-1> <filename>
Print in the shell the last <n> rows of <filename>

10. Add `Homo homini lupus.` at the end of `sed.txt` file in the `lorem-copy` folder.
- echo "<some_text>" >> <filename>
Append text to a file

11. Print the last 3 rows in `sed.txt` file from `lorem-copy` folder. You should see `Homo homini lupus.`.
OK!

12. `sed` command is used to replace the text in a file. Use the `sed` command to replace all occurances of `et` with `ET` in the file `at.txt` file present in the folder `lorem`. You can use the following link to refer to `sed` commands [https://www.linode.com/docs/guides/manipulate-text-from-the-command-line-with-sed/]
Check the contents of the sed.txt file using `cat` command.
- sed -i 's/old-text/new-text/g' input.txt
The s is the substitute command of sed for find and replace
It tells sed to find all occurrences of ‘old-text’ and replace with ‘new-text’ in a file named input.txt

13. Find who is the system user. 
- whoami
Command whoami tells us the name of the user also.

14. Find the current path of the directory you are in.
- pwd
Displays current working directory

15. List all files with the extension `.txt` in lorem folder.
ls *.<ext>
Displays all file with the desired extension

16. Count the rows in `sed.txt` file from lorem folder. Look concatenate `cat` and `wc` with the pipe `|`.

- cat <filename> | wc -l
The wc command is used to find the number of lines, characters, words, and bytes of a file.
To find the number of lines using wc, we add the -l option. This will give us the total number of lines and the name of the file.
We can tell the shell to redirect the file to standard input of the wc -l command. This will give us the number of lines without the filename.

17. Count the **files** which start with `lorem` in all directories.
find <directory> -type f | wc -l
 the “find” command is used in order to search for files on your system.
When used with the “-f” option, you are targeting ony files.
By default, the “find” command does not stop at the first depth of the directory : 
t will explore every single subdirectory, making the file searching recursive.

## Bonus

20. Store your `name` in a variable with `read` command.
- read
read catches a line of input NAME. 
When NAME is not specified, a variable named REPLY is used to store user input.


21. Print that variable.
variable then can be printed with ${REPLY}

22. Create a new directory named with variable `name`.
Simply:
mkdir ${REPLY}

23. Remove that directory.
Simply:
rm -d ${REPLY}