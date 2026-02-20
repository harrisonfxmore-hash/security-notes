# Security Notes

Welcome to my cybersecurity research repository.

This repository documents my learning progress and practical research in:

- Web Application Security
- Smart Contract / Web3 Security
- Bug Bounty Methodologies
- Vulnerability Analysis

---

## Web Security

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
