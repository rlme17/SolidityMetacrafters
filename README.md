# Project Title

Getting Started with SolidityMetaCrafter

## Description

The initiative involves a Solidity-driven Ethereum smart contract geared towards the generation, oversight, and distribution of a bespoke token.

## Getting Started
### Installing
To run this program, use Remix, an online Solidity IDE, available at https://remix.ethereum.org/.

On Remix, create a new file using the "+" on the left sidebar, and save it with a .sol extension like MyToken.sol. Then, copy and paste the following code into this new file:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {

    // public variables here
    string public tokenName = "Solidity";
    string public tokenAbbreviation = "Sol";
    uint public totalSupply = 100;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

```

To compile the code, go to "Solidity Compiler" on the left. Make sure "Compiler" is set to "0.8.18" or a similar version, then click "Compile MyToken.sol".
To deploy, head to "Deploy & Run Transactions" on the left. Select "MyToken" from the list and click "Deploy".
Once deployed, you can start interacting with the contract.

## Help

Ensure you compile MyToken.sol first before initiating its deployment.
Make sure you choose MyToken.sol as the contract prior to launch.

## Authors

Contributors names and contact info
Richard Espino(richespino17@gmail.com)

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
