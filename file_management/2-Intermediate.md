## Scenario 1
**Task:** You want to rename the file app.log to application.log inside the logs directory. Which command will you run?
**Command:**
```bash
mv logs/app.log logs/application.log
```
---
## Scenario 2
**Task:** You want to view the contents of the file application.log. Which command will you run?
**Command:**
```bash
cat logs/application.log
```
---
## Scenario 3
**Task:** You want to view the contents of application.log page by page (useful if the file is large). Which command will you run?
**Command:**
```bash
less logs/application.log
```
> **Why less:**
> Displays content page by page
> **Allows scrolling:**
> - Space → next page
> - b → previous page
> - /text → search
> - q → quit
---
## Scenario 4
**Task:** You want to view only the first 10 lines of the file application.log. Which command will you run?
**Command:**
```bash
head -n 10 logs/application.log
```
---
## Scenario 5
**Task:** You want to view only the last 10 lines of the file application.log (very common for logs). Which command will you run?
**Command:**
```bash
tail -n 10 logs/application.log
```
---
## Scenario 6
**Task:** You want to continuously monitor the log file application.log in real time as new entries are added. Which command will you run?
**Command:**
```bash
tail -f logs/application.log
```
> **Why tail -f**
> - -f = follow
> - Continuously displays new lines as they are appended
> - Extremely common in production debugging
---
## Scenario 7
**Task:** You want to delete the file application.log from the logs directory. Which command will you run?
**Command:**
```bash
rm logs/application.log
```
---
## Scenario 8
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
