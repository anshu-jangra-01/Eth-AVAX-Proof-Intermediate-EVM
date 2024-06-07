# errorHandling Smart Contract
This is solidity project "errorHandling".

## Description
This Solidity smart contract demonstrates basic error handling mechanisms using require, assert, and revert. It includes functions setvalue for setting a value and performDivision fordivision.

## Getting Started
### Executing Program
To run the program use Remix IDE, an Online Platform https://remix.ethereum.org/.

Once you are on the Remix website, create a new file and save the file with a .sol extension (like errorHandling.sol). Copy and paste the code into the file:
```javascript
//SPDX-License-Identifier:MIT
pragma solidity ^0.8.1;
contract errorHandling{
  uint public value;
  function setValue(uint _value) public {
    require(_value>0,"value must be greater than 0");
    assert(_value != value);
    value = _value;
  }
  function performDivision(uint _numerator, uint _denominator) public pure returns (uint){
    require(_denominator !=0, "cannot divide by zero");
      if( _numerator%_denominator!=0){
       revert("numerator must be divisible by denominator");
    }
     return _numerator/_denominator;
  }
}
```
Compile the code and then deploy it
Add data to value and then pass value to _numerator and _denominator for division.

## Authors

Anshu

## License

This project is licensed under the MIT License - see the LICENSE.md file for details




