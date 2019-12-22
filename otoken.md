# oToken: Integrate with existing insurance markets

## Introduction

Opyn uses options to provide insurance. Every option supported by the Convexity Protocol is integrated through an oToken smart contract which is an [EIP-20](https://eips.ethereum.org/EIPS/eip-20) compliant representation of options issued by the protocol. Options sellers create options by locking up collateral for some period of time and minting oTokens. Each oToken protects a unit of the specified underlying ERC20 asset. The Options seller can sell these oTokens on an exchange to earn premiums. The oToken marketplaces deployed for the purpose of insurance are oDai, ocDai and ocUSDC. 

The main functionality offered by the convexity protocol is as below:

1. Create oTokens
2. Keep the oToken repos sufficiently collateralized
3. Liquidate the undercollateralized repos
4. Exercise the oTokens during the expiry window

## Functions 

### **Open Vault**

The open vault function creates an empty vault and sets the owner of the vault to be the msg.sender. The collateral and the outstanding puts issued of the vault are set to 0. 

```javascript
function openVault() returns (uint)
```

> `msg.sender`: The account that shall be the owner of the vault
>
> `RETURN`: The index of the vault opened

{% tabs %}
{% tab title="Solidity" %}
```javascript
oToken ocDai = oToken(0x3BA...);
uint256 vaultIndex = ocDai.openVault();
```
{% endtab %}

{% tab title="Web3" %}
```javascript

```
{% endtab %}
{% endtabs %}

### Add Collateral

The add collateral functions serve two purposes. The first is to add collateral to a new vault. A vault needs to meet the minimum collateral requirements before it is safe for the owner to mint oTokens.The second purpose is to top up i.e. turn a vault that is unsafe because it doesn't meet the minimum collateral requirements into a vault that is safe. The add collateral functions can be called at any point before the oToken's expiry. 

#### Add ETH Collateral

The `addETHCollateral()` function is called if the specified collateral for the oToken contract is ETH. This function call will fail if the collateral type is not ETH. The collateral for the oDai, ocDai and ocUSDC options markets are all ETH. 

```javascript
function addETHCollateral(uint256 vaultIndex) payable returns (uint256) 
```

> `vaultIndex` : The index of the vault to add collateral to
>
> `msg.sender` : The account from which ETH collateral will be transferred into the oToken contract
>
> `msg.value` : The amount of ETH to add
>
> `RETURN` :

{% tabs %}
{% tab title="Solidity" %}
```javascript
oToken ocDai = oToken(0x3BA...);
uint256 vaultCollateralBalance = ocDai.addETHCollateral(1)(1000000);
```
{% endtab %}

{% tab title="Web3" %}
```javascript

```
{% endtab %}
{% endtabs %}

#### Add ERC20 Collateral

The `addERC20Collateral()` function is called if the specified collateral for the oToken contract is any ERC20 asset. The function will only add the specified collateral asset. It will fail if called on any other asset other than the pre specified collateral asset. 

```javascript
function addERC20Collateral(uint256 vaultIndex, uint256 amt) returns (uint256)
```

> `vaultIndex` : The index of the vault to add collateral to
>
> `amt` : The amount of collateral tokens to add
>
> `msg.sender` : The account from which the ERC20 collateral asset will be transferred into the oToken contract
>
> `RETURN` :

{% tabs %}
{% tab title="Solidity" %}
```javascript
oToken ocDai = oToken(0x3BA...);
/** 
 * the spender needs to approve the oToken contract to spend 
 * their ERC20Collateral because they are transferring collateral 
 * tokens to the oToken contract. 
 */
ERC20Collateral.approve(ocDai, 1000000000000000000000000000000);
uint256 vaultCollateralBalance = ocDai.addERC20Collateral(1, 100000000);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

### Issue oTokens

The issue oTokens functionality allows the vault owner to mint new options in the form of oTokens. These oTokens are ERC-20 tokens and are fungible within a specific series. Different series of oTokens are not fungible with each other. 

To mint oTokens, the vault that the tokens are being minted from must meet the `minCollateralizationRatio` requirements \(TODO: Link explanation\). Further, only the owner of a vault can mint oTokens. 

```javascript
function issueOTokens (uint256 vaultIndex, uint256 oTokensToIssue, address receiver)
```

> `vaultIndex`: The index of the vault to issue oTokens from
>
> `oTokensToIssue`: The amount of oTokens to issue
>
> `receiver`: The address that the newly minted oTokens will be sent to
>
> `msg.sender` : The account that is the owner of the vault that is issuing the oTokens

{% tabs %}
{% tab title="Solidity" %}
```javascript
oToken ocDai = oToken(0x3BA...);
ocDai.issueOTokens(1, 1000, 0xFB3...);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

### Burn oTokens

The burn oTokens functionality allows a vault owner to reduce the amount of insurance that they have provided by bringing back oTokens to the oTokens smart contract. By burning oTokens, a vault owner increases the ratio of collateral to oTokens Issued i.e. the vault's collateralization ratio, thus making the vault safer. 

A vault owner can burn oTokens any time before expiry of the oToken contract. 

```javascript
function burnOTokens(uint256 vaultIndex, uint256 amtToBurn)
```

> `vaultIndex` : The index of the vault that will be affected by burning oTokens 
>
> `amtToBurn` : The amount of oTokens to burn
>
> `msg.sender` : The owner of the vault and the account from which oTokens will be burned

{% tabs %}
{% tab title="Solidity" %}
```javascript
oToken ocDai = oToken(0x3BA...);
/** 
 * the spender needs to approve the oToken contract to spend 
 * their oTokens because they are transferring oTokens 
 * to the oToken contract. 
 */
ocDai.approve(ocDai, 1000000000000000000000000000000);
ocDai.burnOTokens(1, 100);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

### Liquidate

A vault that fails to meet the minimum collateralization requirement is subject to liquidation by other users of the protocol, to return the vault back to a safe state. 

When a liquidation occurs, a liquidator may return some or all of the outstanding oTokens issued on behalf of a vault owner and in return receive a discounted amount of collateral held by the vault owner; this discount is defined as the liquidation incentive. 

A liquidator may close up to a certain fixed percentage \(i.e. liquidation factor\) of the outstanding oTokens issued by the unsafe vault. 

```javascript
function liquidate(uint256 vaultIndex, uint256 oTokensToLiquidate)
```

> `vaultIndex` : The index of the vault that is unsafe and is to be liquidated
>
> `oTokensToLiqudate` : The amount of oTokens that the liquidator brings back to the oToken contract
>
> `msg.sender` : The account from which oTokens will be transferred into the oToken contract. The collateral along with a liquidation incentive will also be paid out to this account.

{% tabs %}
{% tab title="Solidity" %}
```javascript
oToken ocDai = oToken(0x3BA...);

/** 
 * the spender needs to approve the oToken contract to spend 
 * their oTokens because they are transferring oTokens 
 * to the oToken contract. 
 */
ocDai.approve(ocDai, 1000000000000000000000000000000);
ocDai.liquidate(1, 10);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

### Exercise

During the exercise window, any oToken holders can transfer their oTokens and corresponding amount of underlying tokens and in return get out strike price amount of the collateral asset per unit of oToken exercised. 

To determine if it is the exercise window, call `isExerciseWindow()`. Exercise can only be called during the exercise window. 

The amount of underlying tokens to be transferred can be calculated by calling the `underlyingToTransfer(uint256 oTokensToExercise)` function. Users first need to approve the oToken contract before they can liquidate a vault because they are transferring in the ERC20 oTokens and underlying tokens into the oToken contract. 

While exercise can be called at anytime during the exercise window, it may be unprofitable to exercise unless there was an actual crash in the price of the underlying asset. The function `isProfitableToExercise()` will return true if the price of the underlying asset has crashed below the strike price of the smart contract. We recommend using this function only as a proxy to provide context to users rather than as a necessary pre-condition to exercising because it relies on on-chain oracles which may not be reflective of actual prices. Furthermore, there might be times when the price of the underlying asset may not have moved, but there might be a liquidity crisis on other platforms which prevents users from accessing their funds on the other platforms, and hence an exercise would be beneficial. For a higher degree of accuracy, we recommend using a combination of off-chain price feeds to determine if it is profitable to exercise. 

```javascript
function exercise(uint256 oTokensToExercise) payable
```

> `oTokensToExercise` : The amount of oTokens being exercised
>
> `msg.sender` : The amount of

## Events 

## Error Table





