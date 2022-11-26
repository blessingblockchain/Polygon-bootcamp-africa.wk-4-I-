# Polygon-bootcamp-africa.wk-4-I-
Smart contract interactions and minting NFts 

# GAS #

1. Every deployed transaction, smart contract, or execution of a smart contract, must be run on every single full node on the Ethereum blockchain to guarantee validity. This is wildly inefficient (though newer blockchains are streamlining this)!
2. Because smart contracts are Turing complete, they can potentially execute forever, locking up every single node on the blockchain.

****What is Turing completeness?****
Practically, a programming language that is Turing complete is able to solve or represent any computational problem, no matter how complex, given enough time and resources. In particular, that has a couple of implications: 
1. Any Turing complete language can theoretically be used to represent the logic of another Turing complete language, though the implementation may be unreasonably long.
2. Turing complete programs can end up looping and executing forever. In fact, there is no universal way to prove that such a program will not end up running forever (otherwise known as the "halting problem").
For example, a regular calculator is not Turing complete, because it allows for only a few types of calculations. However, a computer or scientific calculator is Turing complete because any type of program can be executed on it.

Since smart contract programs can run forever, gas has become the practical way in Ethereum to manage the impact of a blockchain program! Every computation or transaction made on the blockchain costs some fees. These fees prevent expensive (or endless) contract executions, ensure miners are fairly compensated for the work they do, and provide a fair market to prioritize which transactions make it onto the blockchain.

# Calculating Gas Costs

For any given program, the total gas used is calculated as the sum of the gas for each operation executed by the Ethereum Virtual Machine. For example, adding two numbers in a smart contract costs 3 gas, whereas sending a transaction costs 21,000 gas.

The total cost of gas is found by taking the amount of gas used in by a smart contract and multiplying by the **gas price**, a value set by you, the transaction sender.

![https://assets-global.website-files.com/6171e9fea621c60456b9f9ad/621d582167888e9db39cf46b_Screen%20Shot%202022-02-28%20at%203.17.24%20PM.png](https://assets-global.website-files.com/6171e9fea621c60456b9f9ad/621d582167888e9db39cf46b_Screen%20Shot%202022-02-28%20at%203.17.24%20PM.png)

Setting a higher gas price for your transaction means it's more likely to be confirmed on the blockchain, as the Ethereum blockchain can only confirm about 15 transactions a second. However, it also costs more Ether for the sender.

Another important value that can be set is the **gas limit,** or the maximum amount of gas you're willing to spend on your transaction.

By multiplying the gas price by the gas limit, you'll get the maximum amount of Ether you're allowing Ethereum to spend on gas fees for any particular transaction.

![https://assets-global.website-files.com/6171e9fea621c60456b9f9ad/61c0d2509596cd78a9042a41_transactionfee.jpg](https://assets-global.website-files.com/6171e9fea621c60456b9f9ad/61c0d2509596cd78a9042a41_transactionfee.jpg)

****What is "gwei" or "wei", and how do they relate to ETH?
“Wei” is the smallest unit of Ether, where 10¹⁸ Wei represents 1 Ether. One gwei is 10⁹ wei, and there are 10⁹ gwei per Ether.****

