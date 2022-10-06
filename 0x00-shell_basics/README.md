#!/bin/bash
0- pwd: prints the absolute path name of the current working directory
1- ls: displays the content list of the current directory
2- cd: changes the working directory to the user's home directory
3- ls -l: displays current directory contents in a long format
4- ls -la: displays current directory contents (including hidden files) in a long format
5- ls -lna: displays current directory contents in long format, with user and group IDs displayed numerically, and hidden files (starting with .)
6- mkdir /tmp/my_first_directory/: creates a directory in the /tmp/ directory
7- mv /tmp/betty /tmp/my_first_directory/betty: moves the file 'betty' from /tmp to /tmp/my_first_directory
8- rm /tmp/my_first_directory/betty: deletes the file 'betty'
9- rm /tmp/my_first_directory: deletes the directory 'my_first_directory'
10- cd -: changes the working directory to the previous one
11- ls -la . .. /boot: lists all files (including hidden files) in the current directory, the parent of the working directory and the '/boot' directory (in this order) in long format
12- file /tmp/iamafile: prints the type of file named 'iamafile' located in the /tmp directory
13- ln -s /bin/ls __ls__: creates a symbolic link to /bin/ls named __ls__ (created in the current working directory)
14- cp -nu *.html ..: copies all the HTML files from the current working directory to the parent of the working directory, but only copies files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory
100- mv [[:upper:]]* /tmp/u: moves all files beginning with an uppercase letter to the directory /tmp/u
101- rm *~: deletes all files in the current working directory that end with the character ~
102- mkdir -p welcome/to/school: creates the directories 'welcome/' 'welcome/to' and 'welcome/to/school' all inside the current working directory
103- ls -pamv: lists all the files and directories of the current directory, separated by commas(,). Directory names end with a slash(/); files and directories starting with a dot(.) are listed; the listing is in alphabetic order (except for the directories . and .. which are at the very beginning); only letters and digits are used to sort (digits should come first); all files have at least one letter or one digit; the listing ends with a new line.
school.mgc: creates a magic file that can be used with the command 'file' to detect 'School' data files. 'School' data files always contain the string 'SCHOOL' at offset 0.
