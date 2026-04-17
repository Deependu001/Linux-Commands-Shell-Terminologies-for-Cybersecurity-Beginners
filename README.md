# 🐧 Shell Scripting for Cybersecurity Beginners (Linux)

## 📌 Overview
Shell scripting (Bash) is used to automate Linux tasks like system monitoring, log analysis, scanning, and cybersecurity operations.

# ⚙️ Basic Script
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

# 📌 FOR LOOP
for i in 1 2 3 4 5
do
echo "Iteration $i"
done

Output:
Iteration 1
Iteration 2
Iteration 3
Iteration 4
Iteration 5

# 📌 WHILE LOOP
i=1
while [ $i -le 5 ]
do
echo "Count $i"
i=$((i+1))
done

# 📌 FUNCTION
greet() {
echo "Hello $1"
}
greet "Cybersecurity"

Output:
Hello Cybersecurity

# 📌 FILE CHECK
file="test.txt"
if [ -f $file ]
then
echo "File exists"
else
echo "File not found"
fi

# 📌 DIRECTORY CHECK
read dir
if [ -d "$dir" ]
then
ls -la "$dir"
else
echo "Directory not found"
fi

# 📌 LOG ANALYZER
echo "Enter keyword:"
read key
grep "$key" access.log

# 📌 NETWORK INFO
ip a

# 📌 PORT CHECK
ss -tulnp

# 📌 BACKUP SCRIPT
cp -r /home/user/documents /home/user/backup
echo "Backup completed"

# 📌 PROCESS MONITOR
top -b -n 1 | head -n 10

# 📌 ARGUMENTS
echo "First argument: $1"
echo "Second argument: $2"

Run:
./script.sh hacker kali

Output:
First argument: hacker
Second argument: kali

# 📌 EXIT STATUS
ls /root
echo $?

# 🔐 CYBERSECURITY USE CASES
Log monitoring
File integrity checking
Network scanning automation
User tracking
Incident response automation

# 🚀 MINI AUTOMATION SCRIPT
echo "System Scan Started"
who
ss -tulnp
df -h
echo "Scan Complete"

# 🧠 FINAL NOTES
Bash scripting is essential for cybersecurity automation
Use grep awk sed pipes for advanced tasks
Practice daily for Linux and CTF skills