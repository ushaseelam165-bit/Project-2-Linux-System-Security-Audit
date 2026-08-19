# Project 2 - Linux System Security Audit

## 📌 Project Overview

This project performs a basic security audit of an Ubuntu Linux
environment using standard Linux commands. The audit covers system
information, file-system navigation, users and groups, file permissions,
process monitoring, log analysis, SUID files, and basic system-resource
troubleshooting.

## 🎯 Objective

The main objective is to understand and demonstrate basic Linux system
administration and security auditing concepts through practical terminal
commands.

## 🖥️ Environment

-   **Operating System:** Ubuntu 24.04.4 LTS
-   **Codename:** Noble Numbat
-   **Environment:** Windows Subsystem for Linux 2 (WSL2)
-   **Architecture:** x86-64
-   **Kernel:** Linux 6.18.33.2-microsoft-standard-WSL2
-   **Python:** 3.12.3
-   **User:** student

## 🛠️ Commands Used

### 1. System Information

``` bash
hostname
hostnamectl
uname -a
cat /etc/os-release
```

### 2. File System Navigation

``` bash
pwd
ls
ls -la
cd /home
cd /etc
cd /var/log
```

### 3. Users and Groups

``` bash
whoami
id
cat /etc/passwd
groups
```

### 4. File Permissions

``` bash
touch project.txt
ls -l project.txt
chmod 755 project.txt
ls -l project.txt
chmod 644 project.txt
ls -l project.txt
```

### 5. Process Monitoring

``` bash
ps aux
top
```

### 6. Log Analysis

``` bash
cd /var/log
ls
cat /var/log/auth.log
journalctl
```

### 7. Security Audit

``` bash
find / -perm -4000 2>/dev/null
```

This command identifies files with the SUID permission bit. SUID files
can run with the permissions of their owner, so unexpected or
unnecessary SUID files should be reviewed carefully.

### 8. Basic Troubleshooting

``` bash
df -h
free -h
du -sh /home
```

## 🔍 Key Observations

-   The system was identified as **Ubuntu 24.04.4 LTS** running under
    **WSL2**.
-   The current user was verified as **student** with UID 1000 and GID
    1000.
-   The `/etc/passwd` file was inspected to review local system and
    service accounts.
-   File permissions for `project.txt` were changed from **755** to
    **644** and verified using `ls -l`.
-   Running processes and CPU/memory information were examined using
    `ps aux` and `top`.
-   System and authentication logs were inspected under `/var/log`.
-   SUID files were identified using the `find` command.
-   Disk usage, memory usage, and `/home` directory usage were checked
    using `df`, `free`, and `du`.

## 🔐 Security Recommendations

-   Follow the principle of least privilege.
-   Keep the Ubuntu system and packages updated.
-   Review unnecessary user accounts and login shells.
-   Monitor authentication and system logs regularly.
-   Review SUID files and keep only those required by the operating
    system or installed software.
-   Avoid unnecessarily permissive file permissions for sensitive files.
-   Use strong passwords and do not share authentication credentials.

## 📸 Screenshots

Screenshots of the terminal outputs are included with the project
submission as required.

Recommended screenshot topics:

1.  System information
2.  File-system navigation
3.  User and group information
4.  File permissions
5.  Process monitoring
6.  Log analysis
7.  SUID file search
8.  Basic troubleshooting

## 📄 Project Report

The complete Linux System Security Audit report contains:

-   Introduction
-   Objectives
-   System environment
-   Commands used
-   Audit observations
-   Security recommendations
-   Challenges faced
-   Conclusion
-   Supporting screenshots

## 📚 Learning Outcomes

After completing this project, the following Linux skills were
practiced:

-   Linux terminal navigation
-   System information gathering
-   User and group management
-   File permissions
-   Process monitoring
-   Log analysis
-   Basic security auditing
-   System-resource troubleshooting
-   GitHub project publishing

## 👩‍💻 Author

**Usha**

## 📌 Repository

Repository name:

`Project-2-Linux-System-Security-Audit`
