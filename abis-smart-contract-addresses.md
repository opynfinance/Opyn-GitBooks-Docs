# ABIs / Smart Contract Addresses

## Networks 

 The Convexity Protocol is currently deployed on the following Ethereum networks:

### Mainnet

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
      <td style="text-align:left"><a href="https://etherscan.io/address/0x2157a7894439191e520825fe9399ab8655e0f708#code">Uniswap Exchange</a>
      </td>
      <td style="text-align:left"><a href="http://api.etherscan.io/api?module=contract&amp;action=getabi&amp;address=0x2157a7894439191e520825fe9399ab8655e0f708&amp;format=raw">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://docs.uniswap.io/smart-contract-integration/interface">Interface</a>
      </td>
      <td style="text-align:left">(<a href="https://etherscan.io/address/0xc0a47dfe034b400b47bdad5fecda2621de6c4d95#readContract">getExchange from uniswap factory</a>)</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xc0a47dfe034b400b47bdad5fecda2621de6c4d95#code">Uniswap Factory</a>
      </td>
      <td style="text-align:left"><a href="http://api.etherscan.io/api?module=contract&amp;action=getabi&amp;address=0xc0a47dfe034b400b47bdad5fecda2621de6c4d95&amp;format=raw">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://docs.uniswap.io/smart-contract-integration/interface">Interface</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0xc0a47dfe034b400b47bdad5fecda2621de6c4d95#code">0xc0a47dFe034B400B47bDaD5FecDa2621de6c4d95</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x5778f2824a114f6115dc74d432685d3336216017#code">Options Exchange</a>
      </td>
      <td style="text-align:left"><a href="http://api.etherscan.io/api?module=contract&amp;action=getabi&amp;address=0x5778f2824a114f6115dc74d432685d3336216017&amp;format=raw">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x5778f2824a114f6115dc74d432685d3336216017#code">0x5778f2824a114F6115dc74d432685d3336216017</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">cDai</td>
      <td style="text-align:left"><a href="https://compound.finance/developers/abi/mainnet/cDAI">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x6c8c6b02e7b2be14d4fa6022dfd6d75921d90e4e#code">Interface</a>
      </td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x6d7f0754ffeb405d23c51ce938289d4835be3b14">0x6d7f0754ffeb405d23c51ce938289d4835be3b14</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">cUSDC</td>
      <td style="text-align:left"><a href="https://compound.finance/developers/abi/mainnet/cUSDC">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x6c8c6b02e7b2be14d4fa6022dfd6d75921d90e4e#code">Interface</a>
      </td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x5B281A6DdA0B271e91ae35DE655Ad301C976edb1">0x5B281A6DdA0B271e91ae35DE655Ad301C976edb1</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">ocDai</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x57cC8708eFEB7f7D42E4d73ab9120BC275f1DB59">0x57cC8708eFEB7f7D42E4d73ab9120BC275f1DB59</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">ocUSDC</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x59d5652ac7ae3008f59ae7b71ed66c98eda317d6">0x59D5652Ac7aE3008f59AE7b71eD66C98edA317d6</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">Options Factory</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/OptionsFactory.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x34Da8b34c82988e7FF8F98CA35963057fC0ec9bb">0x34Da8b34c82988e7FF8F98CA35963057fC0ec9bb</a>
      </td>
    </tr>
  </tbody>
</table>### Rinkeby

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
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/UniswapExchange.json">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://docs.uniswap.io/smart-contract-integration/interface">Interface</a>
      </td>
      <td style="text-align:left">(<a href="https://docs.uniswap.io/smart-contract-api/factory#getexchange">getExchange</a> from
        uniswap factory)</td>
    </tr>
    <tr>
      <td style="text-align:left">Uniswap Factory</td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/UniswapExchange.json">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://docs.uniswap.io/smart-contract-integration/interface">Interface</a>
      </td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0xf5d915570bc477f9b8d6c0e980aa81757a3aac36#code">0xf5D915570BC477f9B8D6C0E980aA81757A3AaC36</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">Options Exchange</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/OptionsExchange.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x40c471C6B31E752F39Fd0232Ad5daE42240eeD67">0x40c471C6B31E752F39Fd0232Ad5daE42240eeD67</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">cDai</td>
      <td style="text-align:left"><a href="https://compound.finance/developers/abi/mainnet/cDAI">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x6c8c6b02e7b2be14d4fa6022dfd6d75921d90e4e#code">Interface</a>
      </td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x6d7f0754ffeb405d23c51ce938289d4835be3b14">0x6d7f0754ffeb405d23c51ce938289d4835be3b14</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">cUSDC</td>
      <td style="text-align:left"><a href="https://compound.finance/developers/abi/mainnet/cUSDC">JSON</a>
      </td>
      <td style="text-align:left"><a href="https://etherscan.io/address/0x6c8c6b02e7b2be14d4fa6022dfd6d75921d90e4e#code">Interface</a>
      </td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x5B281A6DdA0B271e91ae35DE655Ad301C976edb1">0x5B281A6DdA0B271e91ae35DE655Ad301C976edb1</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">ocDai</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x57cC8708eFEB7f7D42E4d73ab9120BC275f1DB59">0x57cC8708eFEB7f7D42E4d73ab9120BC275f1DB59</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">ocUSDC</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/oToken.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x59d5652ac7ae3008f59ae7b71ed66c98eda317d6">0x59D5652Ac7aE3008f59AE7b71eD66C98edA317d6</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol">Options Factory</a>
      </td>
      <td style="text-align:left"><a href="https://github.com/aparnakr/OptionsProtocol/blob/buyer-and-seller-docs/ABIs/OptionsFactory.json">JSON</a>
      </td>
      <td style="text-align:left">Interface</td>
      <td style="text-align:left"><a href="https://rinkeby.etherscan.io/address/0x34Da8b34c82988e7FF8F98CA35963057fC0ec9bb">0x34Da8b34c82988e7FF8F98CA35963057fC0ec9bb</a>
      </td>
    </tr>
  </tbody>
</table>

