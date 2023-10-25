# Basic

{% code overflow="wrap" %}
```bash
$ man hier
provides description of filesystem hierarchy

$ ls **/*.txt
used to list all the .txt files in current directories and sub directories. 
files and directories are separated by / (separator)
anything btwn separator is called segment
Process of specifying multiply files and directories is called Globbing

$ shopt -s globstar
to set globstar when globbing does not work

$ ls -R 
used to list all the files in directory recursively

$ tree
similar to ls -R but is not pre installed and displays directory contents in tree form

$ cp -R src dest
used to copy the contents of directory

$ mkdir -p directory_name
-p = used to create all folders that do not exists in mentioned path

All folders must have the execute permission, otherwise their contents cannot be explored.
permissions has a numeric value and a letter designation. Read is r or 4. Write is w or 2. Execute is x or 1. The different user classifications are user/owner (u), group (g), others (o), or all (a).

$ less filename
Used to view large files in paged manner
while the file is open, to search a text use from top - 
/<word>
for backward search use - 
?<word>

$ ln filename hardlinkname
used to create a hard link hardlinkname of filename. It references the physical file location in storage. Any changes to original file is reflected in hardlinkname. If original file is moved or deleted, link file exists unless deleted. Cannot be used for directory

$ ln -s filename softlinkname
used to create soft/symbolic link softlinkname of filename.
soft or symbolic links references the file or directory on file system and not storage. If original file is moved or deleted, symbolic link will not work. can cross file system (files on different partitions)

$ apt search package_name
used to search for a package from repository

$ apt show package_name
used to show the details of the package

$ !!
gets the previously entered command

$ !history_no
used to execute command from history at history_no position

$ !command_name
used to execute the last command_name

$ ^original^new^
used to replace original command with new
e.g. if previous command was $ cat file1.txt we can replace file1.txt with file2.txt using $ ^file1.txt^file2.txt^

$ ll "$(cat filename)"
ls does not take stdin from another command. here we use command substitution where command inside $() is executed first in the subshell and then is passed as command line argument to ll

$ chown [-R] owner_name[:group_name] target
-R = change recursively the file and directories 
group_name is optional

$ chgrp -R group_name target
used to change the group owner

$ zcat file_name
same as cat but on compressed files

$ zless file_name
view compressed file similar to less

$ head file_name
used to display 1st 10 lines by default

-n no_of_lines OR --lines=no_of_lines
used to specify no of lines to be displayed

$ tail file_name
reverse of head command

$ tail -f file_name
This flag keeps an open connection to the file and continues refreshing as content is added to the file

$ grep -il word
-i = ignore the case
-l = displays the file name in wich the word is present

$ grep -l pattern * 
used to print only filename matching pattern

```
{% endcode %}
