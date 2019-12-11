# Getting Started

## Introduction to Convexity

Convexity is a Decentralized Put Options Protocol built on the Ethereum Blockchain. Convexity provides an easy interface to buy and sell put options. 

Put options work as insurance in traditional finance. Convexity allows options sellers to earn premiums on their collateral and options buyers to protect themselves against technical, financial and systemic risks that various DeFi projects face. These risks include hacks, bank runs, a DeFi crisis etc. 

This site will serve as a project overview for Convexity - explaining how it works, how to use it, and how to build on top of it. These docs are actively being worked on and more information will be added on an ongoing basis. 

Please join the \#dev room in the Opyn community [Discord](https://discord.gg/ugAv3SH) server; our team, and members of the community, look forward to helping you build an application on top of Opyn. Your questions help us improve, so please don't hesitate to ask if you can't find what you are looking for here. 

## Resources

* [Website](http://www.opyn.co/)
* [Whitepaper](https://drive.google.com/file/d/1YsrGBUpZoPvFLtcwkEYkxNhogWCU772D/view)
* Github
* Twitter
* Discord
* Email

## Example Use Case

Consider the case of a Compound User who wants insurance on their Dai locked in Compound. They fear Compound getting hacked or having a bank run. The insurance buyer pays the insurance provider some premium ahead of time to get access to oTokens. An example of an oToken is the ocDai token which protects the holder of the token from Jan 1 2020 to Jan 1 2021 against any technical or financial risks that Compound's cDai faces. In the case of a disaster, the holder of the oToken can turn in their oToken and their cDai and in exchange take the collateral locked in the Convexity Protocol by insurance providers. If there is no disaster, it is strictly worse for the holder of cDai to give up their cDai in exchange for collateral locked on the Convexity protocol, thus the insurance providers earn a premium on their collateral

## How it Works

The options 

How it works + link to whitepaper, discord, twitter, github, email, website

## Networks 

TODO: figure out how to make it a table

OptionsContractsABI

```text
[
    {
      "constant": true,
      "inputs": [
        {
          "name": "_token",
          "type": "address"
        }
      ],
      "name": "getExchange",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "spender",
          "type": "address"
        },
        {
          "name": "amount",
          "type": "uint256"
        }
      ],
      "name": "approve",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "totalSupply",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "sender",
          "type": "address"
        },
        {
          "name": "recipient",
          "type": "address"
        },
        {
          "name": "amount",
          "type": "uint256"
        }
      ],
      "name": "transferFrom",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "spender",
          "type": "address"
        },
        {
          "name": "addedValue",
          "type": "uint256"
        }
      ],
      "name": "increaseAllowance",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "optionsExchange",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "name": "repos",
      "outputs": [
        {
          "name": "collateral",
          "type": "uint256"
        },
        {
          "name": "putsOutstanding",
          "type": "uint256"
        },
        {
          "name": "owner",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "underlying",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "account",
          "type": "address"
        }
      ],
      "name": "balanceOf",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [],
      "name": "renounceOwnership",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "COMPOUND_ORACLE",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "owner",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "isOwner",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "spender",
          "type": "address"
        },
        {
          "name": "subtractedValue",
          "type": "uint256"
        }
      ],
      "name": "decreaseAllowance",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "recipient",
          "type": "address"
        },
        {
          "name": "amount",
          "type": "uint256"
        }
      ],
      "name": "transfer",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "strike",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "oTokenExchangeRate",
      "outputs": [
        {
          "name": "value",
          "type": "uint256"
        },
        {
          "name": "exponent",
          "type": "int32"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "strikePrice",
      "outputs": [
        {
          "name": "value",
          "type": "uint256"
        },
        {
          "name": "exponent",
          "type": "int32"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "UNISWAP_FACTORY",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "collateral",
      "outputs": [
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "collateralizationRatio",
      "outputs": [
        {
          "name": "value",
          "type": "uint256"
        },
        {
          "name": "exponent",
          "type": "int32"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "owner",
          "type": "address"
        },
        {
          "name": "spender",
          "type": "address"
        }
      ],
      "name": "allowance",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [],
      "name": "expiry",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "newOwner",
          "type": "address"
        }
      ],
      "name": "transferOwnership",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "inputs": [
        {
          "name": "_collateral",
          "type": "address"
        },
        {
          "name": "_collExp",
          "type": "int32"
        },
        {
          "name": "_underlying",
          "type": "address"
        },
        {
          "name": "_oTokenExchangeExp",
          "type": "int32"
        },
        {
          "name": "_strikePrice",
          "type": "uint256"
        },
        {
          "name": "_strikeExp",
          "type": "int32"
        },
        {
          "name": "_strike",
          "type": "address"
        },
        {
          "name": "_expiry",
          "type": "uint256"
        },
        {
          "name": "_optionsExchange",
          "type": "address"
        },
        {
          "name": "_windowSize",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "constructor"
    },
    {
      "payable": true,
      "stateMutability": "payable",
      "type": "fallback"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "repoOwner",
          "type": "address"
        }
      ],
      "name": "RepoOpened",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "amount",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "payer",
          "type": "address"
        }
      ],
      "name": "ETHCollateralAdded",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "amount",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "payer",
          "type": "address"
        }
      ],
      "name": "ERC20CollateralAdded",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "issuedTo",
          "type": "address"
        },
        {
          "indexed": false,
          "name": "oTokensIssued",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        }
      ],
      "name": "IssuedOTokens",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "amtCollateralToPay",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "liquidator",
          "type": "address"
        }
      ],
      "name": "Liquidate",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "amtUnderlyingToPay",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "amtCollateralToPay",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "exerciser",
          "type": "address"
        }
      ],
      "name": "Exercise",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "amtCollateralClaimed",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "amtUnderlyingClaimed",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "repoOwner",
          "type": "address"
        }
      ],
      "name": "ClaimedCollateral",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "oTokensBurned",
          "type": "uint256"
        }
      ],
      "name": "BurnOTokens",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "oldOwner",
          "type": "address"
        },
        {
          "indexed": false,
          "name": "newOwner",
          "type": "address"
        }
      ],
      "name": "TransferRepoOwnership",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": false,
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "amtRemoved",
          "type": "uint256"
        },
        {
          "indexed": false,
          "name": "repoOwner",
          "type": "address"
        }
      ],
      "name": "RemoveCollateral",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "name": "from",
          "type": "address"
        },
        {
          "indexed": true,
          "name": "to",
          "type": "address"
        },
        {
          "indexed": false,
          "name": "value",
          "type": "uint256"
        }
      ],
      "name": "Transfer",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "name": "owner",
          "type": "address"
        },
        {
          "indexed": true,
          "name": "spender",
          "type": "address"
        },
        {
          "indexed": false,
          "name": "value",
          "type": "uint256"
        }
      ],
      "name": "Approval",
      "type": "event"
    },
    {
      "anonymous": false,
      "inputs": [
        {
          "indexed": true,
          "name": "previousOwner",
          "type": "address"
        },
        {
          "indexed": true,
          "name": "newOwner",
          "type": "address"
        }
      ],
      "name": "OwnershipTransferred",
      "type": "event"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "_liquidationIncentive",
          "type": "uint256"
        },
        {
          "name": "_liquidationFactor",
          "type": "uint256"
        },
        {
          "name": "_liquidationFee",
          "type": "uint256"
        },
        {
          "name": "_transactionFee",
          "type": "uint256"
        },
        {
          "name": "_collateralizationRatio",
          "type": "uint256"
        }
      ],
      "name": "updateParameters",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "_address",
          "type": "address"
        }
      ],
      "name": "transferFee",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [],
      "name": "numRepos",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [],
      "name": "openRepo",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        }
      ],
      "name": "addETHCollateral",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": true,
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "amt",
          "type": "uint256"
        }
      ],
      "name": "addERC20Collateral",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "_oTokens",
          "type": "uint256"
        }
      ],
      "name": "exercise",
      "outputs": [],
      "payable": true,
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "numTokens",
          "type": "uint256"
        },
        {
          "name": "receiver",
          "type": "address"
        }
      ],
      "name": "issueOTokens",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "_owner",
          "type": "address"
        }
      ],
      "name": "getReposByOwner",
      "outputs": [
        {
          "name": "",
          "type": "uint256[]"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        }
      ],
      "name": "getRepoByIndex",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        },
        {
          "name": "",
          "type": "uint256"
        },
        {
          "name": "",
          "type": "address"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "_ierc20",
          "type": "address"
        }
      ],
      "name": "isETH",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "pure",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "amtToBurn",
          "type": "uint256"
        }
      ],
      "name": "burnOTokens",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "newOwner",
          "type": "address"
        }
      ],
      "name": "transferRepoOwnership",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "amtToRemove",
          "type": "uint256"
        }
      ],
      "name": "removeCollateral",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        }
      ],
      "name": "claimCollateral",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "_oTokens",
          "type": "uint256"
        }
      ],
      "name": "liquidate",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": true,
      "inputs": [
        {
          "name": "repoIndex",
          "type": "uint256"
        }
      ],
      "name": "isUnsafe",
      "outputs": [
        {
          "name": "",
          "type": "bool"
        }
      ],
      "payable": false,
      "stateMutability": "view",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "amtToCreate",
          "type": "uint256"
        },
        {
          "name": "receiver",
          "type": "address"
        }
      ],
      "name": "createETHCollateralOptionNewRepo",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": true,
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "amtToCreate",
          "type": "uint256"
        },
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "receiver",
          "type": "address"
        }
      ],
      "name": "createETHCollateralOption",
      "outputs": [],
      "payable": true,
      "stateMutability": "payable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "amtToCreate",
          "type": "uint256"
        },
        {
          "name": "amtCollateral",
          "type": "uint256"
        },
        {
          "name": "receiver",
          "type": "address"
        }
      ],
      "name": "createERC20CollateralOptionNewRepo",
      "outputs": [
        {
          "name": "",
          "type": "uint256"
        }
      ],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    },
    {
      "constant": false,
      "inputs": [
        {
          "name": "amtToCreate",
          "type": "uint256"
        },
        {
          "name": "amtCollateral",
          "type": "uint256"
        },
        {
          "name": "repoIndex",
          "type": "uint256"
        },
        {
          "name": "receiver",
          "type": "address"
        }
      ],
      "name": "createERC20CollateralOption",
      "outputs": [],
      "payable": false,
      "stateMutability": "nonpayable",
      "type": "function"
    }
  ]
```

* Rinkeby

| Contract | JSON | Address |
| :--- | :--- | :--- |
| Uniswap Exchange |  |  |
| Uniswap Factory |  | 0xf5D915570BC477f9B8D6C0E980aA81757A3AaC36 |
| Options Exchange |  |  |
| Dai |  |  |
| cDai |  |  |
| cUSDC |  |  |
| ocDai |  |  |
| oDai |  |  |
| ocUSDC |  |  |
| Options Factory |  |  |

* Mainnet
* link 

## Gas Costs 

## web3 version + solidity compiler version  

## Smart Contract Architecture 

## Glossary of Terms 



