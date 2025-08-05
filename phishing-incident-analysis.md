# 📂 Phishing Incident Analysis & Response

This case study presents a complete cybersecurity incident workflow conducted as part of the **Google Cybersecurity Certificate** program. It includes:

- Malware analysis using VirusTotal
- Mapping Indicators of Compromise (IoCs) to the Pyramid of Pain
- Completing and escalating a phishing alert ticket

This exercise demonstrates the ability to analyze malicious files, identify threats, and follow playbook procedures for proper response.

---

## 🔺 Pyramid of Pain Analysis

This section summarizes findings from the VirusTotal analysis of a known malicious file hash and maps them to IoCs in the **Pyramid of Pain** framework.

🔗 **Template Link:** [View the full Pyramid of Pain analysis (Google Slides)](https://docs.google.com/presentation/d/100DBHBMbzkYcWo6tNu5lsB9eSsM9snMe71Oxm5WtUEw/edit?usp=sharing)

### 🧪 File Hash Investigated

```plaintext
SHA256: 54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b
```

**Key Findings**

- **Vendor Detections:** 41 security vendors flagged this file as malicious
- **Community Score:** Negative reputation
- **Malware Family:** Often associated with `Trojan.PSW.Agent` and similar variants

### 📊 Indicators of Compromise

| Category | Example IoC | Description |
|----------|-------------|-------------|
| **Hash Value** | `e365ef2ec9441f15...` (SHA1/SHA512 variants) | Used to uniquely identify the malicious file |
| **IP Address** | `20.83.144.107` | Contacted IP during execution (observed in VirusTotal behavior) |
| **Domain Name** | `office365-appsync[.]online` | Malicious domain contacted during payload execution |
| **TTPs** | MITRE ATT&CK `T1059` (Command and Scripting Interpreter) | Used scripting techniques to execute malicious commands |

## 🛡️ Completed Phishing Alert Ticket

The following ticket documents the incident response workflow related to the phishing attack that deployed the file analyzed above.

### 🧾 Alert Ticket Details

| Ticket ID | Alert Message | Severity | Details | Ticket Status |
|-----------|---------------|----------|---------|---------------|
| **A-2703** | SERVER-MAIL Phishing attempt possible download of malware | Medium | The user may have opened a malicious email and opened attachments or clicked links. | Escalated |

### 📝 Ticket Comments

The alert detected that an employee downloaded and opened a malicious file from a phishing email. There was an inconsistency between the sender’s email address (`76tguy6hh6tgftrt7tg.su`), the name used in the email body ("Clyde West"), and the sender’s name, "Def Communications." The email body and subject line also contained grammatical errors.

The email’s body included a password-protected attachment, **bfsvc.exe**, which was downloaded and opened on the affected machine. Having previously investigated the file hash, it is confirmed to be a known malicious file. The alert severity is reported as medium, so the ticket was escalated to a level-two SOC analyst for further action.

### ✉️ Phishing Email Example

```plaintext
From: Def Communications <76tguyhh6tgftrt7tg.su> [114.114.114.114]
Sent: Wednesday, July 20, 2022 09:30:14 AM
To: hr@inergy.com [176.157.125.93]
Subject: Re: Infrastructure Egnieer role

Dear HR at Ingergy,

I am writing for to express my interest in the engineer role posted from the website.

There is attached my resume and cover letter. For privacy, the file is password protected. Use the password paradise10789 to open.

Thank you,
Clyde West
Attachment: bfsvc.exe
```

---

## 📁 Summary

This exercise showcases my ability to:

- Conduct threat analysis using tools like VirusTotal
- Identify and map Indicators of Compromise
- Use incident response playbooks to handle phishing threats
- Document security incidents professionally for escalation or resolution

