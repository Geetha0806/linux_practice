## Scenario 1
**Task:** You want to delete the file application.log from the logs directory. Which command will you run?
**Command:**
```bash
rm logs/application.log
```
---
## Scenario 2
**Task:** You want to delete the entire logs directory and everything inside it. Which command will you run?
**Command:**
```bash
rm -rf logs/
```
> **Why rm -rf**
> - -r → recursive (deletes directory and its contents)
>- -f → force (no confirmation prompts)
> Common in cleanup scripts and automation
---
## Scenario 3
**Task:** You want to create a directory structure app/config/nginx in one command, even if the parent directories don’t exist. Which command will you run?
**Command:**
```bash
mkdir -p app/config/nginx
```
---
## Scenario 4
**Task:** You want to list only files and directories inside the logs directory (not recursive). Which command will you run?
**Command:**
```bash
ls logs/
```
---
## Scenario 5
**Task:** You want to create a file named app.log inside the logs directory. Which command will you run?
**Command:**
```bash
touch logs/app.log
```
---
## Scenario 6
**Task:** You want to copy the file app.log to a new file named app_backup.log in the same directory. Which command will you run?
**Command:**
```bash
cp logs/app.log logs/app_backup.log
```
---
## Scenario 7
**Task:** You want to move the file app_backup.log from logs to the app directory. Which command will you run?
**Command:**
```bash
mv logs/app_backup.log app/
```
---
