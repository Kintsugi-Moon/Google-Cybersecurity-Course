# 🛡️ Parking Lot USB Exercise

**Course**: Google Cybersecurity Certificate
**Module**: Device and Media Controls
**Scenario**: Investigating a potentially malicious USB drive found at Rhetorical Hospital

## 🗂️ Contents

The USB drive contains both personal and work-related files, such as family and pet photos, a new hire letter, and an employee shift schedule. These documents may contain sensitive personally identifiable information (PII) and operational details related to HR and hospital staffing.

## 🧠 Attacker Mindset

An attacker could use this information to impersonate coworkers or family members in phishing attempts. Knowledge of shift schedules and HR communications could help craft convincing social engineering attacks targeting Jorge or other hospital staff. These details can be exploited to gain trust and facilitate further compromise of hospital systems.

## 🔍 Risk Analysis

USB baiting attacks can deliver various forms of malware, such as keyloggers, ransomware, or backdoors. If an infected USB was discovered and connected by an unsuspecting employee, it could compromise the hospital's network. Sensitive information on the drive could also be leveraged in social engineering attacks. To mitigate these risks:

* **Technical Controls**: Disable AutoRun/AutoPlay on all devices to prevent automatic execution of malicious code.
* **Operational Controls**: Use antivirus and endpoint detection in isolated virtual environments to investigate unknown devices safely.
* **Managerial Controls**: Provide regular training on physical security and policies that prohibit plugging unknown USB drives into workstations.

## 📝 Lessons Learned

Even without malware, misplaced devices containing sensitive data can create attack opportunities. Recognizing and mitigating these risks using layered security controls is crucial in maintaining operational security in healthcare and other sensitive industries.

