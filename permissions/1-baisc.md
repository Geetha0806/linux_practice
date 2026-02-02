## Scenario 1
**Task:** You have a file script.sh in your current directory. You want to make it executable for the owner only. Which command will you run?
**Command:**
```bash
chmod u+x script.sh
```
> **Best Practice / Interview Tip**
> - Use **+** to add permissions
> - Use **-** to remove permissions
> - Use **=** to set exact permissions (overwrites)
> - **u+x** adds the execute permission for the user/owner without removing existing permissions
> - **u=x** would replace all user permissions with only execute, removing read/write if they existed
>     - Usually not desired in scripts
---
## Scenario 2
**Task:** You have a file report.txt.
You want to make it readable and writable for the owner, readable for group and others (common default for text files). Which command will you run?
**Command:**
```bash
chmod 644 report.txt
```
---
## Scenario 3
**Task:** You have a directory scripts.
You want everyone (owner, group, others) to be able to read, write, and enter (execute) this directory. Which command will you run?
**Command:**
```bash
chmod 777 script
```
---
## Scenario 4
**Task:** You want to remove write permission for others on the file report.txt while keeping all other permissions intact. Which command will you run?
**Command:**
```bash
chmod o-w report.txt
```
---
## Scenario 5
**Task:** You have a file deploy.sh.
You want to give execute permission to owner and group, but no permissions to others. Which command will you run?
**Command:**
```bash
chmod ug+x,o= deploy.sh
```
---
## Scenario 6
**Task:** You want to view detailed permissions, owner, and group of all files in the current directory. Which command will you run?
**Command:**
```bash
ls -l
```
> **Why ls -l:**
> - File type (- for file, d for directory)
> - Permissions (rwx for user/group/others)
> - Number of links
> - Owner and group
> - File size and modification date
---
## Scenario 7
**Task:** You want to change the owner of the file deploy.sh to a user named devops. Which command will you run?
**Command:**
```bash
chown devops deploy.sh
```
---
## Scenario 8
**Task:** You want to change both the owner to devops and the group to ops for the file deploy.sh. Which command will you run?
**Command:**
```bash
chown devops:ops deploy.sh
```
---
## Scenario 9
**Task:** You want to change the group of a file deploy.sh to ops without changing the owner. Which command will you run?
**Command:**
```bash
chown :ops deploy.sh
```
---
## Scenario 10
**Task:** You want to recursively change the owner and group of the directory scripts and all its contents to devops:ops. Which command will you run?
**Command:**
```bash
chown -R devops:ops scripts
```
---
## Scenario 5
**Task:** You have a file deploy.sh.
You want to give execute permission to owner and group, but no permissions to others. Which command will you run?
**Command:**
```bash
chmod ug+x,o= deploy.sh
```
---
## Scenario 6
**Task:** You want to view detailed permissions, owner, and group of all files in the current directory. Which command will you run?
**Command:**
```bash
ls -l
```
> **Why ls -l:**
> - File type (- for file, d for directory)
> - Permissions (rwx for user/group/others)
> - Number of links
> - Owner and group
> - File size and modification date
---
## Scenario 7
**Task:** You want to change the owner of the file deploy.sh to a user named devops. Which command will you run?
**Command:**
```bash
chown devops deploy.sh
```
---
