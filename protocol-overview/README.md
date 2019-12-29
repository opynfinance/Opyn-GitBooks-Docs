# Protocol Overview

## Smart Contract Architecture 

### Options Factory

The OptionsFactory contract is used to create and keep track of options marketplaces. Each options marketplace is a new instantiation of the oToken contract. 

![Factory contract keeps track of all the oToken contracts.](../.gitbook/assets/screen-shot-2019-12-19-at-6.54.00-pm.png)

### oToken

Every option supported by the Convexity Protocol is integrated through an oToken smart contract. Options sellers create options by locking up collateral for some period of time and minting oTokens. Each oToken protects a unit of the specified underlying asset. The Options seller can sell these oTokens on an exchange to earn premiums. The oToken marketplaces deployed for the purpose of insurance are oDai, ocDai and ocUSDC. 

