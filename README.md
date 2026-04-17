# 🐧 Linux Commands & Shell Terminologies for Cybersecurity Beginners

## 🔑 Navigation & File Management
- `pwd` → Print working directory
- `ls` → List files (`ls -l` for details, `ls -a` for hidden files)
- `cd <dir>` → Change directory
- `touch <file>` → Create empty file
- `cat <file>` → View file contents
- `head -n 20 <file>` → Show first 20 lines
- `tail -n 20 <file>` → Show last 20 lines
- `cp <src> <dest>` → Copy file
- `mv <src> <dest>` → Move/rename file
- `rm <file>` → Delete file
- `find / -name <filename>` → Search for files

## 🔒 User & Permission Management
- `whoami` → Show current user
- `id` → Show user/group IDs
- `adduser <name>` → Add new user
- `passwd <name>` → Change password
- `chmod 755 <file>` → Change permissions
- `chown user:group <file>` → Change ownership
- `sudo <command>` → Run command as root

## ⚙️ Process & System Monitoring
- `ps aux` → List running processes
- `top` → Real-time process monitor
- `kill <PID>` → Terminate process
- `df -h` → Disk usage
- `du -sh <dir>` → Directory size
- `free -h` → Memory usage
- `uptime` → System uptime

## 🌐 Networking & Security Basics
- `ifconfig` or `ip addr` → Show network interfaces
- `ping <host>` → Test connectivity
- `netstat -tulnp` → Show open ports
- `ss -tulnp` → Modern alternative to netstat
- `curl <url>` → Fetch data from URL
- `wget <url>` → Download file
- `scp <src> user@host:/path` → Secure copy between systems
- `ssh user@host` → Remote login

## 🛡️ Cybersecurity Tools
- `nmap <target>` → Network scanning
- `tcpdump -i eth0` → Packet capture
- `iptables -L` → Firewall rules
- `ufw enable` → Simple firewall activation
- `grep "pattern" <file>` → Search inside files
- `strings <binary>` → Extract readable text from binaries
- `md5sum <file>` → Generate hash
- `gpg --encrypt <file>` → Encrypt file

## 📖 Shell Terminologies
- **Shell** → Interface to interact with OS (bash, zsh)
- **Prompt (`$`)** → Where you type commands
- **Flags/Options** → Modify command behavior (e.g., `ls -l`)
- **Pipe (`|`)** → Send output of one command to another (`cat file | grep text`)
- **Redirect (`>`, `>>`)** → Save output to file (`ls > files.txt`)
- **Environment Variables** → System-wide values (`echo $PATH`)
- **Wildcard (`*`)** → Match multiple files (`ls *.txt`)

## 🚀 Cybersecurity Workflow Example
```bash
# Reconnaissance
nmap -A target.com

# Check open ports
ss -tulnp

# Monitor traffic
tcpdump -i eth0

# Search logs
grep "error" /var/log/syslog
