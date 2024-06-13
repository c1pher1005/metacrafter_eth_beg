# MyToken Solidity Contract

This Solidity contract defines a basic ERC20-like token called `MyToken`. It includes functionalities for minting new tokens and burning existing tokens, along with storing basic details about the token.

## Contract Overview

The contract `MyToken` includes the following functionalities and public variables:

### Public Variables

1. **Token Name (`TkName`)**: A public string variable that holds the name of the token.
2. **Token Abbreviation (`TkAbbrv`)**: A public string variable that holds the abbreviation or symbol of the token.
3. **Total Supply (`Total_Supply`)**: A public uint variable that keeps track of the total supply of tokens issued.

### Mapping

- **Token Balances (`Tk_balance`)**: A mapping from addresses (`address`) to unsigned integers (`uint`), which stores the balance of tokens for each address.

### Functions

1. **Minting Function (`Mint`)**:
   - **Parameters**: `address _address`, `uint _number`
   - **Description**: Increases the total token supply and the balance of the specified address.
   - **Implementation**: Adds `_number` tokens to `Total_Supply` and to the balance of `_address`.

2. **Burning Function (`Burn`)**:
   - **Parameters**: `address _address`, `uint _number`
   - **Description**: Decreases the total token supply and the balance of the specified address, provided that the balance is sufficient.
   - **Implementation**: Checks if `_address` has at least `_number` tokens; if true, subtracts `_number` from `Total_Supply` and from the balance of `_address`.

### Requirements

- **Mint Function**: Increases the total supply and the balance of a specified address.
- **Burn Function**: Decreases the total supply and the balance of a specified address, with checks to ensure the balance is sufficient.

### Additional Information

- This contract does not implement a transfer function, approval mechanism, or other ERC20 functionalities beyond basic minting and burning.
- The contract lacks access control mechanisms, so any address can call `Mint` or `Burn`.

### SPDX License Identifier

- The contract is licensed under the MIT License (`SPDX-License-Identifier: MIT`).

### Usage

- Deploy the contract on a suitable Ethereum Virtual Machine (EVM) like Ganache or Remix.
- Interact with the contract using a suitable Ethereum wallet or through a custom interface.

### Disclaimer

- This contract is a simplified example and lacks many features necessary for a production-ready token (e.g., security measures, gas optimizations, event emissions).
