# Integer Overflow / Underflow Example

## Vulnerable Scenario
A smart contract incorrectly handles arithmetic operations:

```solidity
uint8 total = 255;
total += 1; // Overflow occurs, wraps around to 0
