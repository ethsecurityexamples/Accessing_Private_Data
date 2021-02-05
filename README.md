[![](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/Ethereum-Private-Data.jpg)](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/Ethereum-Private-Data.jpg)

In Solidity when declaring a variable as *private*, does not mean that the variable is hidden. Far from there.

A *private* variable means that other smart contracts can not access that variable.

But that *private* variable can be read by some tools, for example Truffle Suite.

This is possible because Ethereum Blockchain is open to anyone, and data can be read anytime.

So: never store private data for instance like passwords, in the Blockchain.

Let's see a demostration about all this.


------------

First of all we need to have access to a Ethereum testnet, let's say Ropsten.

And deploy there a contract with a *private* variable.

For a nice guide to how connect to Ropsten testnet, take a look to this link:
[5 minute guide to deploying smart contracts with Truffle and Ropsten](https://medium.com/coinmonks/5-minute-guide-to-deploying-smart-contracts-with-truffle-and-ropsten-b3e30d5ee1e "5 minute guide to deploying smart contracts with Truffle and Ropsten")

In our case we are gonna use a contract with the license:
> SPDX-License-Identifier: MITIn our case, we are gonna use a SPDX-License-Identifier: MIT

Take a look to it:



    AccessingPrivateData.sol


------------



First of all let's use Truffle to get access to Ropsten testnet:

[![](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/1.jpg)](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/1.jpg)

Now, check the contract in the .sol file, and see the address where the contract is deployed and stored. This address is:



    0x3505a02BCDFbb225988161a95528bfDb279faD6b

and save that address in a varible inside the truffle console:

[![](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/3.jpg)](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/3.jpg)

Now let's recover the information inside the slot number 2, where the password variable is stored:

to do that we can use the Web3 API funtion: 

    getStorageAt

you can fetch its documentation here:
[Web3 API](https://web3js.readthedocs.io/en/v1.2.1/web3-eth.html#getstorageat "Web3 API")

[![](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/4.jpg)](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/4.jpg)


