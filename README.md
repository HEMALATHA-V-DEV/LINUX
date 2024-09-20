# LINUX
```
Linux is an open-source operating system based on the Unix architecture. that's stable and secure, often used for servers and desktops.
```

Linus distribution 
```
Debian systems and yum for Red Hat systems.
```

File System Hierarchy
```
Root Directory (/): The starting point of the file system.
Common Directories:
/home: User home directories.
/etc: Configuration files.
/var: Variable data (logs, databases).
/bin: Essential command binaries.
```

Basic Commands
```
File Operations:
ls: List files in a directory.
cd <directory>: Change directory.
pwd: Print the current working directory.
mkdir <directory>: Create a new directory.
rmdir <directory>: Remove an empty directory.
cp <source> <destination>: Copy files.
mv <source> <destination>: Move or rename files.
rm <file>: Remove files.
```

Viewing Files:
```
cat <file>: Display file contents.
less <file>: Scroll through file contents.
nano <file>: Edit a file with Nano editor.
head <file>: Display the first 10 lines of a file.
tail <file>: Display the last 10 lines of a file. Use tail -f <file> to view log files in real-time.
```

Searching and Finding
```
find <path> -name <filename>: Search for a file by name.
grep <pattern> <file>: Search for a pattern within a file, to search for text within files.
```

Permissions and Ownership
```
View Permissions: ls -l shows file permissions.
Change Permissions:
chmod <permissions> <file>: Change file permissions.
Change Ownership:
chown <user>:<group> <file>: Change file owner and group.
```

Networking Commands
```
Check Connectivity: ping <hostname> to test if a server is reachable.
View Network Configuration: ifconfig or ip addr show.
Display Active Connections: netstat -tuln.
```

Package Management
```
Debian-Based Systems:
apt update: Update package list.
apt install <package>: Install a package.
Red Hat-Based Systems:
yum update: Update packages.
yum install <package>: Install a package.
```

Process Management
```
ps: Display currently running processes. 
top: Display real-time process information. 
kill <PID>: Terminate a process by its Process ID (PID). Terminate Process - kill <PID> stops a process.
killall <process_name>: Kill all processes by name.
```

System Monitoring
```
Disk Usage: df -h shows disk space usage.
Memory Usage: free -m shows memory usage.
```

Scheduled Tasks

```
Cron Jobs: Use crontab -e to schedule recurring tasks.
```

User Management
```
Add User: adduser <username>.
Delete User: deluser <username>.
Change Password: passwd <username>.
```

Logs and Troubleshooting
```
View System Logs: Check /var/log/syslog or /var/log/messages.
Check Application Logs: Typically found in /var/log or specific application directories.
```

Backup and Recovery
```
Basic Backup: Use cp or tar to create backups.
Restore Files: Use cp to restore from backup.
```

File Compression
```
Compress Files: tar -czvf <archive.tar.gz> <directory>.
Extract Files: tar -xzvf <archive.tar.gz>.
```

Remote Access
```
SSH Access: Use ssh <user>@<hostname> to connect to remote servers securely.
```

disk usage in Linux?
```
df -h to see overall disk usage . Display disk space usage for all mounted filesystems.
du -sh <directory> for a specific folder's size.
```

System Shutdown and Reboot
```
shutdown now: Immediately shut down the system.
reboot: Restart the system.
```

ls command and its various options:

```
1. ls
What it does: Lists the files and directories in the current directory.

2. ls -l
What it does: Lists files and directories in a long format, providing detailed information including:

File permissions
Number of links
Owner name
Group name
File size
Last modified date and time
File or directory name
3. ls -ltr
What it does: Combines options to list files in long format (-l), sorted by modification time (-t), with the oldest files shown first (-r for reverse order).
```

difference between a hard link and a soft link?
```
Answer: A hard link directly points to a file's data, while a soft link (or symbolic link) points to the file's name. 
If the original file is deleted, a hard link still works, but a soft link does not.
```

What is a shell? What are the different types of shells?
```
Answer: A shell is a command-line interface for interacting with the operating system. Common types include Bash, Zsh, and Fish.
```

Shell Scripting
```
Automating tasks with scripts.

#!/bin/bash
echo "Hello, World!"
```

What is the purpose of the /etc/passwd file?
```
Answer: It stores user information, like usernames and home directories.
```

What are processes in Linux? How do you manage them?
```
Answer: Processes are running programs. You can view them with ps, see real-time info with top, and stop them with kill <PID>.
```

