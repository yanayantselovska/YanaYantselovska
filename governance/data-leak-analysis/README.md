# 🛡️ Data Leak Incident Analysis — NIST SP 800‑53 AC‑6 (Least Privilege)

## 📌 Overview
This project analyzes an internal data exposure incident caused by excessive permissions and improper access management. The goal was to identify the root cause, map the findings to NIST SP 800‑53 AC‑6 (Least Privilege), and recommend improvements to prevent future leaks.

The analysis is based on a real-world scenario involving accidental sharing of internal-only documents with external parties.

---

## 🎯 Objectives
- Identify the factors that contributed to the internal data leak  
- Map the incident to NIST SP 800‑53 AC‑6 (Least Privilege)  
- Recommend improvements to access control and privilege management  
- Demonstrate understanding of governance, risk, and compliance (GRC) principles  

---

## 🛠️ Skills & Frameworks Used
- NIST SP 800‑53 AC‑6 (Least Privilege)  
- Access control analysis  
- Governance & compliance  
- Incident review and documentation  
- Role-based access control (RBAC)  
- Privilege auditing  

---

---

## 🔍 Incident Summary
A sales manager shared access to an internal-only folder containing:

- confidential product documents  
- customer analytics  
- promotional materials not yet approved for release  

The manager **did not revoke access** after the meeting.

Later, a sales representative mistakenly shared the **entire internal folder link** with an external business partner. Believing it was promotional content, the partner posted the link publicly on their company’s social media page.

This resulted in an **unintentional data leak**.

---

## 🧠 Key Issues Identified

### 1. Excessive Permissions
- The entire sales team received access to internal documents they did not need.
- Access was not time-bound and remained active after the meeting.

### 2. Lack of Access Revocation
- The manager failed to remove access after the intended use.
- This violated the principle of least privilege.

### 3. Human Error
- The sales representative shared the wrong link.
- Lack of clear separation between internal and external materials increased risk.

### 4. No Automated Safeguards
- No system prevented external sharing of internal folders.
- No alerts or restrictions were triggered when the link was posted publicly.

---

## 🧩 NIST SP 800‑53 AC‑6 Mapping (Least Privilege)

### **Control Definition**
> Only the minimal access and authorization required to complete a task or function should be provided to users.

### **Discussion**
- Users should not operate with privileges beyond what is necessary.
- Access should be role-based and time-bound.
- Privileges should be regularly reviewed and audited.

### **Relevant Enhancements**
- Restrict access to sensitive resources based on user role  
- Automatically revoke access after a defined period  
- Maintain activity logs for provisioned accounts  
- Conduct regular privilege audits  

### **How AC‑6 Applies to This Incident**
- The sales team had **more access than required**  
- Access was **not revoked** after the meeting  
- No **privilege audits** were performed  
- No **automated controls** prevented external sharing  

---

## 🛠️ Root Cause Analysis

### **Primary Cause**
Excessive and persistent access to internal documents that were not required for the sales team’s job functions.

### **Contributing Factors**
- Lack of RBAC enforcement  
- No time-bound access  
- Human error during link sharing  
- No automated safeguards for sensitive folders  

---

## 🧩 Recommendations (Least Privilege Improvements)

### ✔️ Implement Role-Based Access Control (RBAC)
Only grant access to internal documents to employees whose roles require it.

### ✔️ Enforce Time-Bound Access
Automatically revoke access after:
- meetings  
- projects  
- temporary tasks  

### ✔️ Regular Privilege Audits
Review user permissions monthly or quarterly.

### ✔️ Separate Internal vs. External Materials
Store promotional materials in a **public-safe** folder to avoid confusion.

### ✔️ Enable Sharing Restrictions
Prevent external sharing of internal folders unless explicitly approved.

---

## 🧠 Justification for Recommendations
These improvements strengthen the organization’s security posture by:

- reducing the risk of accidental data exposure  
- ensuring employees only access what they need  
- increasing accountability  
- simplifying privilege tracking  
- aligning with NIST SP 800‑53 AC‑6 requirements  

---

## 📘 What I Learned
- How to map real incidents to NIST controls  
- How least privilege failures lead to data leaks  
- How RBAC and time-bound access reduce human error  
- How governance frameworks guide practical security decisions  

---

## 🏁 Final Result
The incident was traced to excessive permissions and lack of access revocation.  
By applying NIST SP 800‑53 AC‑6 and implementing RBAC, time-bound access, and privilege audits, the organization can significantly reduce the risk of future data leaks.

