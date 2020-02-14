# Earning ETH Yield through Etherscan

##  Earn ETH Yield by selling ocDai options

1. Go to the [_Read Contract Tab_](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed#readContract) on the [ocDai](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed) contract page.
2. In the read contract tab, search for the function `maxOTokensIssuable.`
3.  Pass in the amount on ETH you want to supply as collateral in wei. Note down how much collateral you want to supply. You can use this [ETH-to-we](http://eth-converter.com/)i converter to help.The result you get from this function is the maximum number of oTokens you can issue against your ETH. Note down this value as the `safeMaxNumberOfOptions`.
4. This current minimum collateralization ratio is 160%, if you fall below this ratio, you could be liquidated. Hence, I strongly recommend creating less options than the number that is shown to you. Choose your desired collateralization ration &gt; 160%. if your desired collateralization ratio is 200%, then the `numOptions = (safeMaxNumberOfOptions * 160) / 200` . Note down the `numOptions` that you want to create. 
5. Once you know the `numOptions` you want to create and the collateral you want to supply, switch over to the [_Write Contract Tab_](https://etherscan.io/address/0xddac4aed7c8f73032b388efe2c778fc194bc81ed#writeContract).
   1. Ensure you connect your wallet to the etherscan page. 
6. If this is your _**first time creating**_ _**an option**_ **from the current account** search for the `CreateETHCollateralOption` function. 
   1. Fill out the payableAmount in ETH \(**not wei**, this is an Etherscan quirk\). 
   2. Fill out the numOptions with the value that you calculated based on your desired collateralization ratio.
   3. Fill out the address that you want to send the newly created options to in the receiver field.
7. If you have _**already created options from the current account**_ search for the `addETHCollateralOption` function. 
   1. Fill out the payableAmount in ETH \(**not wei**, this is an Etherscan quirk\). 
   2. Fill out the numOptions with the value that you calculated based on your desired collateralization ratio.
   3. Fill out the address that you want to send the newly created options to in the receiver field.
8. And that is all! hit confirm and you have created the options. You can now either [sell them on uniswap](https://uniswap.exchange/) OR [add them to the uniswap ocDai pool.](https://uniswap.exchange/add-liquidity)
   1. The ocDai address is here: [https://etherscan.io/token/0xddac4aed7c8f73032b388efe2c778fc194bc81ed](https://etherscan.io/token/0xddac4aed7c8f73032b388efe2c778fc194bc81ed)

## Earn ETH Yield by selling ocUSDC options

1. Go to the [_Read Contract Tab_](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#readContract) on the [ocUSDC ](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4)contract page.
2. In the read contract tab, search for the function `maxOTokensIssuable.`
3.  Pass in the amount on ETH you want to supply as collateral in wei. Note down how much collateral you want to supply. You can use this [ETH-to-we](http://eth-converter.com/)i converter to help.The result you get from this function is the maximum number of oTokens you can issue against your ETH. Note down this value as the `safeMaxNumberOfOptions`.
4. This current minimum collateralization ratio is 160%, if you fall below this ratio, you could be liquidated. Hence, I strongly recommend creating less options than the number that is shown to you. Choose your desired collateralization ration &gt; 160%. if your desired collateralization ratio is 200%, then the `numOptions = (safeMaxNumberOfOptions * 160) / 200` . Note down the `numOptions` that you want to create. 
5. Once you know the `numOptions` you want to create and the collateral you want to supply, switch over to the [_Write Contract Tab_.](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#writeContract)
   1. Ensure you connect your wallet to the etherscan page. 
6. If this is your _**first time creating**_ _**an option**_ **from the current account** search for the `CreateETHCollateralOption` function. 
   1. Fill out the payableAmount in ETH \(**not wei**, this is an Etherscan quirk\). 
   2. Fill out the numOptions with the value that you calculated based on your desired collateralization ratio.
   3. Fill out the address that you want to send the newly created options to in the receiver field.
7. If you have _**already created options from the current account**_ search for the `addETHCollateralOption` function. 
   1. Fill out the payableAmount in ETH \(**not wei**, this is an Etherscan quirk\). 
   2. Fill out the numOptions with the value that you calculated based on your desired collateralization ratio.
   3. Fill out the address that you want to send the newly created options to in the receiver field.
8. And that is all! hit confirm and you have created the options. You can now either [sell them on uniswap](https://uniswap.exchange/) OR [add them to the uniswap ocUSDC pool](https://uniswap.exchange/add-liquidity). 
   1. The ocUSDC address is here:[https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4)

