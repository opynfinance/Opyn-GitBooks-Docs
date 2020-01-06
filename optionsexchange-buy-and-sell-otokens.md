# optionsExchange: Buy and Sell Options

## Introduction

The oTokens minted can be bought and sold through the optionsExchange contract. 

## State Changing Functions

### Buy oTokens

oTokens can be bought by calling the buy function. Before buying, you need to approve the optionsExchange contract to spend your money. oTokens can be bought and sold on an exchange like Uniswap at anytime before expiry.

The `buyOTokens` function is `payable` because it needs to be able to receive ETH as a `paymentToken`. 

```javascript
function buyOTokens(address payable receiver, address oTokenAddress, address paymentTokenAddress, uint256 oTokensToBuy) payable
```

> `receiver` : The account that will receive the oTokens. The receiver needs to be payable because if the holder of the oToken calls [exercise](otoken.md#exercise), then the claim payout may be in ETH. 
>
> `oTokenAddress` :  The [address of the oToken](abis-smart-contract-addresses.md#networks) that is being bought
>
> `paymentTokenAddress` : The address of the token you are paying for oTokens with. If it is set to 0, it means ETH. 
>
> `oTokensToBuy` : The number of oTokens to buy. See [oTokenExchangeRate](otoken.md#otoken-exchange-rate) for amount of underlying protected by 1 oToken.
>
> `msg.sender` : The account that is paying the premiums.
>
> `msg.value` \(optional\) : If the payment token is ETH, then the msg.value is the amount of ETH paid, else it is 0.

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);

/**
 * Need to approve any ERC20 before spending it. 
 * If paying in ETH, comment out line 7.
 */
paymentToken.approve(address(optionsExchange), 1000000000);

/**
 * receiver is the msg.sender
 * oTokenAddress is the oDai rinkeby address
 * paymentToken is an ERC20
 * 100 oDai protects 100 * 10^-14 Dai i.e. 10^-12 Dai. 
 */
optionsExchange.buyOTokens(msg.sender, 0x3BF..., address(paymentToken), 100);
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const optionsExchange = OptionsExchange.at(0x6B3...);

/**
 * Need to approve any ERC20 before spending it.
 * If paying in ETH, comment out lines 7 - 10.
 */
await paymentToken.methods.approve(
    optionsExchange.options.address,
    '1000000000000000000000000000000'
    ).send();

/**
 * receiver is myAccount
 * oTokenAddress is the oToken contract's address
 * paymentToken is an ERC20
 * 100 oDai protects 100 * 10^-14 Dai i.e. 10^-12 Dai. 
 */
await optionsExchange.methods.buyOTokens(
    myAccount, 
    oToken.options.address, 
    paymentToken.options.address, 
    '100').send();
```
{% endtab %}
{% endtabs %}

### Sell oTokens

oTokens can be sold by calling the sell function. Premiums are received in any token of the seller's choice. oTokens can be sold at anytime before expiry on an Exchange like Uniswap. 

```javascript
function sellOTokens(address payable receiver, address oTokenAddress, address payoutTokenAddress, uint256 oTokensToSell) 
```

> `receiver` : The account that will receive the premiums
>
> `oTokenAddress` :  The [address of the oToken ](abis-smart-contract-addresses.md)that is being sold
>
> `payoutTokenAddress` : The address of the token to receive premiums in. address\(0\) for ETH. 
>
> `oTokensToSell` : The number of oTokens sold
>
> `msg.sender` : The account that is supplying the oTokens to be sold.

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);
/**
 * Need to approve any ERC20 before spending it
 */
oToken.approve(address(optionsExchange), 1000000000);
optionsExchange.sellOTokens(0xFB4..., address(oToken), address(0), 100);
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const optionsExchange = OptionsExchange.at(0x6B3...);

/**
 * Need to approve any ERC20 before spending it
 */
await oToken.methods.approve(
    optionsExchange.options.address,
    '1000000000000000000000000000000'
    ).send();

await optionsExchange.methods.sellOTokens(
    myAccount, 
    oToken.options.address, 
    '0X0', 
    '100').send();
```
{% endtab %}
{% endtabs %}

## Read Only Functions

### Calculate Premiums To Pay

This function calculates the premiums to be paid if a buyer wants to buy oTokens on Uniswap. 

```javascript
function premiumToPay(address oTokenAddress, address paymentTokenAddress, uint256 oTokensToBuy) view returns (uint256)
```

> `oTokenAddress` :  The [address of the oToken](abis-smart-contract-addresses.md#networks) that is being bought
>
> `paymentTokenAddress` : The address of the token you are paying premiums in to buy the option tokens. Is it is set to 0, you can pay with ETH. 
>
> `oTokensToBuy` : The number of oTokens to buy
>
> `RETURN` : The amount of paymentToken to pay as premiums

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);
uint256 ethToPay = optionsExchange.premiumToPay(0x3BF..., address(0), 100);
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const optionsExchange = OptionsExchange.at('0x6B3...');
const ethToPay = optionsExchange.methods.premiumToPay('0x3BF...', '0x0', '100').call();
```
{% endtab %}
{% endtabs %}

### Calculate Premiums Received 

This function calculates the amount of premiums that the seller will receive if they sold oTokens on Uniswap.

```javascript
function premiumReceived(address oTokenAddress, address payoutTokenAddress, uint256 oTokensToSell) view returns (uint256) 
```

> `oTokenAddress` :  The [address of the oToken](abis-smart-contract-addresses.md#networks) that is being sold
>
> `payoutTokenAddress` : The address of the token to receive premiums in. address\(0\) for ETH. 
>
> `oTokensToSell` : The number of oTokens sold
>
> `RETURN` : The amount of payoutToken that the seller will receive

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);
uint256 ethReceived = optionsExchange.premiumReceived(0x3BF..., address(0), 100);
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const optionsExchange = OptionsExchange.at('0x6B3...');
const ethToPay = optionsExchange.methods.premiumReceived('0x3BF...', '0x0', '100').call();
```
{% endtab %}
{% endtabs %}

