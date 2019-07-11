# Cron 

[![Build Status](https://travis-ci.com/carlos-buendia/cron-solidity.svg?token=DJeMzxJJncp3nRaEUuxH&branch=develop)](https://travis-ci.com/carlos-buendia/cron-solidity)
[![codecov](https://codecov.io/gh/Frontier-project/cron/branch/master/graph/badge.svg?token=BGbU5Q6IRV)](https://codecov.io/gh/Frontier-project/cron)



## About

The repo provides tools enabing to divide time in epochs on Ethereum Smart Contracts, through onchain "clocks". Clocks are single contracts following a common interface (`ICron.sol`), and registered in the Crontab.eth registry.


## Motivation

Decoupling the scheduling logic from the Smart Contract developer has the following benefits:

 * **Interoperability**: By decoupling the scheduling logic, Smart Contracts and oracles can easily sync their clocks.
 * **Programability**: Most Smart Contracts develop their own arithmetic rules every time they want to schedule periodic changes. The complexity of coding an arbitrarily complex rule may prevent the developer to include it
 * **Security**: Relaying all programable logic to a single trusted source.
 
 ## Structure
 
![image](https://i.ibb.co/vLN4K5L/Untitled-Diagram-42.png)


## Using it

#### 1. Install

Download the last state of `solidity-cron`

```bash
npm init -y
npm i -E solidity-cron
```

#### 2. Deploying a new cron

Every cron deployed must include the `ICron.sol` interface. 

While a Crontab expression compiler is WI

[./contracts/calendar](https://github.com/carlos-buendia/solidity-cron/tree/develop/contracts/calendar)


#### 3. Use it

```javascript
import "solidity-cron/contracts/ICron.sol";
Cron c = ICron(monthly)
uint256 height =  c.height();
```


## Testing

You can always use the truffle package to test and contribute to the library. The package needs from a running Ethereum rpc instance in `localhost`, port `8545`. You can run a [ganache-cli](https://github.com/trufflesuite/ganache-cli) instance or run [geth](https://github.com/ethereum/go-ethereum). You can run the tests by just running:

```bash
truffle test
```


## Contributing

The project is open to contributions, just open a PR! We follow Angular [Git Commit guidelines](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#-git-commit-guidelines), to follow `semantic-release`versioning.

