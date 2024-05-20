# MyFunctionError2
# Discription 
* A basic smart contract in which each of the functions that follow is executed: revert(), assert(), and require().

# Getting Launched
Installing Remix Online IDE

* Complete all required installations ahead of time.
* Get "ErrorHandling.sol" from the original file and transfer it.
* Go to https: https://remix.ethereum.org start the IDE.

# Using Remix to run a Program
Create folder inside Remix.

* Duplicate the unedited content from ErrorHandling.sol and insert it into the new file.
* Click on the "Solidity Compiler" button to build the contract.
* Click on the "Deploy and Run transactions" button to configure the smart contract.
* After a successful launch, examine the user interface for contract interaction.

# Function Code

 // SPDX-License-Identifier: MIT
pragma solidity ^0.8.1;

contract ErrorHandlingContract {
  uint public value;

function setvalue(uint _value) public {

    require(_value > 0, "Value must be greater than 0.");

    assert(_value != value);

    value = _value;
  }

 function performDivision(uint _numerator, uint _denominator) public pure returns (uint) {
 
    require(_denominator != 0, "Cannont divide by zero.");

    if (_numerator % _denominator != 0) {
        revert("Numerator must be divisible by denominator.");
    }

    return _numerator / _denominator;
  }
  
}


# Autor
* Michaela Ariane B. Cabrera
* Email: 8214136@ntc.edu.ph

