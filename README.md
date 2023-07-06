# MY TOKEN
MyToken is a simple ERC20-compatible token contract implemented in Solidity. It allows token minting and burning operations.The purpose of this program is to how we can create a token for those who are new to Solidity and want to get a feel for how it works.
## Description
This program is a Token contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a two function in which first one is mint and second is burn function and we have three variables (tokenName, tokenAbbrv, totalsupply). This program serves as a token the way how we create token in Solidity programming, and can be used as a stepping stone for more complex projects in the future.
* mint: This function allows the contract owner (or anyone with the appropriate permissions) to mint new tokens and assign them to a specified address. It takes two parameters: _receiver (the address to receive the minted tokens) and _value (the amount of tokens to be minted).
* burn: This function allows an address to burn (destroy) a specified amount of tokens from its own balance. It takes one parameter: _value (the amount of tokens to be burned). Before burning the tokens, it checks whether the sender has enough balance to perform the burn operation.
## Getting Started
### Executing Program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., Token.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    string public tokenName="META";
    string public tokenAbbrv="MTA";
    uint256 public totalSupply= 0;

    mapping(address => uint256) public balances;
    
    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    function burn(address _address, uint256 _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
        balances[_address] -= _value;
        }
    }
}
```
* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible 
  version), and then click on the "Compile Token.sol" button.
* Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" 
  contract from the dropdown menu, and then click on the "Deploy" button.
* After that go to the Deployed Contract and click on "MyToken" scroll down button. After that we copy the account clipboard and paste to mint address bar.
* After that we click mint scroll down button and add the value in the mint value (eg.. we add 1000 unit) then we click on transact, then we see that we have totalsupply we got all 1000 unit.
* After this same goes to burn but in burn how many we want to burn (eg.. we want to burn 500) after that we transact it then we see that we left with 500 totalsupply.
* If we burn the more than totalsupply there is no change in the total supply because of the we using condition satement to overcome this situation.

