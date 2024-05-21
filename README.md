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

pragma solidity ^0.8.23;

contract FunctionAndErrors1 {

    uint256 public value;

    function requireValue(uint256 _newValue) external {
    
        require(_newValue >= 1 && _newValue <= 2000, "There is a value range of 1 to 2000 that you cannot exceed.");
        
        value = _newValue;
    }

    function assertValue(uint256 _num) external pure returns (uint256) {
    
        assert(_num >= 1 && _num <= 2000);
        
        return _num;
    }

    function revertValue(uint256 _num) external pure returns (uint256) {
    
        if (!(_num >= 1 && _num <= 2000)) {
        
            revert("The value must be between 1 and 2000.");
        }
        return _num;
    }

    // Function where sets a given value if each of the checks match.
    
    function setValue(uint256 _value) external {
    
        require(_value >= 1 && _value <= 2000, "Value must be between 1 and 2000.");
        
        assert(_value >= 1 && _value <= 2000); 

        value = _value;
    }
}


# Autor
* Michaela Ariane B. Cabrera
* Email: 8214136@ntc.edu.ph

