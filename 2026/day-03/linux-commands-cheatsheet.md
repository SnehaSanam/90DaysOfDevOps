# 🐧 Linux Commands Cheatsheet

## 📂 File & Directory Commands

| Command | Description |
|--------|-------------|
| `ls` | List directory |
| `ls -a` | List with hidden files |
| `ls -l` | Detailed info about files & directories |
| `ls -i` | Display files with inode numbers |
| `ls -t` | Sort files by last modified time |
| `cd` | Change to home directory |
| `cd dir-name` | Change to specific directory |
| `cd ..` | Go one level up |
| `pwd` | Show current working directory |
| `whoami` | Show logged-in user |

---

## 📄 File Operations

| Command | Description |
|--------|-------------|
| `cat file` | Display file content |
| `cat > file` | Create file and write content |
| `cat >> file` | Append content to file |
| `touch file` | Create empty file |
| `cat file1 file2 > file3` | Merge two files |
| `head file` | Show first 10 lines |
| `head -n 5 file` | Show first 5 lines |
| `tail file` | Show last 10 lines |
| `tail -n 5 file` | Show last 5 lines |

---

## 📁 File & Directory Management

| Command | Description |
|--------|-------------|
| `rm file` | Delete file |
| `mkdir dir` | Create directory |
| `mkdir -p /path` | Create nested directories |
| `rm -r dir` | Delete directory |
| `rm -rf dir` | Force delete directory |
| `tree` | Display directory structure |
| `cp file1 file2` | Copy file |
| `mv file1 file2` | Move or rename file |
| `cp -r dir1 dir2` | Copy directory |

---

## 🔐 Permissions & Ownership

| Command | Description |
|--------|-------------|
| `chmod` | Change file permission |
| `chown` | Change file ownership |
| `chgrp` | Change group ownership |

---

## 🔗 Links

| Command | Description |
|--------|-------------|
| `ln -s source link` | Create symbolic link |
| `ln file hardlink` | Create hard link |

---

## 📊 File Analysis

| Command | Description |
|--------|-------------|
| `wc -l file` | Count number of lines |

---

# ⚙️ Process Management

| Command | Description |
|--------|-------------|
| `ps` | Show running processes |
| `ps aux` | Detailed process list |
| `top` | Real-time process monitor |
| `htop` | Interactive process viewer |
| `kill PID` | Kill process |
| `kill -9 PID` | Force kill process |
| `jobs` | Show background jobs |
| `bg` | Resume job in background |
| `fg` | Bring job to foreground |
| `pidof process` | Get process ID |
| `nohup` | Run process after logout |

---

# 💽 Disk Usage

| Command | Description |
|--------|-------------|
| `df` | Show disk free space |
| `df -h` | Human readable disk usage |
| `du` | Directory space usage |
| `du -sh` | Total size of directory |
| `lsblk` | Show block devices |
| `fdisk -l` | Show disk partitions |

**Tip**

```
df → shows free disk space
du → shows which folder uses space
```

---

# 🌐 Networking Commands

| Command | Description |
|--------|-------------|
| `hostname` | Show system hostname |
| `hostname -I` | Show system IP |
| `ifconfig` | Show network interfaces |
| `ip a` | Show IP addresses |
| `ping host` | Test connectivity |
| `traceroute host` | Show network path |
| `netstat` | Show network connections |
| `netstat -tuln` | Show listening ports |
| `dig / nslookup` | DNS lookup |
| `wget` | Download files |
| `curl` | Fetch webpage |
| `ssh` | Remote login |
| `scp` | Secure copy |
| `nmcli` | Manage network |

---

# 👤 User Management

| Command | Description |
|--------|-------------|
| `who` | Logged-in users |
| `w` | User activity |
| `users` | List users |
| `last` | Login history |
| `id` | UID & GID |
| `groupadd group` | Create group |
| `useradd` | Create user |
| `useradd -m` | Create user with home |
| `passwd` | Set password |
| `usermod -aG group user` | Add user to group |
| `userdel` | Delete user |
| `userdel -r` | Delete user with home |

---

# 🔍 Search & Filter

| Command | Description |
|--------|-------------|
| `grep "text" file` | Search text |
| `find /path -name "*.txt"` | Find files |
| `locate file` | Fast file search |
| `sed 's/old/new/' file` | Replace text |
| `awk '{print $1}' file` | Print column |
| `uniq` | Remove duplicates |

---

# ⏰ Scheduling Tasks

## Cron Commands

| Command | Description |
|--------|-------------|
| `crontab -e` | Edit cron jobs |
| `crontab -l` | List cron jobs |
| `crontab -r` | Remove cron jobs |

### Crontab Format

```
* * * * *
| | | | |
| | | | +---- Day of week
| | | +------ Month
| | +-------- Day of month
| +---------- Hour
+------------ Minute
```

---

# 📦 Archive & Compression

| Command | Description |
|--------|-------------|
| `tar -c` | Create archive |
| `tar -x` | Extract archive |
| `tar -v` | Verbose |
| `tar -f` | File name |
| `tar -z` | gzip compression |
| `tar -j` | bzip2 compression |
| `tar -J` | xz compression |

Example

```
tar -czvf archive.tar.gz folder/
tar -xzvf archive.tar.gz
```
