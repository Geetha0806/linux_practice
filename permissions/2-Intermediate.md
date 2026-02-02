## Scenario 1
**Task:** You have a file deploy.sh.
You want to change only the group ownership to ops. Which command will you run?
**Command:**
```bash
chgrp ops deploy.sh
```
> **Why chgrp:**
> - chgrp → changes group ownership only
> - Owner remains unchanged
> - Often used when multiple users need group-level access
---
## Scenario 2
**Task:** You have a directory shared.
You want to change the group ownership of the directory and everything inside it to ops. Which command will you run?
**Command:**
```bash
chgrp -R ops shared
```
---
## Scenario 3
**Task:** You have an executable file backup.sh.
You want it to always run with the owner’s permissions, regardless of who executes it. Which command will you run?
**Command:**
```bash
chmod u+s backup.sh
chmod 4755 backup.sh
```
> ## The Three Special Permissions

| Permission | Octal | Symbolic | Files Effect | Directory Effect |
|------------|-------|----------|--------------|------------------|
| **SUID**   | 4     | `u+s`    | Runs as file **owner** | Ignored |
| **SGID**   | 2     | `g+s`    | Runs as file **group** | New files inherit dir **group** |
| **Sticky** | 1     | `+t`     | Deprecated | Only **owner** can delete files |

---
## Scenario 4
**Task:** You have a directory shared.
You want all new files created inside it to inherit the group ownership of the directory. Which command will you run?
**Command:**
```bash
chmod g+s shared/
chmod 2775 shared/
```
---
## Scenario 5
**Task:** You have a shared directory /shared/tmp.
You want users to delete only their own files, not others’ files. Which command will you run?
**Command:**
```bash
chmod +t /shared/tmp
chmod 1777 /shared/tmp
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
