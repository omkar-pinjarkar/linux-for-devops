# Linux for DevOps – Part 2: Files, Directories & Permissions

## Introduction
In DevOps, permission issues are one of the most common causes of failures.
Understanding Linux files and permissions is critical for working with servers.

---

## Linux File Types
- Regular file (-)
- Directory (d)
- Symbolic link (l)

---

## File & Directory Commands
```bash
touch file.txt
mkdir mydir
rm file.txt
cp source.txt dest.txt
mv old.txt new.txt
```
## Linux Permissions Explained

## Each file has:
Owner
Group
Others

## Permissions:

r – read
w – write
x – execute

### Example:
```
-rwxr-xr--
```
### chmod – Change Permissions
```
chmod 755 script.sh
chmod u+x script.sh
```
### chown – Change Ownership
```
chown user:group file.txt
```

### Real DevOps Example

Problem:
Jenkins cannot execute a shell script.

Solution:
```
chmod +x deploy.sh
chown jenkins:jenkins deploy.sh
```
