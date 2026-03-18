
# 🐧 Linux File Permissions — Authorization & Access Control

## 📌 Overview
This project demonstrates how Linux file and directory permissions can be analyzed and modified to enforce proper authorization. Using core Linux commands, I evaluated existing permissions, identified misconfigurations, and applied changes to ensure users only had the access they were authorized for.

This project highlights practical skills in system administration, access control, and secure configuration management.

---

## 🎯 Objectives
- Inspect file and directory permissions using Linux commands  
- Interpret permission strings and determine authorization levels  
- Modify permissions to remove unauthorized access  
- Apply least‑privilege principles to files and directories  

---

## 🛠️ Skills & Commands Used
- `ls -la` — view detailed file and directory permissions  
- `chmod` — modify user, group, and other permissions  
- Understanding of:
  - read (r), write (w), execute (x)  
  - user / group / other  
  - hidden files  
  - directory execute permissions  

---

## 🔍 Step‑by‑Step Analysis

### 1. **Checked file and directory details**
I used:
ls -la

This returned:
- one directory (`drafts`)
- one hidden file (`.project_x.txt`)
- five project files  
- permission strings for each item

The 10‑character permission string was used to determine:
- file type  
- user permissions  
- group permissions  
- other permissions  

---

### 2. **Described the permission string**
Example:  
`-rw-rw-r--`

Breakdown:
- `-` → regular file  
- `rw-` → user can read/write  
- `rw-` → group can read/write  
- `r--` → others can read only  

This analysis helped identify where permissions did not match organizational requirements.

---

### 3. **Removed unauthorized write access**
The organization required that **others should not have write access** to any files.

I identified `project_k.txt` as having incorrect permissions and used:
chmod o-w project_k.txt

This removed write access for “other.”

---

### 4. **Modified permissions on a hidden file**
The hidden file `.project_x.txt` was archived and should not be modified.

Required:
- user: read only  
- group: read only  
- others: no access  

Commands used:

chmod u-w .project_x.txt
chmod g-w .project_x.txt
chmod g+r .project_x.txt

This ensured the file was readable but not writable.

---

### 5. **Changed directory permissions**
Only the `researcher2` user should access the `drafts` directory.

I removed execute permissions from group and others:


This prevented unauthorized users from entering the directory.

---

## 🧠 Key Takeaways
- Linux permissions directly enforce authorization policies  
- `ls -la` is essential for auditing access  
- `chmod` allows precise control over user, group, and other permissions  
- Hidden files follow the same permission rules  
- Directory execute permissions determine whether a user can *enter* a folder  

---

## 🏁 Final Result
I successfully updated file and directory permissions to match organizational authorization requirements. This project demonstrates practical Linux security skills and the ability to apply least‑privilege principles in a real environment.



