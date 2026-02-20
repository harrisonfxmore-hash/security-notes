# Broken Access Control Example

## Vulnerable Scenario
A user can access another user’s data by changing a URL parameter:
If the attacker changes `123` to another user ID, they can view someone else’s data.

## Impact
- Data leaks and privacy violations  
- Unauthorized actions or privilege escalation

## Mitigation
- Enforce server-side access checks  
- Never rely on client-side controls  
- Implement role-based access control
