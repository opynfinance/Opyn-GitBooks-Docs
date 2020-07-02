# FAQ

Opyn is a decentralized insurance platform built on Ethereum that allows users to protect themselves from the unique risks they face in DeFi. Opyn is built using Convexity Protocol \([convexity.opyn.co](http://convexity.opyn.co/)\), a generalizable options protocol that allows DeFi users to create put and call options. Anyone can buy options \(oTokens\) to protect themselves against DeFi risks. Users can also deposit collateral in a vault to mint and sell oTokens, earning premiums for protecting others.  
  
Opyn currently allows users to insure Compound deposits, hedging ETH downside with protective put options on ETH, and hedge ETH upside with calls options on ETH. Opyn's smart contracts have been audited by [OpenZeppelin](https://blog.openzeppelin.com/opyn-contracts-audit/).‌ If you have any additional questions not covered below, or want to learn more, join the [Opyn Discord](https://discord.gg/2NFdXaE) or email us at [hello@opyn.co](mailto:hello@opyn.co).‌

## Buying Protection 

### **What protection do you currently offer?**

* ‌ETH downside and upside protection allowing you to protect yourself against ETH price movements, flash crashes, and volatility 
* COMP downside protection allowing you to protect yourself against COMP price movements, flash crashes, and volatility
* Protection for USDC and DAI deposits on Compound 

### **How is protection priced?**

Currently, oTokens are bought and sold using [Uniswap](https://uniswap.exchange/), and pricing is determined by the market price of oTokens on Uniswap. Therefore, pricing is completely decentralized as it is market determined based on the supply and demand of oTokens at any given point in time. ‌

### **What risks are covered?**

**ETH Protection** 

* Opyn’s ETH downside protection \(put options\) gives you the right to sell your ETH for the strike price at anytime, thus mitigating your downside. You can also sell your oTokens in the case of falling ETH price. [This blog](https://medium.com/@aparnalocked/all-about-the-op-sh-yn-part-1-bf26dfea13ee) dives into further detail.
* Opyn's ETH upside protection \(call options\) gives you the right to buy ETH for the strike price at anytime. You can also sell your oTokens in the case of rising ETH price. [This blog ](https://medium.com/opyn/hedging-with-calls-6a1a8f77eb66)dives into further detail on hedging with upside protection. 

**COMP Protection**

* Opyn’s COMP downside protection \(put options\) gives you the right to sell your COMP for the strike price at anytime, thus mitigating your downside. You can also sell your oTokens in the case of falling COMP price. [This blog](https://medium.com/@aparnalocked/all-about-the-op-sh-yn-part-1-bf26dfea13ee) dives into further detail.

**Compound Deposit Protection**

* Opyn’s Compound protection protects against a number of different risks:

  * Technical risks \(eg. smart contracts hacks\)
  * Financial risks \(eg. liquidity crises\)
  * Admin risks \(eg. admin key compromise, governance vulnerabilities\)

* Opyn’s Compound protection does not protect against

  * Issues with Compound's ETH:USD oracle and Maker's ETH:USD oracle
  * Non-transferable ERC20 tokens

* We are actively working on increasing the surface of risks we can cover for future iterations of the protocol.

### **How do claims / exercise work?**

**ETH Downside Protection \(Put Options\)**

* If ETH is below the strike price you purchased your protection at you can exercise at anytime to receive that strike price amount per USDC. For example if you purchased a put option with a strike price of $150, if ETH is below $150, exercise to receive 150 USDC per ETH. You could also choose to sell your oETHp instead of exercising. [This blog](https://medium.com/@aparnalocked/all-about-the-op-sh-yn-part-1-bf26dfea13ee) dives into further detail about selling vs. exercising. 
* There is no auto-exercise. You must come and exercise yourself up until expiry. You can currently exercise from [opyn.co](http://opyn.co/), [opynmonitor.xyz](https://opynmonitor.xyz/#/myvaults/), or [etherscan](https://opyn.gitbook.io/opyn/making-a-claim-through-etherscan). You cannot exercise after expiry.

**ETH Upside Protection \(Call Options\)**

* If ETH is above the strike price you purchased your protection at you can exercise at anytime to buy ETH at that strike price. For example if you purchased a call option with a strike price of $150, if ETH is above $150, exercise to receive 1 ETH per 150 USDC. You could also choose to sell your oETHc instead of exercising. 
* There is no auto-exercise. You must come and exercise yourself up until expiry. You can currently exercise from [opyn.co](http://opyn.co/), [opynmonitor.xyz](https://opynmonitor.xyz/#/myvaults/), or [etherscan](https://opyn.gitbook.io/opyn/making-a-claim-through-etherscan). You cannot exercise after expiry.

**Compound** 

If there is an issue with your Compound deposit, you can make a claim at any time to receive immediate payout.‌Here’s what’s automatically happening in the background:‌

1. Send

    ****a. ****You are sending your cUSDC / cDAI on Compound, which is no longer worth it’s full value due to the hack / financial crisis, to the protocol  
    b. You are sending your insurance tokens \(ocUSDC / ocDAI\) back to the protocol

2. Receive a. You immediately receive your protection payout in ETH

### **Who is providing protection?**

‌Opyn is built as a two sided marketplace, so any individuals interested in putting down collateral and earning a premium can provide protection. 

ETH downside protection \(put options\) are collateralized with USDC, and each option is fully collateralized.

ETH upside protection \(calls options\) are collateralized with ETH, and each option is fully collateralized.

COMP downside protection \(put options\) are collateralized with USDC, and each option is fully collateralized.

Compound deposit protection is collateralized with ETH, and these positions are overcollateralized with the minimum collateralization ratio of 140%, meaning that there is at least $1.40 locked up for each $1 of insurance coverage.‌

### What is "Max Loss" for Compound protection?

‌The "max loss" is the maximum loss you can face on the position that you are covering. The rest is covered by your policy. For example, if you are insuring 1000 DAI and the Max Loss is 20 DAI, then in the case of an adverse event if you max a claim, you will receive $980 of ETH.

## Earning Premiums by Providing Protection

### **How can I earn premiums?**

**ETH Put Options**  
You can earn premiums by selling protective put options on ETH. You are putting down USDC collateral and then minting oTokens \(options\). You can then sell your oTokens on Uniswap and immediately earn a premium. ‌You receive the premium in ETH.

**ETH Call Options**  
You can earn premiums by selling call options on ETH. You are putting down ETH collateral and then minting oTokens \(options\). You can then sell your oTokens on Uniswap and immediately earn a premium. You receive the premium in ETH.

**COMP Put Options**   
You can earn premiums by selling protective put options on COMP. You are putting down USDC collateral and then minting oTokens \(options\). You can then sell your oTokens on Uniswap and immediately earn a premium. ‌You receive the premium in ETH.

**Compound Deposit Protection**  
You can earn ETH premiums by providing protection. In the background, you are supplying ETH as collateral and then minting oTokens \(insurance tokens\). Then you have have two possibilities to earn money on their ETH. They can either sell oTokens to protection buyers on Uniswap and earn premiums or add oTokens to the Uniswap Pool and earn transaction fees from other users' trading activity.

![](https://gblobscdn.gitbook.com/assets%2F-Lt35Xmux_Lnb0dHwjOb%2F-M18JPszFVTJNDfh_34e%2F-M18Jho1TyECIHTwryUM%2FInitial%20Flow%20Infographic.png?alt=media&token=296669d6-c04c-4bd5-8dd4-2b520f7d714f)

### **What does the return profile look like for selling ETH put options?**‌

When you sell ETH put options, you immediately earn a premium. If ETH hits the strike price, you may be exercised on in which case you give up your USDC collateral to option buyers and receive the option buyers’ ETH in return. If ETH does not hit the strike price, then upon expiry you can remove your USDC collateral, keeping all of your collateral in addition to the premium you earned. You can also close out your position by buying back and burning the amount of oETHp you sold. 

### **What does the return profile look like for selling ETH call options?**‌ <a id="what-does-the-return-profile-look-like-for-selling-eth-put-options"></a>

When you sell ETH call options, you immediately earn a premium. If ETH hits the strike price, you may be exercised on in which case you give up your ETH collateral to option buyers and receive the option buyers’ USDC in return. If ETH does not hit the strike price, then upon expiry you can remove your ETH collateral, keeping all of your collateral in addition to the premium you earned. You can also close out your position by buying back and burning the amount of oETHc you sold.

### **What does the return profile look like for selling COMP put options?‌**

When you sell COMP put options, you immediately earn a premium. If COMP hits the strike price, you may be exercised on in which case you give up your USDC collateral to option buyers and receive the option buyers’ COMP in return. If COMP does not hit the strike price, then upon expiry you can remove your USDC collateral, keeping all of your collateral in addition to the premium you earned. You can also close out your position by buying back and burning the amount of oCOMP you sold.

### **What does the return profile look like for selling Compound deposit protection?**‌

[**Selling oTokens on Uniswap**](https://uniswap.exchange/swap?inputCurrency=0x98cc3bd6af1880fcfda17ac477b2f612980e5e33)**:** Selling oTokens to protection buyers on Uniswap allows you to earn premiums on your ETH that far outshine anything you can get currently in DeFi \([currently](https://compound.finance/markets) [0.01% on Compound](https://compound.finance/markets), [0.05% on dYdX](https://trade.dydx.exchange/balances)\), and you will get the entirety of it back as long as you remain above 1.4x collateralized for Compound positions \(otherwise you are at risk of liquidation\) and there isn’t some disaster event \(eg. technical risk like a hack, financial risk like DAI breaking its peg or a run on Compound\). Here you’re taking a similar risk to depositing ETH on Compound, where you earn 0.01% and are exposed to Compound risk. With Opyn, you are exposed to Compound risk and Opyn risk, but earn a significantly higher premium on ETH.‌

### **What are the risks with earning premiums by providing protection?**

**ETH Put Options**   
If the option buyer exercises, you could lose some or all of your USDC collateral. However you would receive the option buyer’s ETH in return. 

**ETH Call Options**   
If the option buyer exercises, you could lose some or all of your ETH collateral. However you would receive the option buyer’s USDC in return. 

**Compound**   
You can currently provide protection for the following on Compound: 

* USDC on Compound \(cUSDC\) - exposing you to USDC, Compound, and Opyn risk
* DAI on Compound \(cDAI\) - exposing you to Maker, Compound, and Opyn risk.

In the case that there is an adverse event affecting the protocols you are exposed to, you may lose some or all of your collateral.‌

### **When could I get liquidated?**

For providing Compound protection you are required to maintain a minimum collateral ratio of 140%. If you fall below this threshold, you are at risk of liquidation.  
  
For providing ETH and COMP downside protection \(put options\) you are not at risk of liquidation since you are collateralizing in USDC. ‌For providing ETH upside protection \(call options\) you are not at risk of liquidation since you are collateralizing with the exact amount of ETH a buyer expects upon exercise.

### Can I liquidate people?

‌Yes, you can check out Opyn's [example liquidator bot here](https://github.com/opynfinance/LiquidatorBot).‌

### **What if I want to close my position before the expiry date?**

You can close your position at any time by buying back the oTokens you had sold on Uniswap and returning them to your vault, which would allow you to redeem your collateral \(ETH for providing Compound protection or selling ETH calls, USDC for selling ETH or COMP puts\). One note is that the price of oTokens could have increased or decreased in the time since you first purchased them. ‌

![](https://paper-attachments.dropbox.com/s_5034B4C62D9D3BC72EFD16F592EDFDCF70907B0703EE1E0E5187016183963F55_1590355976158_Unwinding+Vault+-+Twitter+2.png)

### **What happens in the case of an adverse event?**

In the case of an adverse event, protection buyers can make a claim by sending their oTokens and protected asset to the protocol. Protection providers then pay out protection buyers in the collateral they put down and receive the protected asset.   
  
**For ETH put options**

* Protection buyer exercises by sending ETH and oETHp to the protocol 
* Protection seller gives up USDC collateral and receives protection buyer’s ETH

**For ETH call options**

* Protection buyer exercises by sending USDC and oETHc to the protocol 
* Protection seller gives up ETH collateral and receives protection buyer’s USDC

**For COMP put options**

* Protection buyer exercises by sending COMP and oCOMPp to the protocol 
* Protection seller gives up USDC collateral and receives protection buyer’s ETH

**For Compound protection** 

* Protection buyer claims by sending cDAI or cUSDC and ocDAI or ocUSDC to the protocol 
* Protection seller gives up ETH collateral and receives protection buyer’s cDAI or cUSDC

![](https://paper-attachments.dropbox.com/s_5034B4C62D9D3BC72EFD16F592EDFDCF70907B0703EE1E0E5187016183963F55_1590355985080_Paying+out+in+hack+-+Twitter.png)

## Integrating your DApp

### Can I provide protection for my users?

‌Yes! You can allow your users to access Compound deposit insurance or ETH protection directly through your DApp by integrating with the protocol. You can explore the [documentation here](https://opyn.gitbook.io/opyn/insurance-integrations/insurance-buyer-integrations) and chat with us on [Discord](https://discord.gg/2NFdXaE) :\)‌

### Can I create my own oTokens?

‌Absolutely! The Opyn Convexity protocol is an open protocol that allows anyone to create oTokens and interfaces on top. We encourage the community to bootstrap markets and interfaces. You can get started with bootstrapping your own marketplace [here](https://opyn.gitbook.io/opyn/options-factory) and chat with us on [Discord](https://discord.gg/2NFdXaE) :\) As an example, the [iearn.finance](https://iearn.finance/cover) team created a market for [y.curve.fi](https://y.curve.fi/) \(oCRV\) and they host that interface as well.‌

## Under the hood

### What is the Convexity Protocol?

‌The Convexity Protocol is the first generalizable, on-chain options protocol on Ethereum. Opyn provides insurance using the Convexity Protocol's protective put options. You can access the convexity protocol whitepaper at [convexity.opyn.co](http://convexity.opyn.co/) and can access the [smart contracts here](https://opyn.gitbook.io/opyn/abis-smart-contract-addresses).‌

### Can I build on top of the Convexity Protocol?

‌Yes! [Here's a list of some ideas](https://medium.com/opyn/buidling-with-options-otokens-in-defi-cfd7539c6eef). We are excited to see the all the different applications people will explore with on-chain options. You can find the [documentation here](https://opyn.gitbook.io/opyn/) and chat with us on [Discord](https://discord.gg/2NFdXaE) :\)‌

### What are oTokens?

‌oTokens are ERC20 tokens that represent the insurance \(protective put option\) that you have bought or sold. Compound protection and ETH put option oTokens correspond to one unit of the insured asset. Eg. 1 ocUSDC protects 1 cUSDC, 1 oETHp protects 1 ETH‌

### What is the call options multiplier? 

The way call options are currently implemented in the protocol 1 oETHc call does not correspond to 1 ETH the way it does for put options. Currently there is a multiplier based on the strike price. For example, for a 250 strike call, 250 oETHc calls would correspond to 1 ETH. We're working on changing this for v2 of the protocol. 

### Which oTokens are currently available?

**Compound Protection:** 

| Name | Underlying Asset | Collateral Asset | Strike Price | Expiry |
| :--- | :--- | :--- | :--- | :--- |
| [ocDAI](https://etherscan.io/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33) | [cDAI](https://etherscan.io/token/0x5d3a536E4D6DbD6114cc1Ead35777bAB948E3643) | ETH | $0.01859 | 02/10/2021 |
| [ocDAI](https://etherscan.io/token/0xddac4aed7c8f73032b388efe2c778fc194bc81ed) [\(old\)](https://etherscan.io/token/0xddac4aed7c8f73032b388efe2c778fc194bc81ed) | [cDAI](https://etherscan.io/token/0x5d3a536E4D6DbD6114cc1Ead35777bAB948E3643) | ETH | $0.02 | 02/10/2021 |
| [ocUSDC](https://etherscan.io/token/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4) | [cUSDC](https://etherscan.io/token/0x39aa39c021dfbae8fac545936693ac917d5e7563) | ETH | $0.0208 | 02/10/2021 |

**ETH Protection:** You can find all the ETH put options available along with their strike prices and expiries, [here](https://opyn.gitbook.io/opyn/abis-smart-contract-addresses). 

### Why are there two ocDAI contracts currently?

‌We initially launched with ocDAI and ocUSDC. However, the parameters of ocDAI contract we initially launched with resulted in market prices for insurance of around 10%+, which is too expensive to fulfill the needs of insurance buyers. To mitigate this, we launched an ocDAI contract with adjusted parameters, which has led to rates for insurance of around 2-4% for ocDAI.‌  
  
Specifically, the original strike price for the first ocDAI contract was $0.985 in terms of DAI \($0.02 in terms of cDAI\), however DAI often fluctuates to $0.985 without there being an adverse event, making these contracts prohibitively expensive for insurance buyers. The strike price for the second ocDAI contract is $0.92 \($0.01859 in terms of cDAI\) which gives insurance buyers comprehensive coverage against adverse events with Maker and Compound at a reasonable premium.‌If you purchased insurance on the old ocDAI contract you do not need to take any action. You are still protected.‌

## Security

### Is Opyn safe? Has it been audited? 

‌The security of the Opyn protocol is our highest priority. We understand that especially since we ourselves are a smart contract platform, security is paramount. Our team has created a protocol that we believe is safe and dependable, and has been audited by OpenZeppelin. All smart contract code is publicly verifiable. You can find the [OpenZeppelin audit report here](https://blog.openzeppelin.com/opyn-contracts-audit/) and you can find our [bug bounty here](https://opyn.gitbook.io/opyn/security). 

### What if there is a bug in Opyn’s smart contracts?

‌We recognize that this is a risk, and we have taken precautions to protect against this risk with rigorous internal testing and [external audits](https://blog.openzeppelin.com/opyn-contracts-audit/).‌ Even with this risk, you can still gain significant safety from Opyn protection. With Opyn protection, you can only lose your Compound deposits in the case that both Opyn and Compound are compromised at the same time. For example, if the probability that Opyn is compromised is 1% and the probability that Compound is compromised is 1%, then with Opyn insurance, your risk of losing your funds drops to 0.01%.‌

### How do the price feeds work?

‌Opyn currently uses Compound’s ETH:USD oracle for Compound deposit protection.   
  
ETH and COMP put options \(USDC collateralized\), and ETH calls options \(ETH collateralized\) are 100% collateralized and do not require any oracle. 

### Does the Convexity Protocol have an administrator?

‌There is currently a protocol admin, but our goal is to remove the protocol admin and become fully decentralized.‌The admin can update option parameters within specific bounds that limit its control \(eg. cannot lower minimum collateralization ratio below 100%\), manage the asset whitelist, and set the name / symbol of tokens.‌The admin CANNOT access any user funds - Opyn is completely noncustodial.‌

### Help! I can’t access Opyn!

‌Opyn’s smart contracts are on the Ethereum blockchain and are thus always available. If Metamask, or the [Opyn](http://opyn.co/) interface are unavailable, you can always [access Opyn through the smart contracts.](https://opyn.gitbook.io/opyn/abis-smart-contract-addresses) You can also buy and sell oTokens on [Uniswap v1](https://v1.uniswap.exchange/) and you can check out [OpynMonitor](http://opynmonitor.xyz/), a community built interface.  

## Roadmap 

### When do you release new oTokens? 

We currently release new at the money ETH protective put options with two week expiries each week. We also post a bi-weekly poll on our [discord](http://tiny.cc/opyndiscord) where the community can vote on more experimental oTokens to launch. We will be supporting this schedule for the next quarter.  

### What are you working on next? 

We are currently working on Opyn v2 and looking into different exchange venues for oTokens. Join [\#research](https://paper.dropbox.com/?q=%23research) on our [discord](http://tiny.cc/opyndiscord) to join the conversation!

## Learning resources 

### Do you have a tutorial on how to use the opyn.co interface? 

DeFi rate made a great tutorial on how to buy and sell ETH protective put options using opyn.co, which you can find [here](https://defirate.com/opyn-cover-tutorial/). 

### Where can I learn more about options? 

Here are some great resources to learn more about options! 

* [Khan Academy ](https://www.khanacademy.org/economics-finance-domain/core-finance/derivative-securities)
* [OptionAlpha](https://optionalpha.com/members/video-tutorials/options-basics) 
* [Investopedia](https://www.investopedia.com/options-basics-tutorial-4583012) 

There are also lots of great conversations on our [discord](http://tiny.cc/opyndiscord), and we’re happy to answer any questions :\) 

