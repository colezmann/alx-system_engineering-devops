#!/bin/bash
0- su betty: switches the current user to the user 'betty'
1- whoami: prints the effective username of the current user
2- groups: prints all the groups the current user is part of
3- chown betty hello: changes the owner of the file 'hello' to the user 'betty'
4- touch hello: creates an empty file called 'hello'
5- chmod u+x hello: adds execute permission to the owner of the file 'hello'
6- chmod ug+x,o+r hello: adds execute permission to the owner and the group owner, and read permission to other users, of the file 'hello'
7- chmod a+x hello: adds execution permission to the owner, the group owner and the other users, of the file 'hello'
8- chmod 007 hello: sets the permissions of the file 'hello' as follows
	Owner - no permission at all
	Group - no permission at all
	Other users - all the permissions
9- chmod 753 hello: sets the mode of the file 'hello' to: -rwxr-x-wx
10- chmod --reference=olleh hello: sets the mode of the file 'hello' as the same as 'olleh''s mode
11- chmod a+X *: adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files are not changed.
12- mkdir -m 751 my_dir: creates a directory called 'my_dir' with permissions 751 in the working directory
13- chgrp school hello: changes the group owner to 'school' for the file 'hello'
100- chown vincent:staff *: changes the owner to 'vincent' and the group owner to 'staff' for all the files and directories in the working directory
101- chown -h vincent:staff _hello: changes the owner and the group owner of '_hello' file to 'vincent' and 'staff' respectively. The file'_hello' is a symbolic link.
102- chown --from=guillaume betty hello: changes the owner of the file 'hello' to 'betty' only if it is owned by the user 'guillaume'
103- telnet towel.blinkenlights.nl: will play te StarWars IV episode in the terminal
