Add CSRF example
---

### **CSRF Example** (`csrf-example.md`)

```markdown
# CSRF (Cross-Site Request Forgery) Example

## Vulnerable Scenario
A user is logged in to a banking website.  
An attacker tricks the user into visiting a malicious page that submits a transfer form:

```html
<img src="https://bank.com/transfer?amount=1000&to=attacker_account">
