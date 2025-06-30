# Access Control Assessment – Accounting Incident

## \ud83d\udcdd Notes
- The event log shows that a former employee named **Brent Morales** accessed the payroll file after termination.
- The login was from an **unknown IP address** on **June 12th at 10:34 AM**.

## \u2757 Issues Identified
- Brent\u2019s account was **still active** even after his employment ended.
- All employees are using a **shared cloud drive**, making it difficult to audit or restrict access on a per-user basis.

## \u2705 Recommendations
1. **Automate deprovisioning**: Implement a system that immediately revokes account and file access when an employee departs the company.
2. **Enforce role-based access controls (RBAC)**: Assign **individual accounts** with permissions aligned to specific job responsibilities to limit unauthorized access.

---

> This assessment highlights the importance of timely access removal and proper segmentation of user privileges to mitigate internal threats and improve overall data security.
