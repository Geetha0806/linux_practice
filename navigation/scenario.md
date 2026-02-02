## Scenario 1
**Task:** You want to check your current working directory. Which command will you run?

**Command:**
```bash
pwd
```
---
## Scenario 2
**Task:** You want to move to your home directory from anywhere. Which command will you run?

**Command:**
```bash
cd
```
---
## Scenario 3
**Task:** You want to move to the root directory of the filesystem. Which command will you run?

**Command:**
```bash
cd /
```
---
## Scenario 4
**Task:** You are in /var/log/nginx and want to move one directory up to /var/log. Which command will you run?

**Command:**
```bash
cd ..
```
---
## Scenario 5
**Task:** You are in /etc/nginx/sites-available and want to move directly to /var/www/html. Which command will you run?

**Command:**
```bash
cd /var/www/html
```
---
## Scenario 6
**Task:** You moved to another directory and now want to return to the previous directory. Which command will you run?

**Command:**
```bash
cd -
```
---
## Scenario 7
**Task:** You are in /home/user/projects and want to move to logs inside this directory. Which command will you run?

**Command:**
```bash
cd logs/
```
---
## Scenario 8
**Task:** You are in /var/log and want to jump to /home/user using a relative path. Which command will you run?

**Command:**
```bash
cd ../../home/user
```
---
## Scenario 9
**Task:** You are in /home/user/projects/app/config and want to jump directly to /home/user/projects using a relative path. Which command will you run?

**Command:**
```bash
cd ../..
```
---
## Scenario 10
**Task:** You want to find a file named config.yml in the current directory and all its subdirectories. Which command will you run?

**Command:**
```bash
find . -name config.yml
```
---
## Scenario 11
**Task:** You want to find all .log files inside /var/log. Which command will you run?

**Command:**
```bash
find /var/log -name "*.log"
```
---
## Scenario 12
**Task:** You want to find directories named nginx anywhere under /etc. Which command will you run?

**Command:**
```bash
find /etc -type d -name nginx
```
---
## Scenario 13
**Task:** You want to find a file named deploy.sh anywhere on the system. Which command will you run?

**Command:**
```bash
find / -name deploy.sh
```
---
## Scenario 14
**Task:** You want to find all files larger than 100 MB in /var. Which command will you run?

**Command:**
```bash
find /var -size +100M
```
---
## Scenario 15
**Task:** You want to find all .sh files in the current directory and subdirectories and list them with detailed permissions. Which command will you run?

**Command:**
```bash
find . -name "*.sh" -exec ls -l {} \;
```
## Why Each Component Matters

| Component     | Why We Need It             | Without It                        |
|---------------|----------------------------|-----------------------------------|
| `.`           | Tells WHERE to search      | `find` uses current dir by default, but explicit is clearer |
| `-name "*.sh"`| **FILTER**: Only shell scripts | Gets ALL files (too much noise!) |
| `-exec`       | **ACTION**: Do something with results | Just lists paths (boring)     |
| `ls -l`       | **DETAIL**: Rich info view | Plain filenames only             |
| `{}`          | **REPLACE**: Insert filename | `ls -l` gets literal "{}"       |
| `\;`          | **END**: Command terminator | Syntax error!                    |

---
## Scenario 16
**Task:** You want to find all files in /var/log that were modified in the last 7 days. Which command will you run?

**Command:**
```bash
find /var/log -mtime -7 -type f
```
---
## Scenario 17
**Task:** You want to find all files in the current directory that are writable by others. Which command will you run?

**Command:**
```bash
find . -perm /o=w
```
---
## Scenario 18
**Task:** You want to find all .log files in /var/log larger than 50 MB and suppress permission errors. Which command will you run?

**Command:**
```bash
find /var/log -name "*.log" -size +50M 2>/dev/null 
```
## Why Each Part is Essential

| Component       | Purpose                    | Without It                  |
|-----------------|----------------------------|-----------------------------|
| `/var/log`      | Target log directory       | Searches everywhere (slow!) |
| `-name "*.log"` | **FILTER**: Log files only | Finds ALL large files       |
| `-size +50M`    | **SIZE**: >50MB files      | No size restriction         |
| `2>/dev/null`   | **QUIET**: Hide "Permission denied" | Noisy error spam      |

---
## Scenario 19
**Task:** You want to find all .sh files modified in the last 3 days in /home/user/projects and list them with detailed info. Which command will you run?

**Command:**
```bash
find /home/user/projects -name "*.sh" -mtime -3 -exec ls -l {} \;
```
---
