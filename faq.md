# FAQ

Opyn is building the insurance layer for DeFi. This is the first platform protecting users in DeFi against both technical and financial risks, starting with Compound deposit insurance. The platform is a two-sided marketplace designed using put options on the Convexity Protocol \(convexity.opyn.co\). Opyn also allows ETH holders to earn meaningful premiums on their ETH holdings by providing insurance.

  
If you have any additional questions not covered below, or want to learn more, join the [Opyn Discord](https://discord.gg/2NFdXaE) or email us at [hello@opyn.co](mailto:hello@opyn.co).

## Buying Insurance

### **What DeFi protocols do you currently cover?** 

Opyn currently provides deposit insurance for Compound, specifically DAI and USDC deposits. Based on your [feedback](mailto:hello@opyn.co), we’re looking forward to adding insurance for additional protocols.

### **How is insurance priced?** 

Since insurance contracts are tokenized as oTokens, pricing is determined by the market price of oTokens on Uniswap. Therefore, pricing is completely decentralized as it is market determined based on the supply and demand of insurance at any given point in time.

In the background, insurance is bought and sold using [Uniswap](https://uniswap.exchange/). 

### **What risks are covered?**  

Opyn provides protection against a number of different risks:

* Technical risks \(eg. smart contracts hacks\)
* Financial risks \(eg. liquidity crises\)
* Admin key risks \(eg. admin key compromise\)

Opyn protects against all oracle manipulation with the exception of Compound's ETH:USD oracle, which is used in the protocol. Opyn currently does not protect against non-transferable ERC20s token. We are actively working on increasing the surface of risks we can cover for future iterations of the protocol.

### **How do claims work?** 

If there is an issue with your Compound deposit, you can make a claim at any time to receive immediate payout.

Here’s what’s automatically happening in the background: 

1. Send 

   a. You are sending your USDC/DAI on Compound, which is no longer worth it’s full value due to the hack / financial crisis, to the protocol 

   b. You are sending your insurance tokens back to the protocol 

2. Receive 

   a. You immediately receive your insurance payout in ETH  

### **Who is providing insurance?**  

Opyn is built as a two sided marketplace, so any individuals interested in putting down ETH collateral and earning a premium can provide insurance. These positions are overcollateralized with the minimum collateralization ratio of 160%, meaning that there is at least $1.60 locked up for each $1 of insurance coverage. 

### What is "Max Loss"? 

The "max loss" is the maximum loss you can face on the position that you are covering. The rest is covered by your policy. For example, if you are insuring 1000 DAI and the Max Loss is 20 DAI, then in the case of an adverse event if you max a claim, you will receive $980 of ETH. 

## Earning ETH Yield 

### **How can I earn ETH yields?** 

You can earn ETH yield by providing insurance. In the background, you are supplying ETH as collateral and then minting and selling oTokens \(insurance tokens\). 

You can currently supply ETH and provide insurance using [Opyn’s APIs](https://opyn.gitbook.io/opyn/). An interface for this process is coming soon.

### **Why are their different rates I can choose from?** 

Each rate corresponds to a different set of risks. Generally higher yields imply higher risks.

### **What are the risks with earning ETH yield by providing insurance?** 

Initially you can choose to earn a yield for providing insurance for the following: 

* USDC on Compound - exposing you to USDC, Compound, and Opyn risk 
* DAI on Compound - exposing you to Maker, Compound, and Opyn risk. 

In the case that there is an adverse event affecting the protocols you are exposed to, you may lose some or all of your collateral. 

### **When could I get liquidated?** 

You are required to maintain a minimum collateral ratio of 160%. If you fall below this threshold, you are at risk of liquidation.

### Can I liquidate people? 

Yes, you can check out Opyn's [example liquidator bot here](https://github.com/opynfinance/LiquidatorBot). 

## Integrating your DApp 

### Can I provide insurance for my users? 

Yes! You can allow your users to access Compound deposit insurance directly through your DApp by integrating with the protocol. You can explore the [documentation here](https://opyn.gitbook.io/opyn/insurance-integrations/insurance-buyer-integrations) and chat with us on [Discord](https://discord.gg/2NFdXaE) :\) 

## Under the hood 

### What is the Convexity Protocol? 

The Convexity Protocol is the first generalizable, on-chain options protocol on Ethereum. Opyn provides insurance using the Convexity Protocol's protective put options. You can access the convexity protocol whitepaper at [convexity.opyn.co](http://convexity.opyn.co/) and can access the [smart contracts here](https://opyn.gitbook.io/opyn/abis-smart-contract-addresses). 

### Can I build on top of the Convexity Protocol? 

Yes! We are excited to see the all the different applications people will explore with on-chain options. You can find the [documentation here](https://opyn.gitbook.io/opyn/) and chat with us on [Discord](https://discord.gg/2NFdXaE) :\) 

### What are oTokens? 

oTokens are ERC20 tokens that represent the insurance \(protective put option\) that you have bought or sold. Each oToken corresponds to one unit of the insured asset. Eg. 1 oUSDC protects 1 USDC on Compound 

## Security 

### Is Opyn safe? Has it been audited? Can you cover Opyn yourselves? 

The security of the Opyn protocol is our highest priority. We cannot cover Opyn ourselves. We understand that especially since we ourselves are a smart contract platform, security is paramount. Our team has created a protocol that we believe is safe and dependable, and has been audited by OpenZeppelin. All smart contract code is publicly verifiable. We will also be launching a bug bounty in the coming weeks. You can find the [OpenZeppelin audit report here](https://blog.openzeppelin.com/opyn-contracts-audit/).

### What if there is a bug in Opyn’s smart contracts? 

We recognize that this is a risk, and we have taken precautions to protect against this risk with rigorous internal testing and [external audits](https://blog.openzeppelin.com/opyn-contracts-audit/).   
Even with this risk, you can still gain significant safety from Opyn insurance. With Opyn insurance, you can only lose your Compound deposits in the case that both Opyn and Compound are compromised at the same time. For example, if the probability that Opyn is compromised is 1% and the probability that Compound is compromised is 1%, then with Opyn insurance, your risk of losing your funds drops to 0.01%. 

### How do the price feeds work? 

Opyn currently uses Compound’s ETH:USD oracle. We are actively working on increasing the protocol’s oracle resilience. 

### Does the Convexity Protocol have an administrator? 

There is currently a protocol admin, but our goal is to remove the protocol admin and become fully decentralized. 

The admin can update option parameters within specific bounds that limit its control \(eg. cannot lower minimum collateralization ratio below 160%\), manage the asset whitelist, and set the name / symbol of tokens. 

The admin CANNOT access any user funds - Opyn is completely noncustodial. 

### Help! I can’t access Opyn! 

Opyn’s smart contracts are on the Ethereum blockchain and are thus always available. If Metamask, or the Opyn interface are unavailable, you can always [access Opyn through the smart contracts. ](https://opyn.gitbook.io/opyn/abis-smart-contract-addresses)

