[![](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/Ethereum-Private-Data.jpg)](https://github.com/ethsecurityexamples/Accessing_Private_Data/blob/main/Ethereum-Private-Data.jpg)

In Solidity when declaring a variable as *private*, does not mean that the variable is hidden. Far from there.

A *private* variable means that other smart contracts can not access that variable.

But that *private* variable can be read by some tools, for example Truffle Suite.

This is possible because Ethereum Blockchain is open to anyone, and data can be read anytime.

So: never store private data for instance like passwords, in the Blockchain.

Let's see a demostration about all this.


------------