# Blockchain portfolio

A portfolio of my blockchain development and security works including code and notes

## Index
- [Introduction](#introduction)
- [Resources](#resources)
- [Tools](#tools)
- [Code](#code)
  - [SolidityToken](https://github.com/seeu-inspace/soliditytoken)
- [Attack techniques](#attack-techniques)
  - [Vulnerabilities | Web3 Security Library](https://github.com/immunefi-team/Web3-Security-Library/tree/main/Vulnerabilities)
  - [Integer Overflow / Underflow](#integer-overflow--underflow)
  - [Re-entrancy attacks](#re-entrancy-attacks)
  - [Unchecked Return Values For Low Level Calls](#unchecked-return-values-for-low-level-calls)


## Introduction

The **Blockchain** is a set of technologies in which the ledger is structured as a chain of blocks containing transactions and consensus distributed on all nodes of the network. All nodes can participate in the validation process of transactions to be included in the ledger.

There are two common types of operations that are carried out to create a cryptocurrency:
- **Mining (Proof-of-Work)** Validation of transactions through the resolution of mathematical problems by miners who use hardware and software dedicated to these operations. Whoever solves the problem first wins the right to add a new block of transactions and a reward;
- **Staking (Proof-of-Staking)** consists of users who lock their tokens in a node called a validator. The validators take turns checking the transactions on the network. If they perform well, they receive a prize distributed among all the participants of the validator, otherwise, they receive a penalty.
- Read also "[What Is the Difference Between Blockchain Consensus Algorithms?](https://pixelplex.io/blog/best-blockchain-consensus-algorithms/)" by Pixelplex

**Ethereum** is a blockchain that has popularized an incredible innovation: smart contracts, which are a program or collection of code and data that reside and function in a specific address on the network. Thanks to this factor, it is defined as a "programmable blockchain".

Note: By design, smart contracts are immutable.  This means that once a Smart Contract is deployed, it cannot be modified, with the exception of the [Proxy Upgrade Pattern](https://docs.openzeppelin.com/upgrades-plugins/1.x/proxies).

A token can be created with a smart contract. Most of them reside in the ERC20 category, which is fungible tokens. Other tokens are ERC-721 and ERC-1155, aka NFTs.

A **decentralized application**, also known as **DApp**, differs from other applications in that, instead of relying on a server, it uses blockchain technology. To fully interact with a DApp you need a wallet.
DApps are developed both with a user-friendly interface, such as a web, mobile or even desktop app, and with a smart contract on the blockchain. 

The fact that there is a user-friendly interface means that the "old vulnerabilities" can still be found. An example: If a DApp has a web interface, maybe an [XSS](https://owasp.org/www-community/attacks/xss/) on it can be found and exploited. Another evergreen is phishing, that is frequently used to steal tokens and NFTs.

The source code of the Smart Contracts is often written in **Solidity**, an object-oriented programming language. Another widely used programming language, but less than Solidity, is **Vyper** (Python).

Most of the time the smart contract code is found public in a github such as `github.com/org/project/contracts/*.sol` or you can get it from Etherscan, for example by going to the contract address (such as that of the DAI token), in the Contract tab you will find the code https://etherscan.io/address/0x6b175474e89094c44da98b954eedeac495271d0f#code and contract ABI > a json which indicates how the functions of the smart contract are called.
In any case, the source is almost always public. If it's not public, you can use an EVM bytecode decompiler such as https://etherscan.io/bytecode-decompiler, just enter the contract address here.

[Bitcoin Whitepaper](https://bitcoin.org/bitcoin.pdf) | [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/) | [Ethereum Yellow Paper](https://ethereum.github.io/yellowpaper/paper.pdf)

#### Web3 glossary

- **Decentralized Autonomous Organization (DAO)** A blockchain-based organization that is structured by self-enforcing smart contracts and democratically run by its users using open-source code. A vote is taken by network stakeholders on every decision.

- **Liquidity** The capacity to swap an asset without significantly changing its price and the simplicity with which an asset may be turned into cash are both examples of liquidity.

- **Oracle** A blockchain protocol receives external real-world data from Oracles, third-party information service providers. This implies that they can increase the security, veracity, and strength of the data that a blockchain network receives and make use of.

You can find more here: [Crypto Glossary | Cryptopedia](https://www.gemini.com/cryptopedia/glossary)

#### Ethereum glossary

- **application binary interface (ABI)** The standard way to interact with contracts in the Ethereum ecosystem, both from outside the blockchain and for contract-to-contract interactions.

- **bytecode** An abstract instruction set designed for efficient execution by a software interpreter or a virtual machine. Unlike human-readable source code, bytecode is expressed in numeric format.

- **Ethereum Improvement Proposal (EIP)** A design document providing information to the Ethereum community, describing a proposed new feature or its processes or environment.

- **Ethereum Request for Comments (ERC)** A label given to some EIPs that attempt to define a specific standard of Ethereum usage.

- **Ethereum Virtual Machine (EVM)** is a complex, dedicated software virtual stack that executes contract bytecode and is integrated into each entire Ethereum node. Simply said, EVM is a software framework that allows developers to construct Ethereum-based decentralized applications (DApps).

- **hard fork** A permanent divergence in the blockchain; also known as a hard-forking change. One commonly occurs when nonupgraded nodes can't validate blocks created by upgraded nodes that follow newer consensus rules. Not to be confused with a fork, soft fork, software fork, or Git fork.

- **wei** The smallest denomination of ether. 10<sup>18</sup> wei = 1 ether.

You can find more here: [ethereum.org/en/glossary/](https://ethereum.org/en/glossary/)

#### Personal security

- Store your assets in a **cold wallet** (hardware wallet) instead of a hot wallet (Centralized exchanges or CEXs). Some good examples are [Ledger](https://www.ledger.com/) and [Trezor](https://trezor.io/);
- Keep your **seedphrase** in a safe place and don't share it with anyone. If possible, use a solution like [Zeus from Cryptotag](https://cryptotag.io/products/zeus-starter-kit/);
- Use 2FA, use a password manager (like [KeePass](https://keepass.info/)), double check links and be aware of phishing, read [Five OpSec Best Practices to Live By](https://www.threatstack.com/blog/five-opsec-best-practices-to-live-by).
- Read also [The Ultimate Self Custody Guide by Webacy](https://www.linkedin.com/pulse/ultimate-self-custody-guide-webacy-maika-isogawa/)



## Resources

- [Web3 Security Library](https://github.com/immunefi-team/Web3-Security-Library)
- [A Comprehensive Smart Contract Audit Readiness Guide](https://learn.openzeppelin.com/security-audits/readiness-guide)
- [Blockchain Security Audit List](https://github.com/0xNazgul/Blockchain-Security-Audit-List)

**Vulnerabilities**
- [SWC Registry](https://swcregistry.io/)
- [All known smart contract-side and user-side attacks and vulnerabilities in Web3.0, DeFi, NFT and Metaverse + Bonus](https://telegra.ph/All-known-smart-contract-side-and-user-side-attacks-and-vulnerabilities-in-Web30--DeFi-03-31)

**Updates / News**
- [rekt.news](https://rekt.news/)
- [Blockchain Threat Intelligence](https://newsletter.blockthreat.io/)
- [DeFi Hacks Analysis - Root Cause](https://wooded-meter-1d8.notion.site/0e85e02c5ed34df3855ea9f3ca40f53b?v=22e5e2c506ef4caeb40b4f78e23517ee)



## Tools

**Blockchain exploration**
- [Metamask](https://metamask.io/)
- [Etherscan.io](https://etherscan.io)
- [Bitquery](https://explorer.bitquery.io/)

**Development Environment**
- [Solidity Visual Developer](https://marketplace.visualstudio.com/items?itemName=tintinweb.solidity-visual-auditor)
- [Remix](https://remix-project.org/)
  - [remixd](https://github.com/ethereum/remix-project/tree/master/libs/remixd)
- [Truffle Suite](https://trufflesuite.com/docs/)
  - [Ganache](https://github.com/trufflesuite/ganache)
- [Hardhat](https://hardhat.org/)
  - [Configuration | Hardhat](https://hardhat.org/hardhat-runner/docs/config)
  - [deploy.js](JavaScript/deploy.js)
- [Foundry](https://book.getfoundry.sh/)

**Libraries**
- [web3.js](https://web3js.readthedocs.io/)
  web3.js is very useful for interacting with a smart contract and its APIs. Install it by using the command `npm install web3`. To use it in Node.js and interact with a contract, use the following commands:
  ```javascript
   1: node;
   2: const Web3 = require('web3');
   3: const URL = "http://localhost:8545"; //This is the URL where the contract is deployed, insert the url from Ganache
   4: const web3 = new Web3(URL);
   5: accounts = web3.eth.getAccounts();
   6: var account;
   7: accounts.then((v) => {(this.account = v[1])});
   8: const address = "<CONTRACT_ADDRESS>"; //Copy and paste the Contract Address
   9: const abi = "<ABI>"; //Copy and paste the ABI of the Smart Contract
  10: const contract = new web3.eth.Contract(abi, address).
  ```
- [ethers](https://docs.ethers.org/)
  ethers is a JavaScript library for interacting with Ethereum blockchain and smart contracts. It provides a simple, lightweight interface for making calls to smart contracts, sending transactions, and listening for events on the Ethereum network. Install it with the command `npm install ethers`. An example is [_ethers.js](JavaScript/_ethers.js)

**Vulnerability scanners & others**
- [Slither](https://github.com/crytic/slither)
- [MythX](https://mythx.io/)
- [Solidity Function Profiler](https://github.com/EricR/sol-function-profiler)
- [ERC20 Verifier](https://erc20-verifier.openzeppelin.com/)
- [EVM Codes](https://www.evm.codes/)
- [Ethereum Security Toolbox](https://github.com/trailofbits/eth-security-toolbox)



## Code

[SolidityToken](https://github.com/seeu-inspace/soliditytoken) This project aims to create a token called "SolidityToken $STK". The tokens are then distributed to users who request them from the faucet.

**Solidity**
- [1_Lottery-BlockVariable.sol](Solidity/1_Lottery-BlockVariable.sol) an example of a smart contract for a lottery system written in Solidity, using `block.timestamp` for randomness
- [6_Attempt.sol](Solidity/6_Attempt.sol) deployed at [0x220DBDB08718cF4FF08Dc3520C75837ad59D8b18](https://goerli.etherscan.io/address/0x220dbdb08718cf4ff08dc3520c75837ad59d8b18) to win [this challenge](https://goerli.etherscan.io/address/0xcF469d3BEB3Fc24cEe979eFf83BE33ed50988502#code)
- [7_ERC20.sol](Solidity/7_ERC20.sol) smart contract for an ERC20 token (see: [EIP-20: Token Standard](https://eips.ethereum.org/EIPS/eip-20) and [openzeppelin-contracts/ERC20.sol](https://github.com/OpenZeppelin/openzeppelin-contracts/blob/v4.8.0/contracts/token/ERC20/ERC20.sol))
- [8_Telephone-attacker.sol](Solidity/8_Telephone-attacker.sol) to solve the [4. Telephone challenge](https://ethernaut.openzeppelin.com/level/4) from Ethernaut
- [9_BadRandomness.sol](Solidity/9_BadRandomness.sol) an example of Bad Randomness. See more about this issue here: [Bad Randomness | DASP TOP 10](https://dasp.co/#item-6)
- [11_MultiSig.sol](Solidity/11_MultiSig.sol) an example of Smart Contract for Multiple Signatures
- [12_Storages.sol](Solidity/12_Storages.sol) exercises on storage slots. Test with [storage_lookup.js](JavaScript/storage_lookup.js).
- [13_Proxy.sol](Solidity/13_Proxy.sol) an exercise on proxies. Test with [proxy_tests.js](JavaScript/proxy_tests.js).


**JavaScript**
- [digitalSignatures.js](JavaScript/digitalSignatures.js) is a simulation of public key cryptography
- [blockchain.js](JavaScript/blockchain.js) is a simple Proof of Work blockchain simulation
- [blockchain-explorer.html](JavaScript/blockchain-explorer.html) a simple Ethereum Blockchain Explorer, built using [Ethers](https://docs.ethers.org/) and [Infura](https://www.infura.io/)

**Resources**

- [Clean Contracts - a guide on smart contract patterns & practices](https://www.useweb3.xyz/guides/clean-contracts)
- [Smart Contract Security](https://ethereum.org/en/developers/docs/smart-contracts/security/)
- [Ethereum Smart Contract Security Best Practices](https://consensys.github.io/smart-contract-best-practices/)
- [Ethereum VM (EVM) Opcodes and Instruction Reference](https://github.com/crytic/evm-opcodes)



## Attack techniques

### <ins>Integer Overflow / Underflow</ins>

**Integer Overflow** happens because the arithmetic value of the operation exceeds the maximum size of the variable value type. An example: the variable `amount` is `uint256`. It supports numeric values from 0 to 2<sup>256</sup>. This means that a value like `0x8000000000000000000000000000000000000000000000000000000000000000` corresponding to the decimal value `57896044618658097711785492504343953926634992332820282019728792003956564819968` received in the input for the variable `amount` would trigger a Integer Overflow since it exceeds the maximum value supported.

An example: [Beauty Chain exploit](https://etherscan.io/tx/0xad89ff16fd1ebe3a0a7cf4ed282302c06626c1af33221ebe0d3a470aba4a660f). An input like `["<ADDR_1>","<ADDR_2>"], 0x8000000000000000000000000000000000000000000000000000000000000000` for the function `batchTransfer` would trigger this vulnerability.

**Integer Underflow** happens in the exact opposite of the overflow error. It error occurs when you go below the minimum amount. This triggers the system to bring you right back up to maximum value instead of reverting to zero. For example, injecting the value `-1` in a `uint256` variable that stores the value `0` will result in the number 255.

#### Remediation

To fix this vulnerability, and other integer overflows and underflows, the smart contract can import and use the [SafeMath library by OpenZeppelin](https://github.com/OpenZeppelin/openzeppelin-contracts).

```solidity
import "@openzeppelin/contracts/utils/math/SafeMath.sol";
```

**Note**: Since version `0.8.0` Solidity automatically reverts on integer overflow and underflow instead of circling the value back to zero.


### <ins>Re-entrancy attacks</ins>

A Reentrancy vulnerability is a type of attack to drain the bit-by-bit liquidity of a contract with an insecure code-writing pattern.

An incorrect flow looks like this:
- It verifies that the user has a sufficient balance to execute the transaction
- Sends the funds to the user
- If the operation is successful, the contract updates the user's balance

The problem arises when a contract invokes this operation instead of a user. This can create code that generates a loop, which means that an attacker can invoke the withdrawal function many times because it is the same balance that is checked as the initial value.

An example of a vulnerable function
```Solidity
function withdraw(uint withdrawAmount) public returns (uint) {
		require(withdrawAmount <= balances[msg.sender]);
		msg.sender.call.value(withdrawAmount)("");
		balances[msg.sender] -= withdrawAmount;
		return balances[msg.sender];
}
```

#### Remediation

Implement Checks Effects Interactions Pattern: A secure code-writing pattern that prevents an attacker from creating loops that allow him to re-enter the contract multiple times without blocking.

- Verify that the requirements are met before continuing the execution;
- Update balances and make changes before interacting with an external actor;
- Finally, after the transaction has been validated and the changes have been made, interactions with the external entity are allowed.

#### Resource

- [A Historical Collection of Reentrancy Attacks](https://github.com/pcaversaccio/reentrancy-attacks)


### <ins>Unchecked Return Values For Low Level Calls</ins>

The low level functions are one of Solidity's deeper features. They behave significantly differently from other Solidity functions in terms of handling mistakes, since they do not propagate and do not result in a complete reversal of the present execution. Such low-level calls' return values should always be verified, failing to do so might result in fail-opens and other undesirable results.

These functions are: `call()`, `callcode()`, `delegatecall()` and `send()`.

An example from [DAPS - TOP 10](https://dasp.co/#item-4):
1. A smart contract saves in a variable how much ether is left, for example `etherLeft`;
2. A call is used to send ether to a contract that does not have a `payable` function;
3. The EVM sets the return value to `false`;
4. The return's value is not checked by the contract and the variable `etherLeft` is not updated.

```Solidity
function withdraw(uint256 _amount) public {
	require(balances[msg.sender] >= _amount);
	balances[msg.sender] -= _amount;
	etherLeft -= _amount;
	msg.sender.send(_amount);
}
```

Real world scenario
- [King of Ether | Post-Mortem Investigation (Feb 2016)](https://www.kingoftheether.com/postmortem.html)
