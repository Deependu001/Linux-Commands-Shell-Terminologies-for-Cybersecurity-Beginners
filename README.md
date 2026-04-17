# Shell Scripting for Cybersecurity Beginners (Linux)

## 📌 Overview
Shell scripting is used to automate Linux commands using Bash. It is widely used in cybersecurity for log analysis, system monitoring, automation, scanning, and incident response.

# ⚙️ Basic Shell Script Structure
#!/bin/bash
echo "Hello Cybersecurity World"

Run:
chmod +x script.sh
./script.sh

Output:
Hello Cybersecurity World

# 📌 Variables
#!/bin/bash
name="CyberSec Learner"
echo "Welcome $name"

Output:
Welcome CyberSec Learner

# 📌 User Input
#!/bin/bash
echo "Enter your name:"
read name
echo "Hello $name"

# 📌 IF-ELSE
#!/bin/bash
read num
if [ $num -gt 10 ]
then
echo "Greater than 10"
else
echo "10 or less"
fi

# 📌 Loops
FOR LOOP:
for i in 1 2 3 4 5
do
echo "Iteration $i"
done

WHILE LOOP:
i=1
while [ $i -le 5 ]
do
echo "Count $i"
i=$((i+1))
done

# 📌 Functions
greet() {
echo "Hello $1"
}
greet "Cybersecurity"

# 📌 File Check
file="test.txt"
if [ -f $file ]
then
echo "File exists"
else
echo "File not found"
fi

# 📌 Directory Listing
read dir
if [ -d "$dir" ]
then
ls -la $dir
else
echo "Directory not found"
fi

# 📌 Log Analyzer
echo "Enter keyword:"
read key
grep "$key" access.log

# 📌 Network Info
ip a

# 📌 Port Checking
ss -tulnp

# 📌 Backup Script
cp -r /home/user/documents /home/user/backup
echo "Backup done"

# 📌 Process Monitoring
top -b -n 1 | head -n 10

# 📌 Arguments
echo "First: $1"
echo "Second: $2"

Run:
./script.sh hacker kali

# 📌 Exit Status
ls /root
echo $?

# 🔐 Cybersecurity Use Cases
Log monitoring
File integrity checks
Network scanning automation
User tracking
Incident response automation

# 🚀 Mini Automation Script
echo "System Scan Started"
who
ss -tulnp
df -h
echo "Scan Complete"

# 🧠 Final Notes
Bash scripting is essential in cybersecurity
Use grep, awk, sed, pipes for advanced tasks
Practice daily for Linux + CTF skills