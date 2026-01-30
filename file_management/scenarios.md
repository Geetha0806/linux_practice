# Practice Scenarios for file management commands:

## Scenario 1: Identify Current Location and List Files

### Problem Statement
After logging into a Linux system, you want to:
1. Check your current working directory
2. List all files, including hidden files
3. View file details in long format

---

### ✅ Commands Used

```bash
pwd
ls -a
ls -l
```
---

## Scenario 2: Directory Navigation Using Relative Paths

### Problem Statement
You are currently inside the following directory:
> /home/geetha/project/linux

1. Move one directory up
2. Move two directories up
3. Return to the previous directory

---

### ✅ Commands Used

```bash
cd ..
cd ../..
cd -
```
---
# Scenario 3: Navigating Using Home, Absolute, and Root Paths

## Scenario
You are working on a Linux system and need to quickly move between your home directory, system configuration files, and the root directory.

---

## ✅ Correct Commands

```bash
cd ~
cd /etc
cd ~/Documents
cd /
```
---

# Scenario 4: You are working on a Linux server. Your home directory has the following structure:
```plaintext
/home/geetha/
├── projects/
│   ├── devops/
│   │   ├── scripts/
│   │   │   ├── deploy.sh
│   │   │   └── cleanup.sh
│   │   └── configs/
│   │       ├── app.conf
│   │       └── db.conf
│   └── java/
│       ├── main.java
│       └── utils.java
└── notes/
    ├── linux.md
    └── devops.md
```

## **Scenario:**  
You are in `/home/geetha` and want to:
1. Navigate to `configs` directory inside `devops`
2. List all files with detailed information
3. Return to home directory

## ✅**Correct Commands:**
```bash
# Navigate to configs directory
cd ~/projects/devops/configs

# List all files with details
ls -lh

# Return to home directory
cd
```
---
# Scenario 5: Linux Advanced File Navigation Scenario

**Scenario:**  
You are in `/home/geetha/projects/devops/scripts` and need to:
1. List all `.sh` files in this directory and subdirectories
2. Move one directory up and into `configs` folder using a relative path
3. Find all files in `/home/geetha/projects/java/` containing `main` in their name
4. Return to home directory without typing full path

**Commands:**
```bash
# 1. List all .sh files recursively
find . -type f -name "*.sh"

# 2. Move one directory up and into configs
cd ../configs

# 3. Find files containing 'main' in java folder
find /home/geetha/projects/java/ -type f -name "*main*"

# 4. Return to home directory
cd
```
---
# Scenario 6: You are in /home/geetha/projects/devops/. The structure is:
```plaintext
/home/geetha/projects/devops/
├── scripts/
│   ├── deploy.sh
│   └── cleanup.sh
└── configs/
    ├── app.conf
    └── db.conf
```

**Scenario:**  
You are in `/home/geetha/projects/devops/` and need to:
1. Move `cleanup.sh` from `scripts/` to `configs/`
2. Copy `app.conf` from `configs/` to `scripts/` without removing the original
3. Rename `deploy.sh` to `deploy_v2.sh`
4. Delete `db.conf` from `configs/`
5. Verify all changes

**Commands:**
```bash
# 1. Move cleanup.sh
mv scripts/cleanup.sh configs/

# 2. Copy app.conf
cp configs/app.conf scripts/

# 3. Rename deploy.sh
mv scripts/deploy.sh scripts/deploy_v2.sh

# 4. Delete db.conf
rm configs/db.conf

# 5. Verify changes
ls scripts/
ls configs/
```
---

# Scenario 7: Linux Advanced Navigation & Wildcards Scenario

```plaintext
/home/geetha/projects/
├── devops/
│   ├── scripts/
│   │   ├── deploy_v2.sh
│   │   └── cleanup.sh
│   └── configs/
│       ├── app.conf
├── java/
│   ├── main.java
│   └── utils.java
└── notes/
    ├── linux.md
    └── devops.md
```
**Scenario:**  
You are in `/home/geetha/projects/` and need to:
1. List all `.sh` files in the `devops/` directory recursively
2. Navigate to `java` folder using a relative path, starting from `projects/devops/configs`
3. Go to `notes` folder using only `..` shortcuts
4. List all files starting with `d` in the `projects` directory
5. Return to home directory using the shortest command

**Commands:**
```bash
# 1. List all .sh files recursively
find devops/ -type f -name "*.sh"

# 2. Navigate to java folder from devops/configs
cd ../../java

# 3. Navigate to notes folder using relative path
cd ../notes

# 4. List all files starting with 'd' in projects
find ../ -type f -name "d*"

# 5. Return to home directory
cd
```
---
# Scenario 8: Linux Combined Navigation & File Management Scenario

```plaintext
/home/geetha/projects/
├── devops/
│   ├── scripts/
│   │   ├── deploy_v2.sh
│   │   └── cleanup.sh
│   └── configs/
│       ├── app.conf
├── java/
│   ├── main.java
│   └── utils.java
└── notes/
    ├── linux.md
    └── devops.md

```

**Scenario:**  
You are in `/home/geetha/projects/` and need to:
1. Move all `.sh` files from `devops/scripts/` to `devops/configs/`
2. Copy all `.conf` files from `devops/configs/` to `java/`
3. List all files in `projects` that start with `d` or end with `.md`
4. Navigate to `scripts` from `projects/notes` using relative paths only
5. Return to home directory

**Commands:**
```bash
# 1. Move all .sh files
mv devops/scripts/*.sh devops/configs/

# 2. Copy all .conf files
cp devops/configs/*.conf java/

# 3. List files starting with 'd' or ending with '.md'
find ~/projects/ -type f \( -name "d*" -o -name "*.md" \)

# 4. Navigate to scripts from notes
cd ../devops/scripts

# 5. Return to home directory
cd
```
---

