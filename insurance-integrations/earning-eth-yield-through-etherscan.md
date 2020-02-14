# Earning ETH Yield through Etherscan

##  Earn ETH Yield by selling ocDai options through Etherscan

1. Go to the [_Read Contract Tab_](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed#readContract) on the [ocDai](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed) contract page.
2. In the read contract tab, search for the function `maxOTokensIssuable.`
3.  Pass in the amount on ETH you want to supply as collateral in wei. Note down how much collateral you want to supply. You can use this [ETH-to-we](http://eth-converter.com/)i converter to help.The result you get from this function is the maximum number of oTokens you can issue against your ETH. Note down this value as the `safeMaxNumberOfOTokens`.
4. This current minimum collateralization ratio is 160%, if you fall below this ratio, you could be liquidated. Hence, we strongly recommend creating fewer oTokens than the number that is shown to you. Choose your desired collateralization ratio &gt; 160%. If your desired collateralization ratio is 200%, then the `numOptions = (safeMaxNumberOfOTokens * 160) / 200` . Note down the `numOptions` that you want to create. 
5. Once you know the `numOptions` you want to create and the collateral you want to supply, switch over to the [_Write Contract Tab_](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed#writeContract).
   1. Ensure you connect your wallet to the etherscan page. 
6. If this is your _**first time creating**_ _**an option**_ **from the current account** search for the `CreateETHCollateralOption` function. 
   1. Fill out the `payableAmount` in ETH \(**not wei this time**, this is an Etherscan quirk\). 
   2. Fill out the `numOptions` with the value that you calculated based on your desired collateralization ratio in step 4.
   3. Fill out the address that you want to send the newly created options to in the receiver field. This is most likely your wallet address. 
7. If you have _**already created options from the current account**_ search for the `addETHCollateralOption` function. \(Not to be confused with `addETHCollateral`function\)
   1. Fill out the payableAmount in ETH \(**not wei this time**, this is an Etherscan quirk\). 
   2. Fill out the numOptions with the value that you calculated based on your desired collateralization ratio in step 4. 
   3. Fill out the address that you want to send the newly created options to in the receiver field. This is most likely your wallet address. 
8. Hit write and then confirm the transaction through your wallet. You have created the options! You can now either
   1.  [sell them on uniswap](https://uniswap.exchange/swap/0xddac4aed7c8f73032b388efe2c778fc194bc81ed) OR 
   2. [add them to the uniswap ocDai pool.](https://uniswap.exchange/add-liquidity) \(You will need to search for the oToken with the address below\). The ocDai address is here: [0xddac4aed7c8f73032b388efe2c778fc194bc81ed](https://etherscan.io/token/0xddac4aed7c8f73032b388efe2c778fc194bc81ed). 

## Earn ETH Yield by selling ocUSDC options through Etherscan

1. Go to the [_Read Contract Tab_](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#readContract) __on the [ocUSDC ](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4)

    contract page.

2. In the read contract tab, search for the function `maxOTokensIssuable.`
3.  Pass in the amount on ETH you want to supply as collateral in wei. Note down how much collateral you want to supply. You can use this [ETH-to-we](http://eth-converter.com/)i converter to help.The result you get from this function is the maximum number of oTokens you can issue against your ETH. Note down this value as the `safeMaxNumberOfOTokens`.
4. This current minimum collateralization ratio is 160%, if you fall below this ratio, you could be liquidated. Hence, we strongly recommend creating fewer oTokens than the number that is shown to you. Choose your desired collateralization ratio &gt; 160%. If your desired collateralization ratio is 200%, then the `numOptions = (safeMaxNumberOfOTokens * 160) / 200` . Note down the `numOptions` that you want to create. 
5. Once you know the `numOptions` you want to create and the collateral you want to supply, switch over to the [_Write Contract Tab_](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed#writeContract).
   1. Ensure you connect your wallet to the etherscan page. 
6. If this is your _**first time creating**_ _**an option**_ **from the current account** search for the `CreateETHCollateralOption` function. 
   1. Fill out the `payableAmount` in ETH \(**not wei this time**, this is an Etherscan quirk\). 
   2. Fill out the `numOptions` with the value that you calculated based on your desired collateralization ratio in step 4.
   3. Fill out the address that you want to send the newly created options to in the receiver field. This is most likely your wallet address. 
7. If you have _**already created options from the current account**_ search for the `addETHCollateralOption` function. \(Not to be confused with `addETHCollateral`function\)
   1. Fill out the payableAmount in ETH \(**not wei this time**, this is an Etherscan quirk\). 
   2. Fill out the numOptions with the value that you calculated based on your desired collateralization ratio in step 4. 
   3. Fill out the address that you want to send the newly created options to in the receiver field. This is most likely your wallet address. 
8. Hit write and then confirm the transaction through your wallet. You have created the options! You can now either
   1. [Sell them on uniswap](https://uniswap.exchange/swap/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4) OR 
   2. [Add them to the uniswap ocUSDC pool](https://uniswap.exchange/add-liquidity). \(You will need to search for the oToken with the address below\)The ocUSDC address is here: [0x8ed9f862363ffdfd3a07546e618214b6d59f03d4](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4)

