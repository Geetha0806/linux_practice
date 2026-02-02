# Scenario 1
**Task:** You want to check the username of the currently logged-in user. Which command will you run?
**Command:**
```bash
whoami
```
---
## Scenario 2
**Task:** You want to check the hostname of the system. Which command will you run?
**Command:**
```bash
hostname
```
---
## Scenario 3
**Task:** You want to check detailed OS information, including name and version. Which command will you run?
**Command:**
```bash
cat /etc/os-release (👉 Best for OS name, version, distro info)
uname -a (👉 Best for kernel and system architecture)
```
---
## Scenario 4
**Task:** You want to check how long the system has been running (uptime and load average). Which command will you run?
**Command:**
```bash
uptime
```
> **Why uptime:**
> **Shows:**
> - How long the system has been running
> - Number of logged-in users
> - Load average (1, 5, 15 minutes)
---
## Scenario 5
**Task:** You want to check CPU-related information such as cores, model, and vendor. Which command will you run?
**Command:**
```bash
lscpu
```
---
## Scenario 6
**Task:** You want to check memory usage in a human-readable format. Which command will you run?
**Command:**
```bash
free -h
```
---
## Scenario 7
**Task:** You want to check disk space usage of all mounted filesystems in a human-readable format. Which command will you run?
**Command:**
```bash
df -h
```
---
# Scenario 8
**Task:** You want to check the current date and time of the system. Which command will you run?
**Command:**
```bash
date
```
---
## Scenario 9
**Task:** You want to see real-time system resource usage (CPU, memory, processes). Which command will you run?
**Command:**
```bash
top
```
---
## Scenario 10
**Task:** You want a more user-friendly and colorful version of top (if installed). Which command will you run?
**Command:**
```bash
htop
```
---
## Scenario 11
**Task:** You want to check the Linux distribution name and version (for example Ubuntu 22.04). Which command will you run?
**Command:**
```bash
cat /etc/os-release
lsb_release -a
```
> **Interview Clarity:**
> - “What Linux distro is this?” → lsb_release -a
> - “What OS details are available?” → /etc/os-release
---
## Scenario 12
**Task:** You want to check the system architecture (32-bit or 64-bit). Which command will you run?
**Command:**
```bash
uname -m
arch
```
---
## Scenario 13
**Task:** You want to list all block devices (disks, partitions, and mount points). Which command will you run?
**Command:**
```bash
lsblk
```
> **Why lsblk**
> Lists:
> - Disks
> - Partitions
> - Mount points
> Very useful in cloud, VM, and storage troubleshooting
---
## Scenario 14
**Task:** You want to check all currently mounted filesystems. Which command will you run?
**Command:**
```bash
mount
```
---
# Scenario 15
**Task:** You want a clean, tree-style view of mounted filesystems. Which command will you run?
**Command:**
```bash
findmnt
```
---
## Scenario 16
**Task:** You want to get a quick summary of system performance including CPU, memory, and process stats (without real-time refresh). Which command will you run?
**Command:**
```bash
vmstat
```
> **Why vmstat**
> Provides a snapshot of:
> - CPU usage
> - Memory usage
> - Process and IO stats
> - Lightweight and fast
---
## Scenario 17
**Task:** You want to check detailed OS information, including name and version. Which command will you run?
**Command:**
```bash
cat /etc/os-release (👉 Best for OS name, version, distro info)
uname -a (👉 Best for kernel and system architecture)
```
---
## Scenario 18
**Task:** You want to run df -h every 2 seconds automatically to monitor disk usage changes. Which command will you run?
**Command:**
```bash
watch df -h
```
---
## Scenario 19
**Task:** You want to monitor disk usage every 5 seconds. Which command will you run?
**Command:**
```bash
watch -n 5 df -h
```
---
## Scenario 20
**Task:** You want to watch memory usage with changes highlighted. Which command will you run?
**Command:**
```bash
watch -d free -h
```
---
## Scenario 21
**Task:** You want to monitor running processes (color + differences). Which command will you run?
**Command:**
```bash
watch -d -c 'ps aux | head -10'
```
---
## Scenario 22
**Task:** You want to Watch log file tail (every 3 seconds). Which command will you run?
**Command:**
```bash
watch -n 3 'tail -5 /var/log/syslog'
```
---
## Scenario 23
**Task:** You want to Exit when network connections change. Which command will you run?
**Command:**
```bash
watch -g netstat -tuln
```
---
## Scenario 24
**Task:** You want to monitor running processes (color + differences). Which command will you run?
**Command:**
```bash
watch -d -c 'ps aux | head -10'
```
---
