# Insurance Buyer Integrations

## [Buy oTokens](../optionsexchange-buy-and-sell-otokens.md#buy-otokens) 

Insurance on any underlying asset can be bought by buying the respective oTokens. oTokens can be bought through the [buyOTokens](../optionsexchange-buy-and-sell-otokens.md#buy-otokens) function in the OptionsExchange smart contract. 

The amount of underlying that 1 oToken protects can be determined by calling the [oTokenExchangeRate](../otoken.md#otoken-exchange-rate) in the OToken smart contract.

| oToken | Amount Underlying Protected |
| :--- | :--- |
| 1 ocDai | 10 ^-5 cDai |
| 1 ocUSDC | 10^-5 cUSDC |
| 1 oDai | 10^-14 Dai |

## [Calculate premiums to pay](../optionsexchange-buy-and-sell-otokens.md#calculate-premiums-to-pay)

To buy insurance, the insurance buyer needs to pay some amount of premium upfront. The amount of payment tokens to be paid to buy the insurance can be calculated by calling the [premiumToPay](../optionsexchange-buy-and-sell-otokens.md#calculate-premiums-to-pay) function in the OptionsExchange smart contract. 

## [Exercise ](../otoken.md#exercise)

Once insurance has been bought, it is valid until the oToken contract expires. While the insurance is valid, if the insurance buyer thinks that there is an issue with the underlying system \(e.g. if Maker gets hacked or Compound has a liquidity crisis\), the oToken holder can make a claim and immediately get paid out by calling the [exercise](../otoken.md#exercise) function in the OToken smart contract. 

