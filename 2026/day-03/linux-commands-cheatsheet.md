# Linux Command Cheatsheet

## File & Directory Commands

  Command         Description
  --------------- -----------------------------------------
  `ls`            List directory
  `ls -a`         List with hidden files
  `ls -l`         Detailed info about files & directories
  `ls -i`         Display files with inode numbers
  `ls -t`         Sort files by last modified time
  `cd`            Change to home directory
  `cd dir-name`   Change to specific directory
  `cd ..`         Go one level up
  `pwd`           Show current working directory
  `whoami`        Show current logged-in user

## File Operations

  Command                     Description
  --------------------------- -------------------------------
  `cat file`                  Display file content
  `cat > file`                Create file and write content
  `cat >> file`               Append content to file
  `touch file`                Create empty file
  `cat file1 file2 > file3`   Merge files
  `head file`                 Show first 10 lines
  `head -n 5 file`            Show first 5 lines
  `tail file`                 Show last 10 lines
  `tail -n 5 file`            Show last 5 lines

## File & Directory Management

  Command             Description
  ------------------- ---------------------------
  `rm file`           Delete file
  `mkdir dir`         Create directory
  `mkdir -p path`     Create nested directories
  `rm -r dir`         Remove directory
  `rm -rf dir`        Force remove directory
  `cp file1 file2`    Copy file
  `mv file1 file2`    Move or rename file
  `cp -r dir1 dir2`   Copy directory
  `tree`              Show directory structure

## Permissions

  Command   Description
  --------- ------------------------
  `chmod`   Change file permission
  `chown`   Change file ownership
  `chgrp`   Change group ownership

## Links

  Command               Description
  --------------------- ----------------------
  `ln -s source link`   Create symbolic link
  `ln file hardlink`    Create hard link

## File Analysis

  Command        Description
  -------------- ---------------------
  `wc -l file`   Count lines in file

## Process Management

  Command           Description
  ----------------- -----------------------------
  `ps`              Show running processes
  `ps aux`          Detailed process list
  `top`             Real-time process view
  `htop`            Interactive process monitor
  `kill PID`        Kill process
  `kill -9 PID`     Force kill process
  `jobs`            Show background jobs
  `bg`              Resume job in background
  `fg`              Bring job to foreground
  `pidof process`   Get PID of process
  `nohup`           Run process after logout

## System Info

  Command      Description
  ------------ ---------------------
  `uptime`     System running time
  `uname`      Kernel name
  `uname -r`   Kernel version
  `uname -a`   Full system info
  `date`       Show date & time
  `cal`        Show calendar

## Disk Usage

  Command      Description
  ------------ ---------------------------
  `df`         Disk free space
  `df -h`      Disk usage human readable
  `du`         Directory size
  `du -sh`     Total size of directory
  `lsblk`      Show block devices
  `fdisk -l`   Show disk partitions

**Tip:**\
- `df` → Shows **free disk space**\
- `du` → Shows **which folder uses space**

## Networking Commands

  Command             Description
  ------------------- ----------------------------
  `hostname`          Show system hostname
  `hostname -I`       Show IP address
  `ifconfig`          Show network interfaces
  `ip a`              Show IP addresses
  `ping host`         Test connectivity
  `traceroute host`   Show network path
  `netstat`           Show network connections
  `netstat -tuln`     Show listening ports
  `dig / nslookup`    DNS lookup
  `wget`              Download files
  `curl`              Get webpage source
  `ssh`               Remote login
  `scp`               Secure file copy
  `nmcli`             Manage network connections

## User Management

  Command                    Description
  -------------------------- ---------------------------------
  `who`                      Show logged-in users
  `w`                        Show user activity
  `users`                    List users
  `last`                     Show login history
  `id`                       Show UID & GID
  `groupadd group`           Create group
  `useradd`                  Create user
  `useradd -m`               Create user with home dir
  `passwd`                   Set password
  `usermod -aG group user`   Add user to group
  `userdel`                  Delete user
  `userdel -r`               Delete user with home directory

## Search & Filter

  Command                      Description
  ---------------------------- ------------------------
  `grep "text" file`           Search text
  `find /path -name "*.txt"`   Find files
  `locate file`                Search file quickly
  `sed 's/old/new/' file`      Replace text
  `awk '{print $1}' file`      Print column
  `uniq`                       Remove duplicate lines

## Scheduling Tasks

### Cron

Cron runs scheduled jobs defined in crontab.

  Command        Description
  -------------- ------------------
  `crontab -e`   Edit cron jobs
  `crontab -l`   List cron jobs
  `crontab -r`   Remove cron jobs

### Crontab Time Format

    * * * * *
    | | | | |
    | | | | +---- Day of week (0-7)
    | | | +------ Month (1-12)
    | | +-------- Day of month (1-31)
    | +---------- Hour (0-23)
    +------------ Minute (0-59)

## Archive & Compression (tar)

  Command    Description
  ---------- -------------------
  `tar -c`   Create archive
  `tar -x`   Extract archive
  `tar -v`   Verbose
  `tar -f`   File name
  `tar -z`   gzip compression
  `tar -j`   bzip2 compression
  `tar -J`   xz compression

Example:

    tar -czvf archive.tar.gz folder/
    tar -xzvf archive.tar.gz
