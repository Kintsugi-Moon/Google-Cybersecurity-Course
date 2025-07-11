# 🛡️ Incident Response Review: E-Commerce Data Breach Case

## 🔍 Scenario Overview

As part of my role as a Level 1 SOC Analyst at a retail company, I reviewed the final report of a significant security incident that occurred prior to my employment. This activity supports the **Post-Incident Review** phase of the [NIST Incident Response Lifecycle](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-61r2.pdf), focusing on lessons learned and strengthening defenses against future threats.

---

## 📌 Executive Summary

- **Date of Incident**: December 28, 2022, 7:20 PM PT  
- **Impact**: Unauthorized access to ~50,000 customer records, including PII and financial data  
- **Estimated Financial Loss**: $100,000  
- **Root Cause**: Exploited URL-based vulnerability (forced browsing)

---

## 📅 Timeline Highlights

| Date             | Event                                                                 |
|------------------|-----------------------------------------------------------------------|
| Dec 22, 2022     | Initial extortion email received by employee—marked as spam          |
| Dec 28, 2022     | Follow-up email sent with sample stolen data, higher ransom demand   |
| Dec 28–31, 2022  | Security team investigation; root cause and data exposure confirmed  |

---

## 🧪 Investigation Findings

- The attacker exploited a **forced browsing vulnerability** within the e-commerce platform by altering order numbers in the URL, allowing access to thousands of unique customer order pages.
- Web server logs confirmed sequential scraping behavior.
- No authentication was required for accessing purchase confirmation pages.

---

## 🛠️ Response Actions

- Public disclosure of breach and customer notification
- Complimentary identity protection services provided to victims
- Log analysis pinpointed the high-volume, programmatic access

---

## 🧭 Recommendations

- **Routine vulnerability scans** and **penetration testing**
- **Access control improvements**, including:
  - **Allowlisting** for known URLs
  - **Authentication enforcement** on sensitive endpoints

---

## 🧱 Pyramid of Pain Tie-In

This incident underscores how **observable indicators like URLs and file access patterns (TTPs)**—which reside high on the Pyramid of Pain—can provide more meaningful, proactive defense opportunities than simple hashes or IPs. By remediating behavioral patterns such as forced browsing and improving authorization logic, the organization can *significantly increase the pain* for future attackers.

<!-- Pyramid of Pain slides: https://docs.google.com/presentation/d/100DBHBMbzkYcWo6tNu5lsB9eSsM9snMe71Oxm5WtUEw/edit?usp=sharing -->

---

## ✅ Review Goals

| Goal | Outcome |
|------|---------|
| 1. What happened? | Data exfiltration via forced browsing attack |
| 2. When? | Dec 28, 2022 at 7:20 PM PT |
| 3. Response Actions? | PR response, identity protection, server log review |
| 4. Recommendations? | Patch web app, enforce URL access controls, regular testing |

---

## 📁 GitHub Readiness

- [ ] Add to `/incident-reports/final-report-review.md`
- [ ] Link to associated playbook or Pyramid of Pain presentation
- [ ] Tag with `#IRL #postmortem #retail`

---

## 🧠 Codex Prompt (optional)

> "Generate a GitHub portfolio-ready Markdown report summarizing a real-world security incident involving a data breach. Include timeline, root cause analysis, remediation steps, and NIST lifecycle alignment. Cross-reference the Pyramid of Pain."

---
