# Scenario 1 – System Information Commands (Linux)

**Scenario:**  
You have logged into a Linux server for the first time. You need to quickly gather
basic system information to understand the environment.

---

## Tasks

1. Identify the current logged-in user  
2. Check the system hostname  
3. Display OS and system details  
4. Check system uptime and load average  
5. View CPU information  
6. Check memory usage  
7. Check disk usage  
8. Verify current date and time  

---

## Correct Commands

```bash
# 1. Check current logged-in user
whoami

# 2. Check hostname
hostname

# 3. Display OS and system information
hostnamectl

# 4. Check uptime and load average
uptime

# 5. Display CPU information
cat /proc/cpuinfo
# quick summary alternative:
# lscpu

# 6. Check memory usage
free -h

# 7. Check disk usage
df -h

# 8. Check current date and time
date
```
---


