# Getting Started

## Introduction to Convexity

Convexity is a a generalized options protocol built on the Ethereum Blockchain that allows DeFi users to create call as well as put options. Convexity provides an easy interface to buy and sell options. 

Put options work as insurance in traditional finance. A put option gives the buyer the right to sell a set stock at a specified price on or before a set date. This means that no matter how low a stock goes, the investor has the right to sell the stock for the agreed upon price. Convexity uses put options to allows option buyers to have insurance on their Dai and their assets on Compound \(Dai and USDC\). 

Convexity allows options sellers to earn premiums on their collateral and options buyers to protect themselves against technical, financial and systemic risks that various DeFi projects face. These risks include hacks, bank runs, a DeFi crisis etc. 

Please join the \#dev room in the Opyn community [Discord](https://discord.gg/ugAv3SH) server; our team, and members of the community, look forward to helping you build an application on top of Opyn. Your questions help us improve, so please don't hesitate to ask if you can't find what you are looking for here. 

## Resources

* [Website](http://www.opyn.co/)
* [Whitepaper](https://drive.google.com/file/d/1YsrGBUpZoPvFLtcwkEYkxNhogWCU772D/view)
* [Github](https://github.com/aparnakr/OptionsProtocol)
* [Twitter](https://twitter.com/opyn_)
* [Discord](https://discordapp.com/invite/2NFdXaE)
* [Email](mailto:hello@opyn.co)

### Integrating for Insurance Buyers

**Quickstart relevant sections :**

* [Buy oTokens](optionsexchange-buy-and-sell-otokens.md#buy-otokens)
* [Calculate premiums to pay](optionsexchange-buy-and-sell-otokens.md#calculate-premiums-to-pay)
* [Exercise ](otoken.md#exercise)
* [oTokenExchangeRate](otoken.md#otoken-exchange-rate)

### Integrating for Insurance Providers 

**Quickstart relevant sections:**

* [Create and Sell oTokens](otoken.md#eth-collateralized-options-2)
* [Calculate premiums received](optionsexchange-buy-and-sell-otokens.md#calculate-premiums-received)
* [Add Collateral](otoken.md#add-eth-collateral)
* [Claim Collateral](otoken.md#claim-collateral)

## Insurance Markets:

**The main use case of the options markets seeded on the convexity protocol is to provide insurance.**

Every option supported by the Convexity Protocol is integrated through an oToken smart contract which is an [EIP-20](https://eips.ethereum.org/EIPS/eip-20) compliant representation of options issued by the protocol. The insurance markets that exist are as below:

| oToken | Underlying Protected |
| :--- | :--- |
| [ocDai](abis-smart-contract-addresses.md) | [cDai](abis-smart-contract-addresses.md) |
| [ocUSDC](abis-smart-contract-addresses.md) | [cUSDC](abis-smart-contract-addresses.md) |
| [oDai](abis-smart-contract-addresses.md) | [Dai](abis-smart-contract-addresses.md) |

## Example Use Case 1: Insurance on Compound

Consider the case of a Compound user, _Afraid_, who wants insurance on his $1 worth of Dai locked in Compound. He fears Compound getting hacked or having a liquidity crisis where the reserves left on Compound are insufficient to pay out all the suppliers if they all tried to withdraw their money. The insurance buyer, _Afraid,_ pays the insurance provider, _Brave_,  0.02 ETH premium ahead of time to get access to ocDai tokens. In return, _Brave_, locks up 1 ETH of collateral on the insurance platform for 1 year. 

The ocDai token protects _Afraid_ from Jan 1 2020 to Jan 1 2021 against any technical or financial risks that Compound's cDai faces. The ocDai token gives _Afraid_ the right but not the obligation to sell his cDai for $1 worth of collateral at any time during the next 1 year. 

In the case of a disaster _Afraid_ can turn in his ocDai and his cDai and in exchange take out $1 worth of collateral locked in the Convexity Protocol by all the insurance providers. There is no need for claim assessors to determine if a disaster happened because if the price of cDai ever falls below $1, _Afraid_ can immediately[ exercise](protocol-overview/glossary-of-terms.md) his right to sell his cDai for $1. 

If there is no disaster, it is strictly worse for _Afraid_ to give up his cDai \(worth slightly &gt; $1 because of interest earned\) in exchange for \($1 worth\) collateral locked on the Convexity protocol. When there is no disaster, the insurance provider, _Brave_, keeps her collateral and earns a premium on it. 

## Example Use Case 2: Insurance on Dai

Consider the case of a Dai holder, _Afraid_, who wants insurance on his $1 worth of Dai. He fears Dai losing its peg or getting hacked. The insurance buyer, _Afraid,_ pays the insurance provider, _Brave_,  0.02 ETH premium ahead of time to get access to oDai tokens. In return, _Brave_, locks up 1 ETH of collateral on the insurance platform for 1 year. 

The oDai token protects _Afraid_ from Jan 1 2020 to Jan 1 2021 against any technical or financial risks that Compound's cDai faces. The oDai token gives _Afraid_ the right but not the obligation to sell his Dai for $0.9 worth of collateral at any time during the next 1 year. 

In the case of a disaster _Afraid_ can turn in his oDai and his Dai and in exchange take out $0.9 worth of collateral locked in the Convexity Protocol by all the insurance providers. There is no need for claim assessors to determine if a disaster happened because if the price of Dai ever falls below $0.9, _Afraid_ can immediately[ exercise](protocol-overview/glossary-of-terms.md) his right to sell his Dai for $0.9. 

If there is no disaster, it is strictly worse for _Afraid_ to give up his Dai \(worth $1\) in exchange for \($0.9 worth\) collateral locked on the Convexity protocol. When there is no disaster, the insurance provider, _Brave_, keeps her collateral and earns a premium on it. 