What is a daemon? How do you manage daemon processes?
```
Answer: A daemon is a background service. Manage them with systemctl, like systemctl start <service> to start one.
```

How do you check network connectivity?
```
Answer: Use ping <hostname> to check if a server is reachable. traceroute <hostname> shows the path taken to reach it.
```

What is a package manager? Give examples.
```
Answer: A package manager installs and manages software. Examples include apt for Debian systems and yum for Red Hat systems.
```

What are the different types of file permissions in Linux?
```
Answer: Permissions can be read (r), write (w), and execute (x). They can be set for the owner, group, and others.
```

What is the purpose of the cron service?
```
Answer: cron is used to schedule recurring tasks in Linux. You can edit the cron jobs using crontab -e.
```

How can you check the current memory usage?
```
Answer: Use the free -m command to see memory usage in megabytes.
```

How do you find the last modified files in a directory?
```
Answer: Use the command ls -lt to list files sorted by modification time, with the most recently modified files at the top.
```

How can you monitor system logs?
```
Answer: Use tail -f <logfile> to view logs in real-time, such as /var/log/syslog or /var/log/messages.
```


Simple Linux Questions

What is the name and the UID of the administrator user?
Answer: The administrator user is typically named root, and its User ID (UID) is 0.

How to list all files, including hidden ones, in a directory?
Answer: Use the command ls -a to list all files, including hidden files (those starting with a dot).

What is the Unix/Linux command to remove a directory and its contents?
Answer: Use rm -r directory_name to recursively remove a directory and all its contents.

Which command will show you free/used memory? Does free memory exist on Linux?
Answer: The command free -h shows free and used memory in a human-readable format. Yes, free memory exists on Linux.

How to search for the string "my konfu is the best" in files of a directory recursively?
Answer: Use the command grep -r "my konfu is the best" /directory to search for the string in all files within the specified directory.

How to connect to a remote server or what is SSH?
Answer: SSH (Secure Shell) is a protocol for securely connecting to remote servers. Use ssh user@hostname to connect to a remote server.

How to get all environment variables and how can you use them?
Answer: Use printenv or env to display all environment variables. You can use them in scripts or commands to access system configurations.

I get "command not found" when I run ifconfig -a. What can be wrong?
Answer: The command may not be installed on your system, or it could be located in a directory not included in your PATH. Try using ip addr instead, as ifconfig is deprecated in many distributions.

What happens if I type TAB-TAB?
Answer: Typing TAB twice will auto-complete the command or file name, showing possible completions if there are multiple options.

What command will show the available disk space on the Unix/Linux system?
Answer: Use df -h to display the available and used disk space in a human-readable format.

What commands do you know that can be used to check DNS records?
Answer: The commands dig and nslookup can be used to check DNS records.

What Unix/Linux commands will alter a file's ownership and file's permissions?
Answer: Use chown to change ownership and chmod to change permissions of a file.

What does chmod +x FILENAME do?
Answer: The command chmod +x FILENAME makes the file executable.

What does the permission 0750 on a file mean?
Answer: The permission 0750 means the owner can read, write, and execute the file; the group can read and execute; others have no permissions.

What does the permission 0750 on a directory mean?
Answer: For a directory, 0750 means the owner can read, write, and access the directory; the group can read and access it; others have no permissions.

How to add a new system user without login permissions?
Answer: Use useradd -s /sbin/nologin username to add a user without login permissions.

How to add/remove a group from a user?
Answer: Use usermod -aG groupname username to add a user to a group and gpasswd -d username groupname to remove a user from a group.

What is a bash alias?
Answer: A bash alias is a shortcut for a command. For example, alias ll='ls -l' creates an alias ll for the command ls -l.

How do you set the mail address of the root/a user?
Answer: You can set the mail address by echoing the address into /etc/mailname or configuring the /etc/aliases file.

What does CTRL-c do?
Answer: CTRL-c interrupts and kills the running foreground process in the terminal.

What does CTRL-d do?
Answer: CTRL-d sends an EOF (End Of File) signal, indicating no more input.

What does CTRL-z do?
Answer: CTRL-z suspends the currently running foreground process and puts it in the background.

What is in /etc/services?
Answer: The /etc/services file contains a list of network service names and their corresponding port numbers and protocols.

How to redirect STDOUT and STDERR in bash? (> /dev/null 2>&1)
Answer: The command command > /dev/null 2>&1 redirects both standard output (STDOUT) and standard error (STDERR) to /dev/null, effectively discarding them.

What is the difference between UNIX and Linux?
Answer: UNIX is a proprietary operating system, while Linux is an open-source operating system that is inspired by UNIX.

