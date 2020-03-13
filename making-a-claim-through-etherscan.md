---
description: >-
  A step-by-step guide on how to make claims if you purchased protection through
  Opyn.
---

# Making a Claim through Etherscan

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
* Pass in the amount of ocDAI you want got in step 4, the vault you want to exercise from \(you can find all vaults and their respective collateral amounts [here](https://antoncoding.github.io/opyn-liquidator/#/)\), we recommend `insert our vault` at time of writing. Egs call: 
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
* Pass in the amount of ocUSDC you want got in step 4, the vault you want to exercise from \(you can find all vaults and their respective collateral amounts [here](https://antoncoding.github.io/opyn-liquidator/#/)\), we recommend `insert our vault` at time of writing.Egs call: 
  * payableAmount = `0`
  * oTokensToExercise = `the value you got from balance in step 4`
  * vaults to exercise from = `[0x9e68B67660c223B3E0634D851F5DF821E0E17D84]`

