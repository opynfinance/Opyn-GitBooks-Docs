# Glossary of Terms

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
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
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
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
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
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
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
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
        </p>
        <p>The underlying asset is cDai.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Strike Asset</td>
      <td style="text-align:left">
        <p>The asset that the holder/buyer of the put option will receive their payment
          in if they sell the underlying asset is called the strike asset.</p>
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
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
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
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
        <p><a href="../#example-use-case-insurance-on-compound">In the Example Insurance Use Case:</a>
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
    <tr>
      <td style="text-align:left">Number</td>
      <td style="text-align:left">value * 10 ^ exponent.</td>
    </tr>
  </tbody>
</table>