# Scenario 9: Linux Real-World File Navigation Scenario
```plaintext
/home/geetha/projects/
├── devops/
│   ├── scripts/
│   │   ├── deploy_v2.sh
│   │   └── cleanup.sh
│   └── configs/
│       ├── app.conf
├── java/
│   ├── main.java
│   └── utils.java
└── notes/
    ├── linux.md
    └── devops.md
```
**Scenario:**  
You are in `/home/geetha/projects/` and need to:
1. Search for all `.java` files recursively in `projects/`
2. Navigate to `devops/configs/` from anywhere inside `projects`
3. Go to `notes` folder using only `..` navigation
4. List all files containing the letter `e` in `projects/`
5. Return to home directory

**Commands:**
```bash
# 1. Search for all .java files
find projects/ -type f -name "*.java"

# 2. Navigate to devops/configs/ from anywhere inside projects
cd ../devops/configs

# 3. Go to notes folder using relative path
cd ../../notes

# 4. List all files containing 'e'
find projects/ -type f -name "*e*"

# 5. Return to home directory
cd
```
---
# Scenario 10: Linux Combined Navigation, Wildcards & Verification Scenario

```plaintext
/home/geetha/projects/
├── devops/
│   ├── scripts/
│   │   ├── deploy_v2.sh
│   │   └── cleanup.sh
│   └── configs/
│       ├── app.conf
├── java/
│   ├── main.java
│   └── utils.java
└── notes/
    ├── linux.md
    └── devops.md
```

**Scenario:**  
You are in `/home/geetha/projects/` and need to:
1. List all `.sh` files in `devops/` and subdirectories
2. Navigate to `java` folder from `devops/configs` using relative paths
3. Go to `notes` folder using only `..`
4. List all files in `projects/` that start with `d` OR contain `v`
5. Verify contents of `scripts/` for `.sh` files
6. Return to home directory

**Commands:**
```bash
# 1. List all .sh files recursively
find projects/devops/ -type f -name "*.sh"

# 2. Navigate to java from devops/configs
cd ../../java

# 3. Go to notes folder
cd ../notes

# 4. List files starting with 'd' OR containing 'v'
find projects/ -type f \( -name "d*" -o -name "*v*" \)

# 5. Verify .sh files in scripts/
ls ../devops/scripts/*.sh

# 6. Return to home
cd
```
---
# Scenario 11: Linux File & Directory Management Scenario

```plaintext
/home/geetha/projects/
├── devops/
├── java/
└── notes/
```

**Scenario:**  
You are in `/home/geetha/projects/` and need to:
1. Create a directory `test_env`
2. Create two empty files inside it: `test1.txt` and `test2.txt`
3. Copy `test1.txt` to `devops/`
4. Move `test2.txt` to `java/`
5. Delete `test_env` directory along with its contents
6. Verify files in `devops/` and `java/`

**Commands:**
```bash
# 1. Create test_env directory
mkdir test_env

# 2. Create two empty files
touch test_env/test1.txt test_env/test2.txt

# 3. Copy test1.txt to devops
cp -v test_env/test1.txt devops/

# 4. Move test2.txt to java
mv -v test_env/test2.txt java/

# 5. Delete test_env directory
rm -rf test_env/

# 6. Verify files in devops and java
ls devops/ java/
```
---
# Scenario 12: Linux Advanced File & Directory Management Scenario
```plaintext
/home/geetha/projects/
├── devops/
├── java/
└── notes/
```
**Scenario:**  
You are in `/home/geetha/projects/` and need to:
1. Create a directory `batch_files`
2. Inside `batch_files`, create files: file1.txt … file5.txt
3. Copy all `.txt` files to `devops/` using wildcards
4. Move `file3.txt` and `file4.txt` to `java/` using wildcards
5. Delete remaining `.txt` files in `batch_files/`
6. Verify files in `devops/` and `java/`

**Commands:**
```bash
# 1. Create batch_files directory
mkdir -p batch_files

# 2. Create 5 text files
touch batch_files/file{1..5}.txt

# 3. Copy all .txt files to devops/
cp -v batch_files/*.txt devops/

# 4. Move file3.txt and file4.txt to java/
mv batch_files/file{3..4}.txt java/

# 5. Delete remaining .txt files in batch_files/
rm -v batch_files/*.txt

# 6. Verify files in devops/ and java/
ls devops/ java/
```
---
# Scenario 13 – Realistic DevOps File Management
```plaintext
/home/geetha/projects/
├── devops/
├── java/
└── notes/
```

**Scenario:**  
You are in `/home/geetha/projects/` and need to perform a real-world file management task:
1. Create a directory `release_v1`.
2. Inside `release_v1`, create files: `app.log`, `db.log`, `error.log`.
3. Move all `.log` files from `release_v1/` to `devops/`.
4. Copy `.log` files in `devops/` that start with `a` to `java/`.
5. Delete any remaining `.log` files in `release_v1/`.
6. Verify files in `devops/` and `java/`.
7. Delete the `release_v1` directory completely.

**Commands:**
```bash
# 1. Create release_v1 directory
mkdir -p release_v1

# 2. Create log files inside release_v1
cd release_v1
touch {app,db,error}.log

# 3. Move all .log files to devops/
mv {app,db,error}.log ../devops/

# 4. Copy .log files starting with 'a' from devops/ to java/
cp $(find ../devops/ -type f -name "a*") ../java/

# 5. Delete remaining .log files in release_v1/ (if any)
rm -v *.log

# 6. Verify files in devops/ and java/
ls ../devops/ ../java/

# 7. Delete the release_v1 directory completely
cd ..
rm -rf release_v1/
```
---
