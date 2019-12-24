# Getting Started

## Introduction to Convexity

Convexity is a Decentralized Put Options Protocol built on the Ethereum Blockchain. Convexity provides an easy interface to buy and sell put options. 

Put options work as insurance in traditional finance. Convexity allows options sellers to earn premiums on their collateral and options buyers to protect themselves against technical, financial and systemic risks that various DeFi projects face. These risks include hacks, bank runs, a DeFi crisis etc. 

Please join the \#dev room in the Opyn community [Discord](https://discord.gg/ugAv3SH) server; our team, and members of the community, look forward to helping you build an application on top of Opyn. Your questions help us improve, so please don't hesitate to ask if you can't find what you are looking for here. 

## Resources

* [Website](http://www.opyn.co/)
* [Whitepaper](https://drive.google.com/file/d/1YsrGBUpZoPvFLtcwkEYkxNhogWCU772D/view)
* [Github](https://github.com/aparnakr/OptionsProtocol)
* Twitter
* Discord
* Email
* [Beginner Resources](examples-tutorial.md#beginner-resources)

## Networks 

 The Opyn Protocol is currently deployed on the following networks:

### Rinkeby

<table>
  <thead>
    <tr>
      <th style="text-align:left">Contract</th>
      <th style="text-align:left">JSON</th>
      <th style="text-align:left">
        <p>Solidity</p>
        <p>Interface</p>
      </th>
      <th style="text-align:left">Address</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Uniswap Exchange</td>
      <td style="text-align:left"><a href="https://docs.uniswap.io/smart-contract-integration/interface">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Uniswap Factory</td>
      <td style="text-align:left"><a href="https://docs.uniswap.io/smart-contract-integration/interface">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">0xf5D915570BC477f9B8D6C0E980aA81757A3AaC36</td>
    </tr>
    <tr>
      <td style="text-align:left">Options Exchange</td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/OptionsExchange.json">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Dai</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">cDai</td>
      <td style="text-align:left"><a href="https://compound.finance/developers/abi/mainnet/cDAI">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">cUSDC</td>
      <td style="text-align:left"><a href="https://compound.finance/developers/abi/mainnet/cUSDC">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">ocDai</td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">oDai</td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">ocUSDC</td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Options Factory</td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/OptionsFactory.json">JSON</a>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>### Mainnet

## Example Use Case: Insurance on Compound

Consider the case of a Compound user, person A, who wants insurance on their Dai locked in Compound. They fear Compound getting hacked or having a bank run. The insurance buyer, person A, pays the insurance provider, person B,  0.01 ETH premium ahead of time to get access to ocDai tokens. In return, person B, locks up 1 ETH of collateral on the insurance platform. 

The ocDai token protects the holder of the token from Jan 1 2020 to Jan 1 2021 against any technical or financial risks that Compound's cDai faces. In the case of a disaster, the holder of the ocDai, person A, can turn in their oTokens and their cDai and in exchange take out $1 worth of collateral locked in the Convexity Protocol by insurance providers. If there is no disaster, it is strictly worse for the holder of cDai to give up their cDai in exchange for collateral locked on the Convexity protocol. In such a case, the insurance provider, person B, keeps their collateral and earns a premium on it. 

## Gas Costs 

## web3 version + solidity compiler version  



## Glossary of Terms 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Term</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Put Option</td>
      <td style="text-align:left">A put option gives the owner/buyer the right to sell an asset, at a specified
        price, by a predetermined date to the seller of the put option.</td>
    </tr>
    <tr>
      <td style="text-align:left">Premium</td>
      <td style="text-align:left">
        <p>The money paid upfront by the option buyers to the option sellers in return.</p>
        <p></p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>0.01 ETH is the premium paid by person A to person B.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Option Seller</td>
      <td style="text-align:left">
        <p>The person who sells an <b>option</b> in return for a premium and is obligated
          to perform when the buyer exercises his right under the <b>option</b> contract.</p>
        <p></p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>Person B is the option seller.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Option Buyer</td>
      <td style="text-align:left">
        <p>The person who buys an <b>option</b> by paying a premium. This person has
          right but not obligation to exercise the option.</p>
        <p></p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>Person A is the option buyer/ owner.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Underlying</td>
      <td style="text-align:left">
        <p>The asset that is being protected by the option contract is called the
          underlying asset. The asset that the owner/buyer of the put option has
          the right to sell is called the underlying asset.</p>
        <p></p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>The underlying asset is cDai.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Strike Asset</td>
      <td style="text-align:left">
        <p>The asset that the holder/buyer of the put option will receive their payment
          in if they sell the underlying asset is called the strike asset.</p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>The strike asset is USD.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Strike Price</td>
      <td style="text-align:left">
        <p>The strike price is the specified price at which the buyer/owner of the
          option can sell the underlying asset.</p>
        <p></p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>The strike price is 1 USD.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Collateral Asset</td>
      <td style="text-align:left">
        <p>The asset that the insurance provider puts down as collateral is called
          the collateral asset.</p>
        <p></p>
        <p><a href="./#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>The collateral asset is ETH.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">putsOutstanding</td>
      <td style="text-align:left">The number of oTokens issued by a vault.</td>
    </tr>
    <tr>
      <td style="text-align:left">minCollateralizationRatio</td>
      <td style="text-align:left">The ratio of collateral to the amount of insurance payout that a vault
        would have to make is called the collateralization ratio. The minCollateralizationRatio
        is the lower bound that a vault&apos;s collateralization ratio is allowed
        to be at.</td>
    </tr>
    <tr>
      <td style="text-align:left">Safe</td>
      <td style="text-align:left">
        <p>A vault that meets the minCollateralization condition is considered safe.
          i.e.</p>
        <p></p>
        <p></p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Liquidation factor</td>
      <td style="text-align:left">The maximum percentage of collateral that can be liquidated in one call
        of the liquidation function.</td>
    </tr>
    <tr>
      <td style="text-align:left">Liquidation Incentive</td>
      <td style="text-align:left">
        <p>The reward that is paid out to the liquidator. The liquidator is paid
          out</p>
        <p></p>
        <p>for every oToken that they bring back to the insurance contract to liquidate.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Exercise</td>
      <td style="text-align:left">To exercise means to put into effect the right to sell the underlying
        asset at the specified price.</td>
    </tr>
    <tr>
      <td style="text-align:left">Exercise Window</td>
      <td style="text-align:left">The time period during which the option buyer/ owner can exercise their
        option.</td>
    </tr>
  </tbody>
</table>