What is the difference between Telnet and SSH?
Answer: Telnet is an insecure protocol for accessing remote machines, while SSH (Secure Shell) provides encrypted, secure access.

Explain the three load averages and what do they indicate. What command can be used to view the load averages?
Answer: Load averages indicate the system load over the last 1, 5, and 15 minutes. Use the command uptime or top to view these averages.

Can you name a lower-case letter that is not a valid option for GNU ls?
Answer: The hyphen - is not a valid option.

What is a Linux kernel module?
Answer: A Linux kernel module is a piece of code that can be loaded into the kernel at runtime to extend its functionality.

Walk me through the steps in booting into single-user mode to troubleshoot a problem.
Answer: Modify the bootloader (GRUB) entry to add single or 1 to the kernel parameters, then boot the system to enter single-user mode.

Walk me through the steps you'd take to troubleshoot a 404 error on a web application you administer.
Answer: Check the server logs for error details, verify file permissions, ensure the URL is correct, and confirm that the web server is configured to serve the requested resource.

Medium Linux Questions

What do the following commands do and how would you use them?
tee: Reads from standard input and writes to standard output and files. Use: command | tee file_name.
awk: A powerful text processing tool for pattern matching and reporting. Use: awk '{print $1}' file.
tr: Translates or deletes characters. Use: echo "hello" | tr 'a-z' 'A-Z'.
cut: Cuts sections from lines of files. Use: cut -d':' -f1 /etc/passwd.
tac: Displays files in reverse. Use: tac filename.
curl: Transfers data to or from a server. Use: curl http://example.com.
wget: Downloads files from the web. Use: wget http://example.com/file.
watch: Executes a command periodically and displays the output. Use: watch -n 1 command.
head: Outputs the first few lines of a file. Use: head filename.
tail: Outputs the last few lines of a file. Use: tail filename.
less: View file contents interactively. Use: less filename.
cat: Concatenates and displays file contents. Use: cat filename.
touch: Creates an empty file or updates a file's timestamp. Use: touch filename.
sar: Collects and reports system activity information. Use: sar -u 1 3 to report CPU usage.
netstat: Displays network connections and routing tables. Use: netstat -tuln.
tcpdump: Captures and displays network packets. Use: tcpdump -i eth0.
lsof: Lists open files and associated processes. Use: lsof | grep process_name.

What does an & after a command do?
Answer: The & runs the command in the background, allowing the terminal to be used for other commands.

What does & disown after a command do?
Answer: Running & disown after a command puts it in the background and removes it from the shell’s job table, so it won't be terminated if the shell exits.

What is a packet filter and how does it work?
Answer: A packet filter is a network security mechanism that controls incoming and outgoing network traffic based on predetermined security rules.

What is Virtual Memory?
Answer: Virtual memory is a memory management technique that provides an "idealized abstraction" of the storage resources, allowing a system to use more memory than is physically available.

What is swap and what is it used for?
Answer: Swap is a space on a disk that is used as an extension of RAM; it helps improve performance when the physical memory is full.

What is an A record, an NS record, a PTR record, a CNAME record, an MX record?
Answer:
A Record: Maps a domain to an IPv4 address.
NS Record: Specifies the name servers for a domain.
PTR Record: Maps an IP address to a domain name (reverse DNS).
CNAME Record: Alias for another domain name.
MX Record: Specifies mail servers for a domain.

Are there any other RRs and what are they used for?
Answer: Yes, other Resource Records (RRs) include SRV (service locator), TXT (text information), and SPF (Sender Policy Framework).

What is a Split-Horizon DNS?
Answer: Split-horizon DNS is a configuration where a single DNS server provides different answers based on the source of the request (internal vs. external clients).

What is the sticky bit?
Answer: The sticky bit is a permission that allows only the owner of a file to delete or rename it in a directory. It is often used on shared directories like /tmp.

What does the immutable bit do to a file?
Answer: Setting the immutable bit on a file prevents it from being modified, deleted, or renamed. Use chattr +i filename to set it.

What is the difference between hardlinks and symlinks? What happens when you remove the source to a symlink/hardlink?
Answer: Hard links point directly to the inode of a file, while symlinks point to the file path. Removing the source of a hard link keeps the data accessible, but removing a symlink breaks the link.

What is an inode and what fields are stored in an inode?
Answer: An inode is a data structure that stores information about a file, including its size, permissions, ownership, timestamps, and disk block locations.

How to force/trigger a file system check on next reboot?
Answer: Use the command touch /forcefsck or modify the /etc/fstab entry with the fsck option.

