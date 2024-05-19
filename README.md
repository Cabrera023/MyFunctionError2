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

 function requireValue(uint256 _newValue) external {
   require(_newValue >= 200 && _newValue <= 4000, "There is a value range of 200 to 4000 that you cannot exceed.");
    value = _newValue;
  }
