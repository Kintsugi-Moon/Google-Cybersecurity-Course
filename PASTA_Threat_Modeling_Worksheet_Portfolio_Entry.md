# PASTA Threat Modeling Worksheet – Sneaker Company Mobile App

## I. Define Business and Security Objectives
- The app should provide a seamless user experience for buyers and sellers to connect and transact.
- It must ensure data privacy and secure account management to build user trust.
- A smooth and secure payment process is essential to prevent legal complications and customer dissatisfaction.

## II. Define the Technical Scope
**Technologies used:**
- Application Programming Interface (API)
- Public Key Infrastructure (PKI)
- SHA-256
- SQL

**Priority Tech Focus:**
I would prioritize evaluating the **API** first, as it serves as the main connection point between users and backend services. APIs are commonly targeted for attacks like injection, broken authentication, or excessive data exposure. Securing this surface reduces the chance of external threats accessing sensitive data or manipulating app functions.

## III. Decompose Application
Referencing the data flow diagram, the app allows users to search for sneaker listings from a database. Information flows between the user interface and backend systems using SQL queries and API calls. The system must ensure data confidentiality and integrity during these exchanges using encryption and proper access controls.

## IV. Threat Analysis
- **External Threat:** A malicious actor may exploit the API to gain unauthorized access or extract sensitive data (e.g., via broken access control or injection).
- **Internal Threat:** An employee could misuse their access to user data or account information, leading to privacy breaches or insider attacks.

## V. Vulnerability Analysis
- **SQL Injection:** If SQL queries are not properly sanitized, attackers could execute arbitrary commands and access or corrupt the database.
- **Improper Input Validation on API Endpoints:** Weak or missing input checks may allow attackers to send malicious data and compromise the application or users' accounts.

## VI. Attack Modeling
Refer to the PASTA Attack Tree. For instance:
- A threat actor could exploit a broken API to access stored credentials.
- An insider might copy user data and sell it on a dark web forum.
- A poorly configured database may expose sensitive data if not encrypted properly.

## VII. Risk Analysis and Impact – Security Controls
1. **Input Validation and Sanitization** – Prevent injection attacks by validating all user inputs and escaping database queries.
2. **Access Controls and Role-Based Permissions** – Limit data access based on user roles to prevent insider misuse.
3. **TLS Encryption with Strong PKI** – Ensure all communications are encrypted using AES/RSA to secure data in transit.
4. **Logging and Monitoring** – Track and analyze system activity to detect abnormal behavior or unauthorized access early.
