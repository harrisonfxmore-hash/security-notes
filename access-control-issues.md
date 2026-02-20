---

### **Access Control Issues (Smart Contract)** (`access-control-issues.md`)

```markdown id="access-control"
# Smart Contract Access Control Issues

## Vulnerable Scenario
A function intended for admin use is callable by anyone:

```solidity
function mintTokens(uint amount) public {
    totalSupply += amount;
}
