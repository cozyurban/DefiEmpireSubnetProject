# Defi Empire Subnet Project

This project demonstrates a basic implementation of an ERC20 token in Solidity. The contract includes functions for transferring tokens, approving allowances, transferring tokens on behalf of another address, minting new tokens, and burning tokens.

## Contract Details

- Name: Solidity by Example
- Symbol: SOLBYEX
- Decimals: 18

## Table of Contents

- Introduction
- Functions
  - transfer
  - approve
  - transferFrom
  - mint
  - burn
- Events
  - Transfer
  - Approval
- Usage
- License

## Introduction

This ERC20 contract provides the fundamental functionalities of an ERC20 token, including token transfers, allowances, minting, and burning. It serves as a simple example for understanding the basics of ERC20 tokens in Solidity.

## Functions

`transfer`
`        function transfer(address recipient, uint amount) external returns (bool)
   `
Transfers `amount` of tokens from the caller's account to the `recipient` account.
`approve`
`        function approve(address spender, uint amount) external returns (bool)
   `
Approves spender to spend amount of tokens on behalf of the caller.
`transferFrom`
```
function transferFrom(
address sender,
address recipient,
uint amount
) external returns (bool)

    ```

Transfers `amount` of tokens from sender to `recipient` using the allowance mechanism. The caller must have been approved to spend at least `amount` tokens on behalf of `sender`.
`mint`
`        function mint(uint amount) external
   `
Mints `amount` of new tokens to the caller's account, increasing the total supply.
`burn`
`        function burn(uint amount) external
   `
Burns `amount` of tokens from the caller's account, decreasing the total supply.
Events
`Transfer` Event
`        event Transfer(address indexed from, address indexed to, uint value)
   `
Emitted when value tokens are transferred from one account (from) to another (to).
`Approval` Event
`        event Approval(address indexed owner, address indexed spender, uint value)
   `
Emitted when owner approves spender to spend value tokens on their behalf.

## Usage

To use this contract, deploy it to an Ethereum network using a tool like Remix, Truffle, or Hardhat. After deployment, you can interact with it using web3 or ethers.js, or through a frontend interface.
Example Interactions

1. Minting Tokens

   ```
       DegenToken.mint(1000);

   ```

2. Transferring Tokens

   ```
       DegenToken.transfer("0xRecipientAddress", 100);

   ```

3. Approving Allowance
   ```
       DegenToken.approve("0xSpenderAddress", 200);
   ```
4. Transferring Tokens on Behalf

   ```
       DegenToken.transferFrom("0xSenderAddress", "0xRecipientAddress", 50);

   ```

5. Burning Tokens

   ```
       DegenToken.burn(100);

   ```

## License

This project is licensed under the MIT License. See the LICENSE file for details.