What is SNMP and what is it used for?
Answer: SNMP (Simple Network Management Protocol) is used for network management, monitoring network devices, and gathering statistics.

What is a runlevel and how to get the current runlevel?
Answer: A runlevel defines the state of the machine (e.g., multi-user, single-user). Use runlevel or who -r to get the current runlevel.

What is SSH port forwarding?
Answer: SSH port forwarding allows you to tunnel network connections through an SSH connection, securing the traffic.

What is the difference between local and remote port forwarding?
Answer: Local port forwarding forwards traffic from a local port to a remote destination, while remote port forwarding forwards traffic from a remote port to a local destination.

What are the steps to add a user to a system without using useradd/adduser?
Answer: Manually edit the /etc/passwd file to add a new user entry and then create a home directory and set permissions.

What is MAJOR and MINOR numbers of special files?
Answer: MAJOR numbers identify the driver associated with a device, while MINOR numbers distinguish between devices managed by that driver.

Describe the mknod command and when you'd use it.
Answer: The mknod command creates special files (device files). Use it when you need to create a device file that isn’t automatically created by the system.

Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.
Answer: This can occur when the inode limit is reached, meaning there are no more inodes available for new files, even if disk space is free.

Describe a scenario when deleting a file, but 'df' not showing the space being freed.
Answer: If a file is deleted while a process is still using it, the space won't be freed until the process releases the file descriptor.

Describe how 'ps' works.
Answer: The ps command displays information about running processes, including their PID, memory usage, and CPU time.

What happens to a child process that dies and has no parent process to wait for it and what’s bad about this?
Answer: The child process becomes a zombie process. This wastes system resources and can lead to process table overflow.

Explain briefly each one of the process states.
Answer:
Running: The process is currently executing.
Sleeping: The process is waiting for an event.
Stopped: The process has been stopped, typically by receiving a signal.
Zombie: The process has completed execution but still has an entry in the process table.

How to know which process listens on a specific port?
Answer: Use lsof -i :port_number or netstat -tuln | grep port_number to identify the process.

What is a zombie process and what could be the cause of it?
Answer: A zombie process is a terminated process that remains in the process table. It occurs when the parent process has not read the exit status of the child.

You run a bash script and you want to see its output on your terminal and save it to a file at the same time. How could you do it?
Answer: Use bash script.sh | tee output_file.txt to display the output on the terminal and save it to a file.

Explain what echo "1" > /proc/sys/net/ipv4/ip_forward does.
Answer: This command enables IP forwarding, allowing the system to route packets between interfaces.

Describe briefly the steps you need to take in order to create and install a valid certificate for the site https://foo.example.com.
Answer: Generate a CSR (Certificate Signing Request), submit it to a Certificate Authority (CA), receive the certificate, and install it on your web server.

Can you have several HTTPS virtual hosts sharing the same IP?
Answer: Yes, you can use Server Name Indication (SNI) to host multiple HTTPS virtual hosts on the same IP address.

What is a wildcard certificate?
Answer: A wildcard certificate allows you to secure a domain and all its subdomains with a single certificate (e.g., *.example.com).

Which Linux file types do you know?
Answer: Common Linux file types include regular files, directories, symbolic links, character devices, block devices, and sockets.

What is the difference between a process and a thread? And parent and child processes after a fork system call?
Answer: A process is an independent execution unit, while a thread is a lightweight unit of execution within a process. After a fork, the parent process creates a child process that is a copy of itself.

What is the difference between exec and fork?
Answer: fork creates a new process by duplicating the existing process, while exec replaces the current process image with a new program.

What is "nohup" used for?
Answer: nohup allows a command to continue running after logging out or closing the terminal.

What is the difference between these two commands?
myvar=hello: This sets a variable in the current shell.
export myvar=hello: This sets a variable and makes it available to child processes.

How many NTP servers would you configure in your local ntp.conf?
Answer: It's recommended to configure at least 3 NTP servers for redundancy and accuracy.

What does the column 'reach' mean in ntpq -p output?
Answer: The 'reach' column indicates the status of the last eight responses received from the NTP server, showing connectivity.

You need to upgrade the kernel at 100-1000 servers, how would you do this?
Answer: Use configuration management tools like Ansible or Puppet to automate the upgrade process across all servers.

How can you get Host, Channel, ID, LUN of SCSI disk?
Answer: Use the command lsblk -o NAME,HCTL,SIZE,TYPE or lsscsi to get details about SCSI disks.

