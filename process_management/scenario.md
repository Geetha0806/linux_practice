# Scenario 1
**Task:** You want to see all running processes on the system. Which command will you run?
**Command:**
```bash
ps -ef
ps aux
```
---
## Scenario 2
**Task:** You want to check processes related to nginx only. Which command will you run?
**Command:**
```bash
ps -C nginx
ps -ef | grep nginx
```
---
## Scenario 3
**Task:** You want to see process IDs (PIDs) of all running nginx processes only. Which command will you run?
**Command:**
```bash
pgrep nginx
```
---
## Scenario 4
**Task:** You want to see real-time resource usage of processes. Which command will you run?
**Command:**
```bash
top
```
---
## Scenario 5
**Task:** You want to find the PID of a process listening on port 8080. Which command will you run?
**Command:**
```bash
lsof -i 8080
ss -lntp | grep 8080
```
---
## Scenario 6
**Task:** You want to terminate a process with PID 1234 gracefully. Which command will you run?
**Command:**
```bash
kill 1234
```
---
## Scenario 7
**Task:** The process with PID 1234 does not stop with a normal kill.
You want to forcefully terminate it. Which command will you run?
**Command:**
```bash
kill -9 1234
```
---
# Scenario 8
**Task:** You want to kill all running nginx processes at once. Which command will you run?
**Command:**
```bash
pkill -9 nginx
```
---
## Scenario 9
**Task:** You start a long-running script backup.sh and want to run it in the background. Which command will you run?
**Command:**
```bash
./backup.sh &
```
---
## Scenario 10
**Task:** You started a command in the foreground and now want to move it to the background. Which command will you run?
**Command:**
```bash
ctrl + Z
bg
```
---
## Scenario 11
**Task:** You want to see all background and stopped jobs in the current shell. Which command will you run?
**Command:**
```bash
jobs
```
---
## Scenario 12
**Task:** You want to bring job number 1 back to the foreground. Which command will you run?
**Command:**
```bash
fg %1
```
---
## Scenario 13
**Task:** You want to start a script backup.sh with lower CPU priority so it doesn’t impact other processes. Which command will you run?
**Command:**
```bash
nice -n 10 ./backup.sh
```
---
## Scenario 14
**Task:** A process with PID 2345 is consuming high CPU.
You want to lower its priority while it is running. Which command will you run?
**Command:**
```bash
renice -n 5 -p 2345
```
---
# Scenario 15
**Task:** You want to see the hierarchy of all processes (parent–child relationships) on the system. Which command will you run?
**Command:**
```bash
pstree
```
---
## Scenario 16
**Task:** You want to measure how long a script deploy.sh takes to run. Which command will you run?
**Command:**
```bash
time ./deploy.sh 
```
---
## Scenario 17
**Task:** You want to trace system calls made by a running process with PID 5678 to debug it. Which command will you run?
**Command:**
```bash
strace -p 5678
```
---
