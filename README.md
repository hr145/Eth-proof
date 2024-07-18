MyToken

Description

This Solidity program is a simple smart contract for a basic token system. The purpose of this program is to demonstrate the creation of a token, minting new tokens, and burning existing tokens. It serves as a foundation for more complex Solidity programming tasks related to token management.

The contract has the following main functions:

mint: Allows the creation of new tokens.
burn: Allows the destruction of existing tokens.
Getting Started
Executing Program
To run this program, you can use Remix, an online Solidity IDE. Follow the steps below to get started:

Steps to Execute
Visit Remix:
Go to the Remix website at Remix IDE.

Create a New File:

Click on the "+" icon in the left-hand sidebar.
Save the file with a .sol extension (e.g., MyToken.sol).

code:

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract MyToken {
    string public tokenName = "META";
    string public tokenAbbry = "MTA";
    uint public totalSupply = 0;

    mapping(address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
Compile the Code:

Click on the "Solidity Compiler" tab in the left-hand sidebar.

Ensure the "Compiler" option is set to version 0.8.18.

Click on the "Compile MyToken.sol" button.


Deploy the Contract:

Go to the "Deploy & Run Transactions" tab in the left-hand sidebar.

Select the "MyToken" contract from the dropdown menu.

Click on the "Deploy" button.


Interact with the Contract:

After deployment, interact with the contract using the available functions:

mint: Mint new tokens to a specified address.

burn: Burn tokens from a specified address.

Example Interactions


Mint Tokens:

Select the mint function.

Enter the address and the amount of tokens to mint.

Click "transact" to execute.


Burn Tokens:

Select the burn function.

Enter the address and the amount of tokens to burn.

Click "transact" to execute.


Authors

HARSH

@HARSH RAJ

License

This project is licensed under the MIT License - see the LICENSE.md file for details.

