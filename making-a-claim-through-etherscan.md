---
description: >-
  A step-by-step guide on how to make claims if you purchased protection through
  Opyn.
---

# Making a Claim \(Exercising\) through Etherscan

## Exercising oETH  

### 1. Go to the [_Write_ _Contract Tab_](https://etherscan.io/address/0x48ab8a7d3bf2eb942e153e4275ae1a8988238dc7#writeContract) on the oETH contract page.

### 2. Approve the contract to transfer your oETH

* In the [write contract tab](https://etherscan.io/address/0x48ab8a7d3bf2eb942e153e4275ae1a8988238dc7#writeContract), search for the function`approve​`
* Pass in the oETH address `0x48AB8A7d3Bf2EB942e153e4275Ae1a8988238dC7`

  and an amount in WEI to approve the contract to transfer. We recommend `1000000000000000000000000000000`

* Click _write_ and confirm the transaction through your wallet. 

### 3. Get your oETH balance 

* In the [read contract tab](https://etherscan.io/address/0x48ab8a7d3bf2eb942e153e4275ae1a8988238dc7#readContract), search for the function `balance` 
* Pass in your `address` 
* Click _query_ and you'll see how many oETH you have

### 4. Call the Exercise function 

* In the [write contract tab](https://etherscan.io/address/0x48ab8a7d3bf2eb942e153e4275ae1a8988238dc7#writeContract), search for the function`exercise`
* Pass in the amount of oETH you want got in step 3, the vault you want to exercise from \(you can find all vaults and their respective collateral amounts [here](https://antoncoding.github.io/opyn-liquidator/#/option/0x48ab8a7d3bf2eb942e153e4275ae1a8988238dc7)\). For example:
  * payableAmount = `0`
  * oTokensToExercise = `the value you got from balance in step 3`
  * vaults to exercise from = `[0x076c95c6cd2eb823acc6347fdf5b3dd9b83511e4]`

## Making ocDAI claims 

### 1. Go to the [_Write_ _Contract Tab_](https://etherscan.io/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33#writeContract) on the ocDAI contract page.

### 2. Approve the contract to transfer your ocDAI

* In the [write contract tab](https://etherscan.io/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33#writeContract), search for the function`approve​`
* Pass in the ocDAI address `0x98cc3bd6af1880fcfda17ac477b2f612980e5e33`

  and an amount in WEI to approve the contract to transfer. We recommend `1000000000000000000000000000000`

* Click _write_ and confirm the transaction through your wallet. 

### 3. Approve the contract to spend your cDAI

* In the [write contract tab](https://etherscan.io/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33#writeContract), search for the function`approve​`
* Pass in the ocDAI address 

  `0x98cc3bd6af1880fcfda17ac477b2f612980e5e33`

   and an amount in WEI to approve the contract to transfer. We recommend `1000000000000000000000000000000`

* Click _write_ and confirm the transaction through your wallet. 

### 4. Get your ocDAI balance 

* In the [read contract tab](https://etherscan.io/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33#readContract), search for the function `balance` 
* Pass in your `address` 
* Click _query_ and you'll see how many ocDAI you have

### 5. Call the Exercise function 

* In the [write contract tab](https://etherscan.io/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33#writeContract), search for the function`exercise`
* Pass in the amount of ocDAI you want got in step 4, the vault you want to exercise from \(you can find all vaults and their respective collateral amounts [here](https://antoncoding.github.io/opyn-liquidator/#/token/0x98cc3bd6af1880fcfda17ac477b2f612980e5e33)\). For example:
  * payableAmount = `0`
  * oTokensToExercise = `the value you got from balance in step 4`
  * vaults to exercise from = `[0x9e68B67660c223B3E0634D851F5DF821E0E17D84]`

## Making ocUSDC claims 

### 1. Go to the [_Write_ _Contract Tab_](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#writeContract) on the ocUSDC contract page.

### 2. Approve the contract to transfer your ocUSDC

* In the [write contract tab](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#writeContract), search for the function`approve​`
* Pass in the ocUSDC address `0x8ED9f862363fFdFD3a07546e618214b6D59F03d4`

  and an amount in WEI to approve the contract to transfer. We recommend `1000000000000000000000000000000`

* Click _write_ and confirm the transaction through your wallet. 

### 3. Approve the contract to spend your cUSDC

* In the [write contract tab](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#writeContract), search for the function`approve​`
* Pass in the cUSDC address `0x8ED9f862363fFdFD3a07546e618214b6D59F03d4`

   and an amount in WEI to approve the contract to transfer. We recommend `1000000000000000000000000000000`

* Click _write_ and confirm the transaction through your wallet. 

### 4. Get your ocUSDC balance 

* In the [read contract tab](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#readContract), search for the function `balance` 
* Pass in your `address` 
* Click _query_ and you'll see how many ocUSDC you have

### 5. Call the Exercise function 

* In the [write contract tab](https://etherscan.io/address/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4#writeContract), search for the function`exercise`
* Pass in the amount of ocUSDC you want got in step 4, the vault you want to exercise from \(you can find all vaults and their respective collateral amounts [here](https://antoncoding.github.io/opyn-liquidator/#/token/0x8ed9f862363ffdfd3a07546e618214b6d59f03d4)\). For example:
  * payableAmount = `0`
  * oTokensToExercise = `the value you got from balance in step 4`
  * vaults to exercise from = `[0x9e68B67660c223B3E0634D851F5DF821E0E17D84]`

