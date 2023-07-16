# Degen Gaming Token (DGN) - Readme

## Introduction:
The Degen Gaming Token (DGN) is an ERC-20 standard token implemented on the Ethereum blockchain. It allows users to participate in various gaming applications and platforms within the ecosystem. This token contract is deployed on the Ethereum network and can be utilized by developers to integrate DGN functionality into their decentralized applications (DApps).

## Token Information:

* Token Name: Degen Gaming Token
+ Symbol: DGN
- Decimals: 0

## Smart Contract Features:

1. **Minting Function:**
The contract has a mint function that allows the contract owner (deployer) to mint new DGN tokens and send them to a specified address. This function is protected by the onlyOwner modifier, ensuring that only the contract owner has the privilege to create new tokens.

2. **Decimals Override:**
The contract overrides the decimals() function to return 0. This means that the token is non-divisible, and each token unit represents one whole DGN.

3. **Balance Retrieval:**
The contract has a getBalance function that allows any external user to query their DGN token balance. This function is read-only and does not modify the contract state.

4. **Token Transfer:**
The contract has a transferTokens function, which provides a way for users to transfer their DGN tokens to another address. Before initiating the transfer, the user must approve the contract to spend a certain amount of DGN tokens on their behalf. The contract then transfers the approved amount to the specified receiver.

5. **Token Burning:**
The contract inherits from ERC20Burnable, which means that token holders can burn (destroy) their DGN tokens, reducing the total supply. This is useful for scenarios like reducing the token supply over time or implementing deflationary mechanisms.

6. **Access Control:**
The contract uses the Ownable module from the OpenZeppelin library, which provides a basic access control mechanism. The onlyOwner modifier is applied to the mint function, ensuring that only the contract deployer can mint new tokens.

## OpenZeppelin Library:
The contract utilizes the OpenZeppelin library, which is a collection of reusable smart contracts for Ethereum. It imports the following contracts:

* ERC20.sol: This provides the implementation of the ERC-20 standard functions for the token.
+Ownable.sol: This provides basic access control functionalities, allowing the contract to have an owner with special privileges.
- ERC20Burnable.sol: This extends the ERC-20 token to include burning (destroying) of tokens.

## Security Considerations:

* The contract owner should be a trusted entity, as they have control over the minting function, which can increase the token supply. Ensure the contract is deployed by a reputable entity.
+ The approve function should be used carefully, and users should be aware of the amount they approve for spending by the contract to avoid potential misuse.
- Smart contract upgrades and changes should be handled carefully, considering the impact on existing token holders and gaming applications using DGN.

## Author
Vaishnavi Arora

## License
This contract is licensed under the MIT License. SPDX-License-Identifier: MIT. loom video link,
https://www.loom.com/share/25cd9aa01d4b4065bc979eb5528a0165?sid=294edb41-b1fb-47bb-b341-739db043a647
