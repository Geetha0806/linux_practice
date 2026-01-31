# Scenario 1 – File Permissions

**Scenario:**  
You are in `/home/geetha/projects/devops/` and need to manage permissions for the script `deploy_v2.sh`.

**Tasks:**  
1. Check the current permissions of `deploy_v2.sh`.  
2. Make `deploy_v2.sh` executable by the owner only.  
3. Allow **read and execute** permissions for the group, no write.  
4. Remove **all permissions for others**.  
5. Verify the changes.

**Correct Commands:**
```bash
# 1. Check current permissions
ls -l deploy_v2.sh

# 2. Make the file executable by the owner only
chmod u+x deploy_v2.sh

# 3. Allow read & execute for group, no write
chmod g=rx deploy_v2.sh

# 4. Remove all permissions for others
chmod o= deploy_v2.sh

# Alternatively, combine numeric mode
chmod 750 deploy_v2.sh

# 5. Verify changes
ls -l deploy_v2.sh
```
---
# Scenario 2 – Changing Ownership and Group Permissions

**Scenario:**  
You are in `/home/geetha/projects/devops/`. The file `deploy_v2.sh` belongs to user `geetha` and group `devops`. You need to modify ownership and group permissions.

**Tasks:**
1. Verify current owner and group.  
2. Change owner to `root`.  
3. Change group to `admins`.  
4. Change both owner and group to `geetha:admins`.  
5. Verify the changes.

**Correct Commands:**
```bash
# 1. Verify owner and group
ls -l deploy_v2.sh

# 2. Change owner to root
sudo chown root deploy_v2.sh

# 3. Change group to admins
sudo chown :admins deploy_v2.sh
# or
sudo chgrp admins deploy_v2.sh

# 4. Change both owner and group to geetha:admins
sudo chown geetha:admins deploy_v2.sh

# 5. Verify changes
ls -l deploy_v2.sh
```
---
# Scenario 3 – Combined Permissions & Ownership for Scripts

**Scenario:**  
You are in `/home/geetha/projects/devops/`. The `scripts/` directory contains the following files:
deploy.sh
cleanup.sh
monitor.sh

You need to prepare these scripts for deployment by setting proper permissions and ownership.

**Tasks:**
1. Verify permissions and ownership of all files.  
2. Make all scripts executable by the owner only.  
3. Give read & execute permissions to the group.  
4. Remove all permissions for others.  
5. Change owner to `geetha` and group to `admins`.  
6. Verify permissions and ownership.

**Correct Commands:**
```bash
# 1. Verify current permissions and ownership
ls -l scripts/

# 2. Set permissions: owner=rwx, group=rx, others=none
chmod 750 scripts/*.sh
# symbolic alternative:
chmod u+x,g=rx,o= scripts/*.sh

# 5. Change owner and group
chown geetha:admins scripts/*.sh

# 6. Verify changes
ls -l scripts/
```
---
# Scenario 5 – Special Permissions (SUID, SGID, Sticky Bit)

**Scenario:**  
You are in `/home/geetha/projects/`. The directory `shared_tools/` is shared across multiple users.
```plaintext
shared_tools/
├── deploy.sh
├── cleanup.sh
└── monitor.sh
```
You must configure special permissions securely.
---

## Tasks

1. Verify permissions of directory and files  
2. Set **SUID** on `deploy.sh`  
3. Set **SGID** on `shared_tools/`  
4. Set **Sticky Bit** on `shared_tools/`  
5. Verify special permissions  

---

## Correct Commands

```bash
# 1. Verify current permissions
ls -l shared_tools/
ls -ld shared_tools/

# 2. Set SUID on deploy.sh
chmod u+s shared_tools/deploy.sh
# numeric alternative:
# chmod 4750 shared_tools/deploy.sh

# 3. Set SGID on the directory
chmod g+s shared_tools/
# numeric alternative:
# chmod 2750 shared_tools/

# 4. Set Sticky Bit on the directory
chmod +t shared_tools/
# numeric alternative:
# chmod 1750 shared_tools/

# 5. Verify special permissions
ls -l shared_tools/
ls -ld shared_tools/
```
---

# Scenario 6 – umask & Default File Permissions

**Scenario:**  
You are working on a Linux system and notice that:
- Newly created files have permission `644`
- Newly created directories have permission `755`

You need to understand and control **default permissions** using `umask`.

---

## Tasks

1. Check the current `umask` value  
2. Create a file and directory to observe default permissions  
3. Explain how default permissions are calculated  
4. Change the `umask` so that:
   - New files get `640`
   - New directories get `750`
5. Verify the new default permissions  
6. Reset `umask` to the previous value  

---

## Correct Commands

```bash
# 1. Check current umask
umask

# 2. Create a file and directory to observe defaults
touch testfile.txt
mkdir testdir

# 3. Verify permissions
ls -l testfile.txt
ls -ld testdir

# 4. Change umask to restrict permissions
umask 027

# 5. Create new file and directory with new umask
touch securefile.txt
mkdir securedir

# 6. Verify new permissions
ls -l securefile.txt
ls -ld securedir

# 7. Reset umask (example: default 022)
umask 022
```
---

