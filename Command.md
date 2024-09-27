# LINUX
```
Linux is an open-source operating system based on the Unix architecture. that's stable and secure, often used for servers and desktops.
```
# Linus distribution 
```
Debian systems and Red Hat systems.
```

# File System Hierarchy
```
Root Directory (/): The starting point of the file system.
Common Directories:
/home: User home directories.
/etc: Configuration files.
/var: Variable data (logs, databases).
/bin: Essential command binaries.
```

# Comman Command
```
info – Manual browser, The GNU alternative to man
man – The standard unix documentation system
which - locate a command
wc - print newline, word, and byte counts for each file
locate - find files by name
Realpath <file.name> - provide file path
ln – Link one file/directory to another
find – Search for files through a directory hierarchy
quota – display disk usage and limits
du – Calculate used disk space
more – Pager
less – Improved more-like text pager
exit - cause normal process termination
logout – terminates login shell
dd - Convert and copy a file (Disk Dump)
uptime – Print how long the system has been running
history - GNU History Library
tar – Tape ARchiver, concatenates files
passwd – Change user password
su – Start a new process (defaults to shell) as a different user (defaults to root)
sudo – execute a command as a different user.
who – Show who is logged on (with some details)

Package Management
Debian-Based Systems:
apt update: Update package list.
apt install <package>: Install a package.
Red Hat-Based Systems:
yum update: Update packages.
yum install <package>: Install a package.
```

# 1. File and Directory Management Commands

```
ls
ls lists files in the current directory.

ls -l
-l shows detailed information like permissions, ownership, and file size.

cd /home/user
cd changes the current directory.

cd ..
cd .. moves up one directory.

pwd
Displays the full path of the current directory.

mkdir <new_folder_name>
It create a new directory

mkdir -p /path/to/multiple/directories
-p creates parent directories as needed.

touch
This Command by default creates an empty file.


cp – Copy command

cp <source_file> <destination_file>
It copies the source file content to destination file

cp -r /path/to/source/ /path/to/destination/
-r recursively copies directories.


mv – Move or rename command

mv <oldfile_name> <newfile_name>
It moves the content from one file to another file

mv <file.txt> </path/to/new/location/>
Renames or moves files and directories.


rm – Remove command

rm –f <file_name>
It removes or deletes the files

rm -rf <directory_name>
force remove the files & folders of directory recursively (-f force).

rmdir <empty_folder>
Removes empty directories.
```

# 2. File Viewing and Editing

```
cat <file_name>
Displays the contents of a file.

tac <file_name>
Display file content in reverse order

less <file_name>
View file content one screen at a time
Use arrow keys to scroll, q to quit.

head <file_name>
View the first 10 lines of a file

head -n 5 <file_name>
-n specifies the number of lines to display.

tail <file_name>
View the last 10 lines of a file

tail -n 5 <file_name>
-n specifies the number of lines to display.

echo – display line of text
cut – Remove sections from each line of a file or
standard input
paste - merge lines of files
diff – Compare two text files line by line
sort - sort lines of text files
cmp – Compare two files byte for byte
join – Join lines of two files on a common field

Searching and Finding

find <path> -name <filename>: Search for a file by name.
grep <pattern> <file>: Search for a pattern within a file, to search for text within files.
awk – A pattern scanning and processing language
```

#3. File Permissions and Ownership

```
Change file permissions

chmod 755 <file_name>
755 grants read, write, execute for the owner, and read/execute for group and others.

chmod u+x <file_name>
u+x adds execute permission for the owner.

chown user:group <file_name>
Changes the owner and group of a file.

chgrp group_name <file_name>
Changes the group ownership which is associated with a file.
```

# 4. Disk Usage and Storage

```
df -h
Display disk space usage
-h shows human-readable sizes (KB, MB, GB).

du -sh /path/to/directory/
Estimate file space usage
-s provides a summary, and -h shows human-readable sizes.
```

# 5. Process Management

```
ps
shows the currently running process.

ps -ef
Displays all processes running on the system.

top
Shows the real-time, dynamic view of the running processes of a system.

kill <pid>
Terminate a process PID

kill -9 <pid>
-9 forces termination.
```

# 6. Networking Commands

```
ifconfig
Displays the network interface information.

ping <hostname>
Test network connection. It tests the reachability & responsiveness of the remote host.

netstat -lntp
Displays all listening ports and connections.

ssh user@<remote_host_address>
Securely connect to a remote machine
Connects to a remote system via SSH.

wget <url>
Download files from the web

curl <url>
Downloads the content <url> and displays it in the terminal.
```

# 7. System Information

```
uname
Displays kernel and system information.

hostname
Shows the name of the system host.

hostid
shows the host id of the system assigned by the OS

uptime
Shows the elapsed time duration since the machine logged in.

whoami
Shows the currently logged-in username of the terminal.

last
Displays a list of recent logins.

date
Shows the current date and time in UTC format.

history
lists all the commands executed until now
```

# 8. Package Management

```
Package management for RedHat

sudo dnf update
Refresh the list of available packages.
Check for newer versions of installed software.

sudo dnf install <package_name>
Installing the packages

sudo dnf remove <package_name>
removing the package
```

# 9. Service Management

```
sudo systemctl start <service name>
To start the service

sudo systemctl enable <service name>
To enable the service

sudo systemctl disable <service name>
To disable the service

sudo systemctl status <service name>
check the status of the service

sudo systemctl restart <service name>
To restart a service
```

# System Monitoring
```
Disk Usage: df -h shows disk space usage.
Memory Usage: free -m shows memory usage.
```
# Scheduled Tasks
```
Cron Jobs: Use crontab -e to schedule recurring tasks.
```

# User Management
```
Add User: adduser <username>.
Delete User: deluser <username>.
Change Password: passwd <username>.
```

# Logs and Troubleshooting
```
View System Logs: Check /var/log/syslog or /var/log/messages.
Check Application Logs: Typically found in /var/log or specific application directories.
```

# Backup and Recovery
```
Basic Backup: Use cp or tar to create backups.
Restore Files: Use cp to restore from backup.
```

# Remote Access
```
SSH Access: Use ssh <user>@<hostname> to connect to remote servers securely.
```

# System Shutdown and Reboot
```
shutdown now: Immediately shut down the system.
reboot: Restart the system.
```
