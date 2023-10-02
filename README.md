//Target Contract:
//This contract contains the logic that will be executed via delegate call.
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract TargetContract {

    function increaseBy(uint256 amount, address callingContract) external {
        StorageContract(callingContract).updateValue(amount);
    }
}
