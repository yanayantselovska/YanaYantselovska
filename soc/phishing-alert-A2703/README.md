# Phishing Alert Triage — Ticket A‑2703
# 🛡️ Phishing Alert Triage — Malicious Attachment (Ticket A‑2703)

## 📌 Overview
This case study documents the triage of a phishing alert involving a suspicious email containing a known malicious attachment. The goal was to analyze the email, identify indicators of compromise, and determine whether escalation to Tier 2 was required.

The analysis was performed based on the alert details provided in the SOC ticket and the attached evidence.

---

## 🎯 Objectives
- Validate whether the email posed a real security threat  
- Identify phishing indicators in sender details, content, and attachments  
- Verify the attachment hash against known malware  
- Determine appropriate escalation actions  

---

## 🛠️ Tools & Skills Used
- Email header & metadata analysis  
- Phishing indicator identification  
- Hash verification (malware database lookup)  
- SOC triage methodology  
- Incident documentation & escalation reasoning  

---

## 🔍 Incident Summary
**Ticket ID:** A‑2703  
**Alert Message:** SERVER‑MAIL — Phishing attempt, possible malware download  
**Severity:** Medium  
**Status:** Escalated  

The alert indicated that a user may have opened a malicious email and interacted with its contents (attachments or links). Initial review revealed multiple red flags consistent with phishing activity.

---

## 🧠 Key Findings

### 1. **Sender Mismatch**
- Display name: **“Clyde West”**  
- Claimed organization: **“Def Communications”**  
- Actual sender email did **not** match either  
- This is a common phishing tactic to impersonate trusted identities  

### 2. **Grammar & Content Anomalies**
- Subject line and body contained **grammar errors**  
- Poorly written content is a frequent indicator of mass phishing campaigns  

### 3. **Malicious Attachment**
- The attached file’s **hash matched a known malicious sample**  
- This confirmed the attachment was harmful  
- This alone elevates the risk level significantly  

### 4. **Severity vs. Reality**
- Although the alert was marked **Medium**,  
  the combination of:
  - sender mismatch  
  - suspicious content  
  - confirmed malicious attachment  
  justified escalation  

---

## 🧩 Triage Methodology

1. **Reviewed ticket details**  
   - Alert message  
   - Severity  
   - User interaction indicators  

2. **Analyzed sender information**  
   - Compared display name vs. actual email  
   - Checked organization mismatch  

3. **Inspected email content**  
   - Looked for grammar errors  
   - Evaluated tone and intent  

4. **Verified attachment hash**  
   - Compared against known malware databases  
   - Confirmed malicious classification  

5. **Assessed risk & business impact**  
   - User may have opened the attachment  
   - Potential malware execution  

6. **Escalated to Tier 2**  
   - Due to confirmed threat indicators  
   - Required deeper investigation and containment  

---

## 🚨 Escalation Reasoning
The incident was escalated because:

- The attachment was **confirmed malicious**  
- Multiple phishing indicators were present  
- User interaction was possible or likely  
- Medium severity did not reflect actual risk  

Escalation ensured that Tier 2 analysts could perform:

- Endpoint investigation  
- Malware analysis  
- Containment actions  
- User impact assessment  

---

## 📘 What I Learned
- How to validate phishing attempts using structured SOC triage  
- How to identify subtle indicators such as sender mismatch  
- How to verify malicious attachments using hash lookups  
- How to justify escalation decisions with evidence  
- How to document incidents clearly and professionally  

---

## 🏁 Final Result
The alert was **correctly escalated** to Tier 2 due to the presence of a known malicious attachment and multiple phishing indicators. This prevented potential malware execution and supported timely incident response.

---

## 📎 Attached Evidence
- **Alert ticket.pdf** — original SOC alert details  
- Additional screenshots and analysis files located in `/evidence` and `/analysis` folders  


