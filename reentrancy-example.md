# Reentrancy Example (Smart Contract)

## Vulnerable Scenario
A smart contract allows withdrawals without updating the balance first:

```solidity
function withdraw(uint amount) public {
    msg.sender.call.value(amount)();
    balances[msg.sender] -= amount;
}