How to check the system for core dumps?
Answer: Check for core dumps in the directory specified by /proc/sys/kernel/core_pattern or search for files with the .core extension.

How to make a kernel module?
Answer: Write the module code, create a Makefile, and then use make to compile the module. Load it with insmod or modprobe.

How to change the default runlevel in RedHat?
Answer: Edit the /etc/inittab file and change the default runlevel number in the initdefault line.

Explain top command output.
Answer: The top command displays running processes and their resource usage, including CPU and memory consumption, along with system uptime and load averages.

What is a task scheduler in Linux?
Answer: The task scheduler manages process execution and CPU resource allocation, deciding which process runs at any given time.

How would you identify a hung process?
Answer: Use commands like ps, top, or htop to identify processes that are not responding, and check their status.

What is the function of /etc/hostname?
Answer: The /etc/hostname file contains the hostname of the system, which is used to identify the machine on the network.

How can you change the hostname of a running system?
Answer: Use the command hostnamectl set-hostname new_hostname to change the hostname on a running system.

What is the purpose of the /etc/hosts file?
Answer: The /etc/hosts file maps hostnames to IP addresses, allowing local hostname resolution without querying a DNS server.

How to create a symbolic link?
Answer: Use the command ln -s target_file link_name to create a symbolic link to the specified target file.

What is the purpose of the chmod command?
Answer: The chmod command is used to change the file permissions for users, groups, and others.

How to check the current users logged in to the system?
Answer: Use the who or w command to see the currently logged-in users and their activity.

What does grep do?
Answer: The grep command searches for patterns in files and outputs lines that match the specified pattern.

How to copy files and directories recursively?
Answer: Use cp -r source_directory destination_directory to copy files and directories, including all subdirectories.

How to move or rename a file?
Answer: Use the command mv old_filename new_filename to rename or move a file to a different directory.

What does df -h display?
Answer: The df -h command displays disk space usage in a human-readable format, showing total, used, and available space for each filesystem.

How to find the largest files in a directory?
Answer: Use the command du -ah | sort -rh | head -n 10 to list the top 10 largest files and directories.

What is a kernel panic?
Answer: A kernel panic is a safety measure taken by the operating system when it encounters a fatal error from which it cannot safely recover.

How to check the hardware information of a Linux system?
Answer: Use the lshw, lscpu, or lsblk commands to display hardware details about the system.

What is the purpose of the ping command?
Answer: The ping command checks the network connectivity to a host by sending ICMP echo requests and waiting for replies.

How to check the running services on a Linux system?
Answer: Use systemctl list-units --type=service or service --status-all to view running services.

What does the command sudo do?
Answer: The sudo command allows a permitted user to execute a command as the superuser or another user, as specified in the sudoers file.

How to view the contents of a compressed file?
Answer: Use zcat filename.gz for .gz files or tar -tvf archive.tar for .tar files to list their contents without extracting them.

What is a process ID (PID)?
Answer: A process ID (PID) is a unique identifier assigned to each running process in the system.

How to change the priority of a running process?
Answer: Use the renice command followed by the new priority value and the PID of the process to change its priority.

What does the find command do?
Answer: The find command searches for files in a directory hierarchy based on specified criteria such as name, size, or modification date.

What is the function of the ps command?
Answer: The ps command displays information about running processes, including their status, CPU, and memory usage.

How to display the last 10 lines of a file?
Answer: Use the command tail filename to display the last 10 lines of a file.

What is the purpose of the history command?
Answer: The history command displays a list of previously executed commands in the current shell session.

How to list all currently running processes?
Answer: Use the ps aux command to list all currently running processes along with their details.

What does uname -r display?
Answer: The uname -r command displays the current kernel version of the Linux system.

How to display network configuration details?
Answer: Use the ip addr or ifconfig command (if available) to display network configuration and interface details.

What does the kill command do?
Answer: The kill command is used to terminate processes by sending them a signal, usually the SIGTERM signal.

How to check system logs?
Answer: Use the journalctl command or check the /var/log directory for various system log files.

What is a swap partition?
Answer: A swap partition is a designated space on the disk that is used as virtual memory to extend the physical RAM.

How to check the temperature of CPU?
Answer: Use the sensors command (from the lm-sensors package) to check CPU temperature and other hardware monitoring details.

What does tar -cvf do?
Answer: The tar -cvf command creates a new tar archive file, where c stands for create, v for verbose, and f specifies the filename.

How to compress a directory using gzip?
Answer: Use the command tar -czvf archive.tar.gz directory_name to compress a directory into a gzip-compressed tarball.

