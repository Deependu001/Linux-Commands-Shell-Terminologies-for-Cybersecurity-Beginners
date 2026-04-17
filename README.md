# 🐧 Linux Commands & Shell Terminologies for Cybersecurity Beginners

This cheat sheet collects **essential Linux commands** and **shell concepts** for beginners in cybersecurity.  

---

## 🔑 Navigation & File Management
- `pwd` → Print working directory
- `ls` → List files (`ls -l` for details, `ls -a` for hidden files)
- `cd <dir>` → Change directory
- `touch <file>` → Create empty file
- `cat <file>` → View file contents
- `less <file>` → View file with paging
- `head -n 20 <file>` → Show first 20 lines
- `tail -n 20 <file>` → Show last 20 lines
- `cp <src> <dest>` → Copy file
- `mv <src> <dest>` → Move/rename file
- `rm <file>` → Delete file
- `find / -name <filename>` → Search for files
- `locate <filename>` → Faster file search (requires `updatedb`)
- `tree` → Display directory structure

---

## 🔒 User & Permission Management
- `whoami` → Show current user
- `id` → Show user/group IDs
- `adduser <name>` → Add new user
- `passwd <name>` → Change password
- `groups <user>` → Show group memberships
- `chmod 755 <file>` → Change permissions
- `chown user:group <file>` → Change ownership
- `sudo <command>` → Run command as root
- `su <user>` → Switch user

---

## ⚙️ Process & System Monitoring
- `ps aux` → List running processes
- `top` → Real-time process monitor
- `htop` → Enhanced process monitor
- `kill <PID>` → Terminate process
- `df -h` → Disk usage
- `du -sh <dir>` → Directory size
- `free -h` → Memory usage
- `uptime` → System uptime
- `dmesg | less` → Kernel/system logs
- `journalctl -xe` → Systemd logs

---

## 🌐 Networking & Security Basics
- `ifconfig` or `ip addr` → Show network interfaces
- `ping <host>` → Test connectivity
- `traceroute <host>` → Trace route to host
- `netstat -tulnp` → Show open ports
- `ss -tulnp` → Modern alternative to netstat
- `curl <url>` → Fetch data from URL
- `wget <url>` → Download file
- `scp <src> user@host:/path` → Secure copy between systems
- `rsync -avz <src> <dest>` → Sync files securely
- `ssh user@host` → Remote login
- `ssh-keygen` → Generate SSH keys
- `scp -r <dir> user@host:/path` → Copy directories securely

---

## 🛡️ Cybersecurity Tools
- `nmap <target>` → Network scanning
- `tcpdump -i eth0` → Packet capture
- `wireshark` → GUI packet analysis
- `iptables -L` → Firewall rules
- `ufw enable` → Simple firewall activation
- `grep "pattern" <file>` → Search inside files
- `egrep "regex" <file>` → Extended regex search
- `strings <binary>` → Extract readable text from binaries
- `md5sum <file>` → Generate hash
- `sha256sum <file>` → Stronger hash
- `gpg --encrypt <file>` → Encrypt file
- `openssl enc -aes-256-cbc -in file -out file.enc` → Encrypt with OpenSSL
- `fail2ban` → Intrusion prevention (monitor logs, ban IPs)

---

## 📖 Shell Terminologies
- **Shell** → Interface to interact with OS (bash, zsh)
- **Prompt (`$`)** → Where you type commands
- **Flags/Options** → Modify command behavior (e.g., `ls -l`)
- **Pipe (`|`)** → Send output of one command to another (`cat file | grep text`)
- **Redirect (`>`, `>>`)** → Save output to file (`ls > files.txt`)
- **Environment Variables** → System-wide values (`echo $PATH`)
- **Wildcard (`*`)** → Match multiple files (`ls *.txt`)
- **Background jobs (`&`)** → Run command in background
- **Job control (`fg`, `bg`)** → Manage background jobs
- **History (`history`)** → Show past commands

---

## 🚀 Cybersecurity Workflow Example
```bash
# Reconnaissance
nmap -A target.com

# Check open ports
ss -tulnp

# Monitor traffic
tcpdump -i eth0

# Search logs for suspicious activity
grep "error" /var/log/syslog

# Hash verification
sha256sum suspicious_file
