# 🐍 Algorithm for File Updates in Python — Access Control Automation

## 📌 Overview
This project demonstrates how Python can be used to manage and update an allowlist of authorized IP addresses. The file **allow_list.txt** contains IPs that are permitted to access restricted content. A separate list, `remove_list`, contains IPs that should no longer have access.

The algorithm reads the allow list, removes unauthorized IPs, and writes the updated list back to the file. This type of automation is commonly used in cybersecurity workflows such as access control, firewall rule updates, and allowlist/blocklist maintenance.

---

## 🎯 Objectives
- Read and parse a text file containing authorized IP addresses  
- Convert file contents into a list for easier processing  
- Iterate through a list of IPs to remove unauthorized entries  
- Overwrite the file with the updated allowlist  
- Demonstrate safe and efficient Python file handling  

---

## 🛠️ Skills & Python Concepts Demonstrated
- File handling with `open()`  
- Safe file operations using `with` statements  
- Reading file contents using `.read()`  
- Converting strings to lists using `.split()`  
- Iterating through lists with `for` loops  
- Conditional logic to identify unauthorized IPs  
- Removing items from a list using `.remove()`  
- Converting lists back to strings using `.join()`  
- Writing updated content back to a file with `.write()`  

---

## 🔍 Step-by-Step Process

### 1. **Open the allow list file**
I assigned the filename to a variable and used a `with open(..., "r")` block to safely read the file.  
This ensures the file closes automatically after reading.

### 2. **Read the file contents**
Using `.read()`, I loaded the entire file into a string and stored it in `ip_addresses`.

### 3. **Convert the string into a list**
I used `.split()` to break the string into a list of individual IP addresses.  
This makes it easier to iterate and modify the data.

### 4. **Iterate through the remove list**
I looped through the list of IPs and checked whether each one appears in `remove_list`.

### 5. **Remove unauthorized IP addresses**
Inside the loop, I used:
This removes any IP that should no longer have access.

# File that contains the allow list
import_file = "allow_list.txt"

# List of IPs that should be removed
remove_list = ["192.168.1.10", "10.0.0.5"]

# --- Read the file and convert contents to a list ---
with open(import_file, "r") as file:
    ip_addresses = file.read().split()

# --- Remove IPs that appear in remove_list ---
for element in remove_list:
    if element in ip_addresses:
        ip_addresses.remove(element)

# --- Convert list back to string and write updated data ---
updated_ips = "\n".join(ip_addresses)

with open(import_file, "w") as file:
    file.write(updated_ips)
