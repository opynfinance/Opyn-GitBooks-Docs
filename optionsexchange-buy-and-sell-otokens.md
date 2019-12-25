# optionsExchange: Buy and Sell oTokens

## Introduction

The oTokens minted can be bought and sold through the optionsExchange contract. 

## State Changing Functions

### Buy oTokens

oTokens can be bought by calling the buy function. Before buying, you need to approve the optionsExchange contract to spend your money. oTokens can be bought and sold on an exchange like Uniswap at anytime before expiry.

```javascript
function buyOTokens(address payable receiver, address oTokenAddress, address paymentTokenAddress, uint256 oTokensToBuy) payable
```

> `receiver` : The account that will receive the oTokens
>
> `oTokenAddress` :  The address of the oToken that is being bought

> `paymentTokenAddress` : The address of the token you are paying premiums in to buy the option tokens. Is it is set to 0, you can pay with ETH. 
>
> `oTokensToBuy` : The number of oTokens to buy
>
> `msg.value` : If the payment Token is ETH, then the msg.value is the amount of ETH paid, else it is 0. 
>
> `msg.sender` : The account that is paying the premiums

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);
/**
 * Need to approve any ERC20 before spending it
 */
paymentToken.approve(address(optionsExchange), 1000000000);
optionsExchange.buyOTokens(msg.sender, 0x3BF..., address(paymentToken), 100);
```
{% endtab %}

{% tab title="Web3" %}
```

```
{% endtab %}
{% endtabs %}

### Sell oTokens

oTokens can be sold by calling the sell function. Premiums are paid in any token of the seller's choice. oTokens can be sold at anytime before expiry on an Exchange like Uniswap. 

```javascript
function sellOTokens(address payable receiver, address oTokenAddress, address payoutTokenAddress, uint256 oTokensToSell) 
```

> `receiver` : The account that will receive the premiums
>
> `oTokenAddress` :  The address of the oToken that is being sold
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
address(this).approve(address(optionsExchange), 1000000000);
optionsExchange.sellOTokens(0xFB4..., 0x3BF..., address(0), 100);
```
{% endtab %}

{% tab title="Web3" %}
```

```
{% endtab %}
{% endtabs %}

## Read Only Functions

### Calculate Premiums To Pay

This function calculates the premiums to be paid if a buyer wants to buy oTokens on Uniswap. 

```javascript
function premiumToPay(address oTokenAddress, address paymentTokenAddress, uint256 oTokensToBuy) view returns (uint256)
```

> `oTokenAddress` :  The address of the oToken that is being bought
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

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

### Calculate Premiums Received 

This function calculates the amount of premiums that the seller will receive if they sold oTokens on Uniswap.

```javascript
function premiumReceived(address oTokenAddress, address payoutTokenAddress, uint256 oTokensToSell) view returns (uint256) 
```

> `oTokenAddress` :  The address of the oToken that is being sold
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

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

