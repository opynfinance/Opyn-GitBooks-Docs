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

### Integrating as an Insurance Provider 

**Quickstart relevant sections:**

* [Create and Sell oTokens](otoken.md#eth-collateralized-options-2)
* [Calculate premiums received](optionsexchange-buy-and-sell-otokens.md#calculate-premiums-received)
* [Add Collateral](otoken.md#add-eth-collateral)
* [Claim Collateral](otoken.md#claim-collateral)

## Example Use Case: Insurance on Compound

Consider the case of a Compound user, person A, who wants insurance on their Dai locked in Compound. They fear Compound getting hacked or having a bank run. The insurance buyer, person A, pays the insurance provider, person B,  0.01 ETH premium ahead of time to get access to ocDai tokens. In return, person B, locks up 1 ETH of collateral on the insurance platform. 

The ocDai token protects the holder of the token from Jan 1 2020 to Jan 1 2021 against any technical or financial risks that Compound's cDai faces. In the case of a disaster, the holder of the ocDai, person A, can turn in their oTokens and their cDai and in exchange take out $1 worth of collateral locked in the Convexity Protocol by insurance providers. If there is no disaster, it is strictly worse for the holder of cDai to give up their cDai in exchange for collateral locked on the Convexity protocol. In such a case, the insurance provider, person B, keeps their collateral and earns a premium on it. 

