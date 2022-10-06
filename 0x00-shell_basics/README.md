#!/bin/bash
pwd: prints the absolute path name of the current working directory
ls: displays the content list of the current directory
cd: changes the working directory to the user's home directory
ls -l: displays current directory contents in a long format
ls -la: displays current directory contents (including hidden files) in a long format
ls -lna: displays current directory contents in long format, with user and group IDs displayed numerically, and hidden files (starting with .)
mkdir /tmp/my_first_directory/: creates a directory in the /tmp/ directory
mv /tmp/betty /tmp/my_first_directory/betty: moves the file 'betty' from /tmp to /tmp/my_first_directory
rm /tmp/my_first_directory/betty: deletes the file 'betty'
rm /tmp/my_first_directory: deletes the directory 'my_first_directory'
cd -: changes the working directory to the previous one
ls -la . .. /boot: lists all files (including hidden files) in the current directory, the parent of the working directory and the '/boot' directory (in this order) in long format
file /tmp/iamafile: prints the type of file named 'iamafile' located in the /tmp directory
ln -s /bin/ls __ls__: creates a symbolic link to /bin/ls named __ls__ (created in the current working directory)
cp -nu *.html ..: copies all the HTML files from the current working directory to the parent of the working directory, but only copies files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory
