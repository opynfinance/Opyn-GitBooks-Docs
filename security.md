# Security

The security of the Opyn protocol is our highest priority. Our team has created a protocol that we believe is safe and dependable, and has been audited by OpenZeppelin. All smart contract code is publicly verifiable and we have a bug bounty for undiscovered vulnerabilities. Options are complex instruments that when understood correctly can be powerful hedges. We want to remind our users to be optimistic about innovation while remaining cautious about where they put their money.

## Audits

Opyn's smart contracts have undergone rigorous internal testing and a smart contract audit from OpenZeppelin.

[**OpenZeppelin Audit** ](https://blog.openzeppelin.com/opyn-contracts-audit/)\*\*\*\*

## Bug Bounty Program

Security is one of our highest priorities, and while Opyn's smart contracts have been rigorously tested and audited, there may still be undiscovered vulnerabilities with this new technology. We really value the community's input in helping us discover vulnerabilities responsibly disclosing them. 

#### Scope

This program is limited to the vulnerabilities affecting the Convexity Protocol in the following contracts:

* [OptionsFactory](https://github.com/opynfinance/Convexity-Protocol/blob/master/contracts/OptionsFactory.sol)
* [OptionsContract](https://github.com/opynfinance/Convexity-Protocol/blob/master/contracts/OptionsContract.sol)
* [oToken](https://github.com/opynfinance/Convexity-Protocol/blob/master/contracts/oToken.sol)
* [OptionsExchange](https://github.com/opynfinance/Convexity-Protocol/blob/master/contracts/OptionsExchange.sol)
* [Oracle](https://github.com/opynfinance/Convexity-Protocol/blob/master/contracts/Oracle.sol)\*

_\*The oracle contract is not used for ETH puts or calls. The oracle calls from Compound's oracle and is only used for the price of ETH as collateral for Compound protection. cTokens will not be used as collateral in this version of the protocol._ 

Submissions should be based off this commit hash: [https://github.com/opynfinance/Convexity-Protocol/tree/097d23322b86ceee0f6a3125d49f6d3e85dedb14](https://github.com/opynfinance/Convexity-Protocol/tree/097d23322b86ceee0f6a3125d49f6d3e85dedb14)  


**Rewards** 

Severity of bugs will be assessed under the [CVSS Risk Rating](https://www.first.org/cvss/calculator/3.0) scale, as follows:

* Critical \(9.0-10.0\): Up to $40,000
* High \(7.0-8.9\): Up to $10,000
* Medium \(4.0-6.9\): Up to $5,000
* Low \(0.1-3.9\): Up to $1,000

#### Disclosures

Any vulnerability or bug discovered must be reported only to the following email: security@opyn.co must not be disclosed publicly, must not be disclosed to any other person, entity or email address prior to disclosure to the security@opyn.co email, and must not be disclosed in any way other than to the security@opyn.co email. In addition, disclosure to security@opyn.co must be made promptly following discovery of the vulnerability. Please include as much information about the vulnerability as possible, including:

* The conditions on which reproducing the bug is contingent.
* The steps needed to reproduce the bug or, preferably, a proof of concept.
* The potential implications of the vulnerability being abused.

Anyone who reports a unique, previously-unreported vulnerability that results in a change to the code or a configuration change and who keeps such vulnerability confidential until it has been resolved by our engineers will be recognized publicly for their contribution, if agreed.

#### Ineligible Findings

* Vulnerabilities contingent upon the occurrence of any of the following activities also are outside the scope of this Program:
  * Front end bugs
  * DDOS attack
  * Spamming
* Exploiting the vulnerability in any way, including through making it public or by obtaining a profit \(other than a reward under this Program\).
* Duplicate vulnerabilities: Only the first reporter will be rewarded \(in compliance with the disclosure requirements above.\)
* Findings already known as part of a formal audit or are marked on the repo as issues.  

