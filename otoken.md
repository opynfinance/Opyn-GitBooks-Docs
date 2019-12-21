# oToken

## Introduction

Every option supported by the Convexity Protocol is integrated through an oToken smart contract which is an [EIP-20](https://eips.ethereum.org/EIPS/eip-20) compliant representation of options issued by the protocol. Options sellers create options by locking up collateral for some period of time and minting oTokens. Each oToken protects a unit of the specified underlying ERC20 asset. The Options seller can sell these oTokens on an exchange to earn premiums. The oToken marketplaces deployed for the purpose of insurance are oDai, ocDai and ocUSDC. 

The main functionality offered by the convexity protocol is as below:

1. Create oTokens
2. Keep the oToken repos sufficiently collateralized
3. Liquidate the undercollateralized repos
4. Exercise the oTokens during the expiry window

## Functions 

### **Open Vault**

The open vault function creates an empty vault and sets the owner of the vault to be the msg.sender. The collateral and the outstanding puts issued of the vault are set to 0. 

```javascript
function openVault() public returns (uint)
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
function addETHCollateral(uint256 vaultIndex) public payable returns (uint256) 
```

> `vaultIndex` : The index of the vault to add collateral to
>
> `msg.sender` : The account from which ETH collateral will be transferred into the oToken contract
>
> `msg.value` : The amount of ETH to add

#### Add ERC20 Collateral

The `addERC20Collateral()` function is called if the specified collateral for the oToken contract is any ERC20 asset. The function will only add the specified collateral asset. It will fail if called on any other asset other than the pre specified collateral asset. 

#### Create Options Contract 

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

* `string memory _collateralType`: The collateral asset \(eg. ETH, USDC, etc.\) 
* `string memory _underlyingType`: The asset upon which the option is based. In the insurance use case, the asset that is being protected. \(eg. DAI, cUSDC, etc.\) 
* `uint256 _strikePrice`: The amount of the strike asset that will be paid out upon exercise \(eg. 1\)
* `string memory _strikeAsset`: The asset in which the option is denominated. \(eg. DAI option denominated in USDC\)
* `string memory _payoutType`: The asset in which the option is paid out. \(eg. ETH\)
* `uint256 _expiry`: The unix time at which the option expires \(eg. 1574457816\)
* `RETURN address:` The address of the options contract on success; otherwise TODO: Error Code

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

{% tab title="web3" %}
```javascript
const factory = OptionsFactory.at(0xABCD...);
const optionContract = await factory.methods.createOptionsContract(
                                "ETH",
                                "DAI",
                                "USDC", 
                                1,
                                "USDC", 
                                "ETH",  
                                1574457816
).call();
```
{% endtab %}
{% endtabs %}

#### 

## Events 

## Error Table





