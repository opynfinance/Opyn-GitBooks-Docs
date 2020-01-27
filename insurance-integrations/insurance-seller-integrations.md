# Insurance Provider Integrations

## Create and Sell Insurance

The [`createAndSellEthCollateralOption(..)`](../otoken.md#eth-collateralized-options-2) function allows the seller to create new oTokens \(the holder of the oTokens has insurance\), and sell those oTokens on uniswap. 

The amount of underlying that 1 oToken protects can be determined by calling the [`oTokenExchangeRate(..)`](../otoken.md#otoken-exchange-rate)in the OToken smart contract.

| oToken | Amount Underlying Protected |
| :--- | :--- |
| 1 ocDai | 10 ^-8 cDai |
| 1 ocUSDC | 10^-8 cUSDC |
| 1 oDai | 10^-14 Dai |

Create oToken allows the Open Vault + Add Collateral + Issue oTokens calls to be made in one step. Issue oTokens mints new oTokens only if a given vault has sufficient collateral. 

## Calculate Premiums Received

The premiums earned from selling insurance can be calculated by calling the function [`premiumReceived(..)`](../optionsexchange-buy-and-sell-otokens.md#calculate-premiums-received) in the OptionsExchange contract. 

## Ensure sufficient collateral backs all insurance sold 

To ensure that the oToken contract always has never sold more insurance than it can pay, each insurance seller needs to ensure that their positions are sufficiently collateralized. They can meet the minimum collateralization requirements by calling the [`addETHCollateral(..)`](../otoken.md#add-eth-collateral) or [`burnOTokens(..)`](../otoken.md#burn-otokens) functions. 

## Redeem Collateral

After the insurance has expired, the insurance provider can take out all the collateral that they put down. If insurance claims were made during the insurance lifetime, the insurance provider may not be able to redeem all of their collateral. The insurance provider can take out their collateral by calling the [`claimCollateral(..)`](../otoken.md#claim-collateral) function. 

