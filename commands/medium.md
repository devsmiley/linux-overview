# Medium

{% code overflow="wrap" %}
```bash

$ df -h
used to display different volumes on hard drive
-h = human readable

$ du -hsP
used to display disk space used by individual file
-h = human readable
-s = total space used
-P = not to follow symbolic links 

$ tar -c/x z/j vf dest_name src_dir
-c/x = create/extract tarball (bundling files)
-z/j = gunzip/bunzip2 (compressing algo)
-v = verify proper extraction or compression
-f = file name

$ free
used to display resources available on server

$ hostname
returns host name as configured in /etc/hostname file

$ useradd -d home_dir -p password -m user_name
used to create new user to host
-d = specify home directory than default
-m = create user's home directory
-p = password for new account

$ userdel usern_name
used to delete user account from host

$ usermod
used to change the properties of a user. This command needs to be executed only as a root user.

$ passwd user_name
used to reset user password. while updating other user's password, no need to provide current one

$ tee file_name
used to pass the output from another command and copying to file_name

$ pushd new_directory_name
used to push the current directory in stack and move to new directory
E.g. If we are working in Desktop folder and wish to go to Downloads folder, use
$ pushd Downloads

$ popd
this will pop the last directory value that was pushed to the stack and move us there

In this case, it will return us back to Desktop folder

$ nmcli -p device show
nmcli = command line tool for controlling Network Manager
-p = pretty
this command shows info of all the interfaces connected to the device

$ find directory ! -name filename/wildcard -exec command {} +
used to execute command on files/folders in directory excluding filename/wildcard files/folders

$ fdisk
used to view and alter the partitioning scheme used on your hard drive

$ awk -F "separator" "operation"
used to perform text transformations.

$ ip link set eth/wireless_conn down/up
used to disconnect/connect to the network

$ rsync -avzh src_path dest_path
a = archive; use recursion and preserve everything
v = verbose
z = compression
h = human readable
used to copy files from src to dest

$ crontab -e
used to create a cronjob for the logged in user

$ crontab -l
used to list all the cronjobs for the user

$ crontab -r
used to delete the cronjob for the user

$ /etc/init.d
startup script added to the path for processes to run during boot up

$ /etc/rc*.d
they are run level directories. When the system boots, we can choose the run level
rc5.d = for desktop systems
rc3.d = servers
rc1.d = for debugging or finding corrupt file or directories, etc.

$ scp local_file_name remote_uname@remote_ip:path
Copy from current system to remote

$ scp remote_uname@remote_ip:path local_file_name
Copy from remote system to current system

$ nslookup
used to query name resolution for a domain

$ server ip
with nslookup, the ip mentioned will be used as default server for queries


```
{% endcode %}
