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
**Task:** You want new files to be created with 644 permissions by default. Which command will you run?
**Command:**
```bash
umask 022
```

---
## Scenario 7
**Task:** You want new directories to be created with 750 permissions by default. Which command will you run?
**Command:**
```bash
umask 027
```
---
