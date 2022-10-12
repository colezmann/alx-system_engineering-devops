0- `echo "Hello, World"`:		prints `Hello, World` followed by a new line to the standard output.

1- `echo "\"(Ôo)'"`:			displays a confused smiley.

2- `cat /etc/passwd`:			displays the content of the `/etc/passwd` file.

3- `cat /etc/passwd /etc/hosts`:	displays the content of `/etc/passwd` and `/etc/hosts`.

4- `tail /etc/passwd`:			displays the last 10 lines of `/etc/passwd`.

5- `head /etc/passwd`:			displays the first 10 lines of `/etc/passwd`.

6- `head -n 3 iacta | tail -n 1`: 	displays the third line of the file `iacta`.

7- `echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)`:
					creates a file named exactly `\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)` containing the text "Best School" ending by a new line.

8- `ls -la > ls_cwd_content`:		writes into the file `ls_cwd_content` the result of the command `ls-la`. If the file `ls_cwd_content` already exists, this command overwrites its content. If the file `ls_cwd_content` doesn't exist, this command creates it.

9- `tail -n 1 iacta >> iacta`:		duplicates the last line of the file `iacta` and appends the result to the file `iacta`.

10- `find . -type f -name "*.js" -delete`:
					deletes all the regular files (not the directories) with a `.js` extension that are present in the current directory and all its subfolders.	

11- `find . -type d -not -name '.' | wc -l`:
					counts the number of directories and sub-directories in the current directory.
					_The current and parent directories are not taken into account_.
					_Hidden directories are counted_.

12- `ls -t1 | head -n 10`:		displays the 10 newest files in the current directory.
					_One file per line_.
					_Sorted from the newest to the oldest_.

13- `sort | uniq -u`:			takes a list of words as inputs and prints only words that appear exactly once.
					_Input format: One line, one word_.
					_Output format: One line, one word_.
					_Words are sorted_.

14- `grep -i "root" /etc/passwd`:	displays lines containing the pattern "root" from the file `/etc/passwd`.

15- `grep -c -i "bin" /etc/passwd`:	displays the number of lines that contain the pattern "bin" in the file `/etc/passwd`.

16- `grep -i "root" -A 3 /etc/passwd`:	displays lines containing the pattern "root" and 3 lines after them in the file `/etc/passwd`.

17- `grep -i -v "bin" /etc/passwd`:	displays all the lines in the file `/etc/passwd` that do not contain the pattern "bin".

18- `grep -i "^[a-z]" /etc/ssh/sshd_config`:
					displays all lines of the file `/etc/ssh/sshd_config` starting with a letter.
					_includes capital letters as well_.

19- `tr "A" "Z" | tr "c" "e"`:		replaces all characters `A` and `c` from input to `z` and `e` respectively.

20- `tr -d "cC"`:			removes all letters `c` and `C` from input.

21- `rev`:				reverses its input.

22- `cut -d ':' -f 1,6 /etc/passwd | sort`:
					displays all users and their home directories, sorted by users.
					_Based on the `/etc/passwd` file_.

23- `find . -empty | rev | cut -d '/' -f 1 | rev`:
					finds all empty files and directories in the current directory and all sub-directories.
					_Only the names of the files and directories are displayed (not the entire path)_.
					_Hidden files are listed_.
					_One file name per line_.
					_The listing ends with a new line_.

24- `find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d "." -f 2- | rev | LC_ALL=C sort -f`:
					lists all the files with a `.gif` extension in the current directory and all its sub-directories.
					_Hidden files are listed_.
					_Only regular files (not directories) are listed_.
					_The names of the files are displayed without their extensions_.
					_The files are sorted by byte values, but case-insensitive (file `aaa` is listed before file `bbb`, file `.b` is listed before file `a`, and file `Rona` is listed after file `jay`)_.
					_One file name per line_.
					_The listing ends with a new line_.

25- `cut -c 1 | paste -s -d ''`:	decodes acrostics that use the first letter of each line.
					_The 'decoded' message ends with a new line_.

26- `tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev`:
					parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.
					_Ordered by number of requests, most active host or IP at the top_.
