# Insurance Seller Integrations

## Create and Sell Insurance

The [`createAndSellEthCollateralOption(..)`](../otoken.md#eth-collateralized-options-2) function allows the seller to create new oTokens \(the holder of the oTokens has insurance\), and sell those oTokens on uniswap. 

Create oToken allows the Open Vault + Add Collateral + Issue oTokens calls to be made in one step. Issue oTokens mints new oTokens only if a given vault has sufficient collateral. 

The amount of underlying that 1 oToken protects can be determined by calling the [`oTokenExchangeRate(..)`](../otoken.md#otoken-exchange-rate)in the OToken smart contract.

| oToken | Amount Underlying Protected |
| :--- | :--- |
| 1 ocDai | 10 ^-8 cDai |
| 1 ocUSDC | 10^-8 cUSDC |
| 1 oDai | 10^-14 Dai |

## [Calculate premiums received](../optionsexchange-buy-and-sell-otokens.md#calculate-premiums-received)

## [Add Collateral](../otoken.md#add-eth-collateral)

## [Claim Collateral](../otoken.md#claim-collateral)

