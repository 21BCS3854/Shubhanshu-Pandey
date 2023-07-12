# Error Handling
This Solidity program is simple is that how we handle error in the program.The purpose of this program is to serve as a starting point for those who are want to learn how we error hanling work.
## Description
This program is a simple contract written in Solidity, a programming language used for smart contracts on the blockchain. The contract has a single function "statement" in which we discussing all the the satement ( require, assert, revert statement). This program servers as a simple and straightforward introduction that how we handle Error in the Solidity programming,  and can be used as a stepping stone for more complex projects in the future.
## Getting Started
### Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g. ErrorHandling.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract ErrorHandling{
    function statement(uint256 x) external pure returns (uint256) {
        // require statement
        require(x>0, "x never less than zero");
        
        // assert statement
        assert(x!=0);
        
        // revert statement
        if (x == 42) {
            revert("x cannot be 42");
        }
        
        return x * 2;
    }
}
```
* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile ErrorHandling.sol" button.
* Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. After that we go to the Deployed contracts and click on siled button and call the x value to confirm the statement.
* After that we pass the value of x in the statement 
