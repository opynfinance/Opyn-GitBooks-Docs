# Insurance Provider Integrations

## Create and Sell Insurance

The [`createAndSellEthCollateralOption(..)`](../otoken.md#eth-collateralized-options-2) function allows the seller to create new oTokens \(the holder of the oTokens has insurance\), and sell those oTokens on uniswap. 

The amount of underlying that 1 oToken protects can be determined by calling the [`oTokenExchangeRate(..)`](../otoken.md#otoken-exchange-rate)in the OToken smart contract.



| oToken | Amount Underlying Protected | Decimals for oToken | Smallest Unit protected |
| :--- | :--- | :--- | :--- |
| 1 ocDai | 1 cDai | 8 | 10^-8 cDai |
| 1 ocUSDC | 1 cUSDC | 8 | 10^-8 cUSDC |

Create oToken allows the Open Vault + Add Collateral + Issue oTokens calls to be made in one step. Issue oTokens mints new oTokens only if a given vault has sufficient collateral. 

## Calculate Premiums Received

The premiums earned from selling insurance can be calculated by calling the function [`premiumReceived(..)`](../optionsexchange-buy-and-sell-otokens.md#calculate-premiums-received) in the OptionsExchange contract. 

## Ensure sufficient collateral backs all insurance sold 

To ensure that the oToken contract always has never sold more insurance than it can pay, each insurance seller needs to ensure that their positions are sufficiently collateralized. They can meet the minimum collateralization requirements by calling the [`addETHCollateral(..)`](../otoken.md#add-eth-collateral) or [`burnOTokens(..)`](../otoken.md#burn-otokens) functions. 

## Redeem Collateral and Underlying

After the insurance has expired, the insurance provider can take out all the collateral that they put down. If insurance claims were made during the insurance lifetime, the insurance provider may not be able to redeem all of their collateral. The insurance provider can take out their collateral by calling the [`redeemVaultBalance(..)`](../otoken.md#redeem-vault-balance) function. 

The [`removeUnderlying(..)`](../otoken.md#remove-underlying) function allows the underlying balance of the vault to be removed at anytime. The vault only gets an underlying balance if an exercise event affects the vault. 

