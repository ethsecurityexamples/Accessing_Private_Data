[![](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/Ethereum-Private-Data.jpg)](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/Ethereum-Private-Data.jpg)

In Solidity when declaring a variable as *private*, does not mean that the variable is hidden. Far from there.

A *private* variable means that other smart contracts can not access that variable.

But that *private* variable can be read by some tools, for example Truffle Suite.

This is possible because Ethereum Blockchain is open to anyone, and data can be read anytime.

So: never store private data for instance like passwords, in the Blockchain.

Let's see a demostration about all this.


------------

First of all we need to hace access to a Ethereum testnet, let's say Ropsten.

And deploy there a contract with a *private* variable.

For a nice guide to how connect to Ropsten, take a look to this link:
[5 minute guide to deploying smart contracts with Truffle and Ropsten](https://medium.com/coinmonks/5-minute-guide-to-deploying-smart-contracts-with-truffle-and-ropsten-b3e30d5ee1e "5 minute guide to deploying smart contracts with Truffle and Ropsten")


