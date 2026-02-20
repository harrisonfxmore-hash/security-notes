# SQL Injection Example

## Vulnerable Scenario
A login query that doesn’t sanitize input:

```sql
SELECT * FROM users WHERE username = 'user' AND password = 'pass';
