# OptionsFactory: Bootstrap new Options Markets

## Functions 

### Create Options Contract 

The create options contract function creates a new options contract \(series\) as per the below parameters. 

```javascript
function createOptionsContract(
        string memory _collateralType,
        string memory _underlyingType,
        uint256 _strikePrice,
        string memory _strikeAsset,
        string memory _payoutType,
        uint256 _expiry
    )
        public
        returns (address)
```

> `string memory _collateralType`: The collateral asset \(eg. ETH, USDC, etc.\) 
>
> `string memory _underlyingType`: The asset upon which the option is based. In the insurance use case, the asset that is being protected. \(eg. DAI, cUSDC, etc.\) 
>
> `uint256 _strikePrice`: The amount of the strike asset that will be paid out upon exercise \(eg. 1\)
>
> `string memory _strikeAsset`: The asset in which the option is denominated. \(eg. DAI option denominated in USDC\)
>
> `string memory _payoutType`: The asset in which the option is paid out. \(eg. ETH\)
>
> `uint256 _expiry`: The unix time at which the option expires \(eg. 1574457816\)
>
> `RETURN` : The address of the options contract on success

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsFactory factory = OptionsFactory(0xABCD...);
address optionContract = factory.createOptionsContract(
                                "ETH",
                                "DAI",
                                "USDC", 
                                1,
                                "USDC", 
                                "ETH",  
                                1574457816
)
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const factory = await OptionsFactory.at('0xABCD...');
const optionContract = await factory.methods.createOptionsContract(
                                "ETH",
                                "DAI",
                                "USDC", 
                                '1',
                                "USDC", 
                                "ETH",  
                                '1574457816'
).send();
```
{% endtab %}
{% endtabs %}

### Get Number of Options Contracts

Provides the number of options contracts created

```javascript
function getNumberOfOptionsContracts() public view returns (uint256)
```

> `RETURN:` The number of options contracts created on success

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsFactory factory = OptionsFactory(0xABCD...);
uint256 numContracts = factory.getNumberOfOptionsContracts();
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const factory = await OptionsFactory.at('0xABCD...');
const numContracts = await factory.methods.getNumberOfOptionsContracts().call();
```
{% endtab %}
{% endtabs %}

### Supports Asset 

Checks whether an asset is in the set of supported assets that can be used as collateral, strike, or underlying.

```javascript
function supportsAsset(string memory _asset) public view returns (bool)
```

> `string memory _asset`: The asset to check
>
> `RETURN:` True if the asset is in the set of supported assets; otherwise false

{% tabs %}
{% tab title="Solidity" %}
```javascript
OptionsFactory factory = OptionsFactory(0xABCD...);
bool isSupported = factory.supportsAsset("TKN");
```
{% endtab %}

{% tab title="Web3 1.0" %}
```javascript
const factory = OptionsFactory.at('0xABCD...');
const isSupported = await factory.methods.supportsAsset("TKN").call();
```
{% endtab %}
{% endtabs %}

## Events





