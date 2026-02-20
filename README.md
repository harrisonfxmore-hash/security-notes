## Security Notes

Welcome to my cybersecurity research repository.

This repository documents my learning progress and practical research in:

- Web Application Security
- Smart Contract / Web3 Security
- Bug Bounty Methodologies
- Vulnerability Analysis

---

## Web Security - OWASP Top 10

### 1. SQL Injection (SQLi)
- Definition:
  Attacker injects malicious SQL statements via user input to manipulate the database.
- Impact:
  Can read, modify, or delete database data; may lead to full system compromise.
- Prevention:
  Use prepared statements / parameterized queries, input validation, and ORM frameworks.

### 2. Cross-Site Request Forgery (CSRF)
- Definition:
  Forces authenticated users to execute unwanted actions on a web app without their consent.
- Impact:
  Unauthorized transactions, account changes, or data deletion.
- Prevention:
  Use anti-CSRF tokens, enforce same-site cookies, and validate origin headers.

### 3. Broken Access Control
- Definition:
  Users can access data or functions outside their privileges.
- Impact:
  Data leaks, privilege escalation, unauthorized actions.
- Prevention:
  Implement server-side role checks, never rely on client-side restrictions.

### 4. Security Misconfigurations
- Definition:
  Improperly configured servers, databases, or apps (default passwords, verbose errors, open directories).
- Impact:
  Attackers gain access or information; system is easily exploitable.
- Prevention:
  Harden configurations, remove defaults, disable unnecessary features, patch regularly.

### 5. Sensitive Data Exposure
- Definition:
  Storing or transmitting sensitive data insecurely.
- Impact:
  Leaks of passwords, credit cards, personal info.
- Prevention:
  Encrypt data at rest and in transit, use strong protocols (HTTPS, TLS), avoid exposing secrets.

### 6. Insecure Deserialization
- Definition:
  Processing untrusted serialized data without validation.
- Impact:
  Remote code execution or privilege escalation.
- Prevention:
  Avoid deserialization of untrusted data; validate inputs, use safe libraries.

### 7. Using Components with Known Vulnerabilities
- Definition:
  Outdated libraries or frameworks with public exploits.
- Impact:
  Exploitation of known vulnerabilities.
- Prevention:
  Regularly update dependencies, use vulnerability scanning tools.

### 8. Cross-Site Scripting (XSS)
- Definition:
  Injection of malicious scripts into web pages viewed by others.
- Impact:
  Session hijacking, phishing, defacement.
- Prevention:
  Input validation, output encoding, use CSP, avoid unsafe innerHTML.

### 9. Insufficient Logging & Monitoring
- Definition:
  Failing to log events or monitor suspicious activity.
- Impact:
  Breaches go undetected; delayed response increases damage.
- Prevention:
  Implement centralized logging, alerting, and auditing.

### 10. Broken Authentication
- Definition:
  Weak authentication mechanisms or session management issues.
- Impact:
  Account takeover, impersonation.
- Prevention:
  Enforce strong passwords, MFA, secure session management, limit login attempts.

### XSS (Cross-Site Scripting)
- Definition:XSS is a vulnerability that allows an attacker to inject malicious JavaScript into a web application.
Impact:Attackers can steal session cookies, hijack user accounts, or execute actions on behalf of users.
Prevention:Input validation, output encoding, Content Security Policy (CSP), and avoiding unsafe rendering of user input.
  

### SQL Injection
- Definition:Injecting malicious SQL queries through user input to manipulate databases.
- Impact:Attackers can read, modify, or delete database records.
- Prevention:Use prepared statements, parameterized queries, and input validation.
- 

## Authentication & Authorization Issues
- Common mistakes:
  - Weak passwords or no password complexity rules
  - Lack of multi-factor authentication (MFA)
  - Broken session management
  - Users accessing data or functions outside their role
- Mitigation strategies:
  - Enforce strong password policies
  - Implement multi-factor authentication
  - Properly manage session timeouts and invalidation
  - Enforce role-based access control on the server side

---

## Smart Contract Security

### Reentrancy
- Definition:
  A vulnerability where a smart contract function calls an external contract before updating its state, allowing repeated withdrawals.
- Risk:
  Attackers can drain funds from the contract repeatedly before balances update.
- Mitigation:
  - Use the Checks-Effects-Interactions pattern
  - Limit external calls
  - Consider using ReentrancyGuard libraries (e.g., OpenZeppelin)

### Integer Overflow / Underflow
- Definition:
  Occurs when arithmetic operations exceed the max/min value for a variable type.
- Risk:
  Can lead to incorrect balances, bypassing limits, or contract malfunction.
- Mitigation:
  - Use safe math libraries (like OpenZeppelin SafeMath)
  - Update to Solidity >=0.8 which has built-in overflow checks

### Access Control Issues
- Example:
  Unauthorized users calling admin-only functions.
- Prevention:
  - Use modifiers like `onlyOwner` in Solidity
  - Validate user roles before executing sensitive functions
  - Avoid hardcoding privileged addresses; use flexible role management

---

## Goal

To continuously improve my vulnerability detection skills, document best practices, and contribute to a safer Web3 and web ecosystem.
