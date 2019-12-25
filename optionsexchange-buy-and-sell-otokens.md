# optionsExchange: Buy and Sell oTokens

## Introduction

The oTokens minted can be bought and sold through the optionsExchange contract. 

## Functions

### Buy oTokens

oTokens can be bought by calling the buy function. Before buying, you need to approve the optionsExchange contract to spend your money. oTokens can be bought and sold on an exchange like Uniswap at anytime before expiry.

```text
function buyOTokens(address payable receiver, address oTokenAddress, uint256 oTokensToBuy, address paymentTokenAddress) payable
```

> `receiver` : The account that will receive the oTokens
>
> `oTokenAddress` :  The address of the oToken that is being bought
>
> `oTokensToBuy` : The number of oTokens to buy
>
> `paymentTokenAddress` : The address of the token you are paying premiums in to buy the option tokens. Is it is set to 0, you can pay with ETH. 
>
> `msg.value` : If the payment Token is ETH, then the msg.value is the amount of ETH, else it is 0. 
>
> `msg.sender` : The account that is paying the premiums

```text
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);
paymentToken.approve(address(optionsExchange), 1000000000);
optionsExchange.buyOTokens(msg.sender, 0x3BF..., 100, address(paymentToken));
```

### Sell oTokens

oTokens can be sold by calling the sell function. Premiums are paid in any token of the seller's choice. oTokens can be sold at anytime before expiry on an Exchange like Uniswap. 

```text
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
```text
OptionsExchange optionsExchange = OptionsExchange(0x6B3...);
address(this).approve(address(optionsExchange), 1000000000);
optionsExchange.sellOTokens(0xFB4..., 0x3BF..., address(0), 100);
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

