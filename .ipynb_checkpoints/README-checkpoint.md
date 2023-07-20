# advanced-solidity
Module 21 Challenge: Martian Token Crowdsale

## Evaluation evidence
### Ganache initialized
![Ganache initialized](Evaluation_Evidence/ganache_initialized.png)  
The addresses used in this demonstration were obtained from a Ganache workspace.

### KaseiCoin contract compiled
![KaseiCoin contract compiled](Evaluation_Evidence/kasei_coin_contract_compiled.png)  
The KaseiCoin contract was compiled using Solidity compiler 0.5.17 (the compiler version used for all lesson work) in the `SOLIDITY COMPILER` section of Remix - Ethereum IDE.

### KaseiCoinCrowdsale contract compiled
![KaseiCoinCrowdsale contract compiled](Evaluation_Evidence/kasei_coin_crowdsale_contract_compiled.png)  
The KaseiCoinCrowdsale contract was compiled using Solidity compiler 0.5.17 (the compiler version used for all lesson work) in the `SOLIDITY COMPILER` section of Remix - Ethereum IDE.

### KaseiCoinCrowdsaleDeployer contract compiled
![KaseiCoinCrowdsaleDeployer contract compiled](Evaluation_Evidence/kasei_coin_crowdsale_deployer_contract_compiled.png)  
The KaseiCoinCrowdsale contract was compiled using Solidity compiler 0.5.17 (the compiler version used for all lesson work) in the `SOLIDITY COMPILER` section of Remix - Ethereum IDE.

### KaseiCoinCrowdsaleDeployer contract initialized, confirmed and deployed
#### Contract initialized and confirmed

| ![KaseiCoinCrowdsaleDeployer contract initialized](Evaluation_Evidence/kasei_coin_crowdsale_deployer_contract_initialized.png) | ![KaseiCoinCrowdsaleDeployer contract confirmed](Evaluation_Evidence/kasei_coin_crowdsale_deployer_contract_confirmed.png) |
| --- | --- |

The KaseiCoinCrowdsaleDeployer contract was initialized using the following inputs:
- `NAME` => `KaseiCoin`
- `SYMBOL` => `KSC`
- `WALLET` => `0xD90aFeC47BD8e33A18233759869a5dA598F9673B`
> **Note:** The `WALLET` address was taken from address index `2` in Ganache.

Upon clicking the `transact` button, a transaction confirmation prompt was provided by MetaMask.

#### Contract deployed
![KaseiCoinCrowdsaleDeployer contract deployed](Evaluation_Evidence/kasei_coin_crowdsale_deployer_contract_deployed.png)  
Upon clicking the `Confirm` button in the MetaMask prompt, the contract was deployed.

#### Contract functions
![KaseiCoinCrowdsaleDeployer contract functions](Evaluation_Evidence/kasei_coin_crowdsale_deployer_contract_functions.png)  
The deployed contract contains two functions:
- `kasei_crowdsale_address`
- `kasei_token_address`

#### Kasei crowdsale address
![Kasei crowdsale address](Evaluation_Evidence/kasei_crowdsale_address.png)  
The Kasei crowdsale address can be obtained using the `kasei_crowdsale_address` function.
> **Note:** The Kasei crowdsale address is: `0x64F53c16E3782f392ea6B0939e1f5BF5719c1747`

#### Kasei token address
![Kasei token address](Evaluation_Evidence/kasei_token_address.png)  
The Kasei token address can be obtained using the `kasei_token_address` function.
> **Note:** The Kasei token address is: `0x90Cd285dfc08f3e875fe1F29D36cB6019A619a83`

### KaseiCoinCrowdsale contract loaded
#### Contract initialized
![KaseiCoinCrowdsale contract loaded](Evaluation_Evidence/kasei_coin_crowdsale_contract_loaded.png)  
The KaseiCoinCrowdsale contract was loaded using the `Load contract from Address` function located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The address entered in the input was the Kasei crowdsale address. Upon clicking the `At Address` button, the contract was loaded.

#### Contract functions
![KaseiCoinCrowdsale contract functions](Evaluation_Evidence/kasei_coin_crowdsale_contract_functions.png)  
The deployed contract contains five functions:
- `buyTokens`
- `rate`
- `token`
- `wallet`
- `weiRaised`

### KaseiCoin contract loaded
#### Contract initialized
![KaseiCoin contract loaded](Evaluation_Evidence/kasei_coin_contract_loaded.png)  
The KaseiCoin contract was loaded using the `Load contract from Address` function located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The address entered in the input was the Kasei token address. Upon clicking the `At Address` button, the contract was loaded.

#### Contract functions
![KaseiCoin contract functions](Evaluation_Evidence/kasei_coin_contract_functions.png)  
The deployed contract contains 15 functions:
- `addMinter`
- `approve`
- `decreaseAllowance`
- `mint`
- `increaseAllowance`
- `renounceMinter`
- `transfer`
- `transferFrom`
- `allowance`
- `balanceOf`
- `decimals`
- `isMinter`
- `name`
- `symbol`
- `totalSupply`

### First token purchase
#### Token purchase initialized and confirmed

| ![First token purchase initialized](Evaluation_Evidence/first_token_purchase_initialized.png) | ![First token purchase confirmed](Evaluation_Evidence/first_token_purchase_confirmed.png) |
| --- | --- |

The first token purchase was initialized using the following inputs:
- `VALUE` => `10` and `Ether`
- `beneficiary` => `0x325e7365f2208Cf281d2AE62F6E3f2FE933b8F5e`
> **Note:** The `beneficiary` address was taken from address index `1` in Ganache.

The `VALUE` inputs are located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The `beneficiary` input is located in the `buyTokens` function of the `KaseiCoinCrowdsale` contract.

Upon clicking the `transact` button in the `buyTokens` function, a transaction confirmation prompt was provided by MetaMask.

#### Token purchase completed
![First token purchase completed](Evaluation_Evidence/first_token_purchase_completed.png)  
Upon clicking the `Confirm` button in the Metamask prompt, the token purchase was completed.

#### Crowdsale confirmation
![First token purchase crowdsale confirmation](Evaluation_Evidence/first_token_purchase_crowdsale_confirmation.png)  
Crowdsale confirmation of the token purchase was obtained using the `weiRaised` function of the `KaseiCoinCrowdsale` contract. Upon clicking the `weiRaised` button, the value of Wei raised from the purchase was displayed.
> **Note:** The value of Wei raised from the purchase was 10000000000000000000.

#### Beneficiary confirmation
![First token purchase beneficiary confirmation](Evaluation_Evidence/first_token_purchase_beneficiary_confirmation.png)  
Beneficiary confirmation of the token purchase was obtained using the `balanceOf` function of the `KaseiCoin` contract. The address entered in the `account` input was the `beneficiary` address used to initialize the token purchase. Upon clicking the `call` button in the `balanceOf` function, the value of the token purchase in Wei was displayed.
> **Note:** The Wei value of 10 Ether is 10000000000000000000.

### Second token purchase
#### Token purchase initialized and confirmed

| ![Second token purchase initialized](Evaluation_Evidence/second_token_purchase_initialized.png) | ![Second token purchase confirmed](Evaluation_Evidence/second_token_purchase_confirmed.png) |
| --- | --- |

The second token purchase was initialized using the following inputs:
- `VALUE` => `31500000000000000000` and `Wei`
- `beneficiary` => `0x4564415Df66508974afbf630Cd1a44196AA8d30f`
> **Note:** The `beneficiary` address was taken from address index `0` in Ganache.

The `VALUE` inputs are located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The `beneficiary` input is located in the `buyTokens` function of the `KaseiCoinCrowdsale` contract.

Upon clicking the `transact` button in the `buyTokens` function, a transaction confirmation prompt was provided by MetaMask.

#### Token purchase completed
![Second token purchase completed](Evaluation_Evidence/second_token_purchase_completed.png)  
Upon clicking the `Confirm` button in the Metamask prompt, the token purchase was completed.

#### Crowdsale confirmation
![Second token purchase crowdsale confirmation](Evaluation_Evidence/second_token_purchase_crowdsale_confirmation.png)  
Crowdsale confirmation of the token purchase was obtained using the `weiRaised` function of the `KaseiCoinCrowdsale` contract. Upon clicking the `weiRaised` button, the value of Wei raised from the first two purchases was displayed.
> **Note:** The value of Wei raised from the first two purchases was 41500000000000000000.

#### Beneficiary confirmation
![Second token purchase beneficiary confirmation](Evaluation_Evidence/second_token_purchase_beneficiary_confirmation.png)  
Beneficiary confirmation of the token purchase was obtained using the `balanceOf` function of the `KaseiCoin` contract. The address entered in the `account` input was the `beneficiary` address used to initialize the token purchase. Upon clicking the `call` button in the `balanceOf` function, the value of the token purchase in Wei was displayed.

### Ganache results
![Ganache results](Evaluation_Evidence/ganache_results.png)  
The result of all contract functions performed was visible in the Ganache workspace.

## Other information
- All work for the KaseiCoin contract can be found in the [KaseiCoin.sol](https://github.com/julianritchey/solidity-homework/blob/main/KaseiCoin.sol) file.
- All work for the KaseiCoinCrowdsale and KaseiCoinCrowdsaleDeployer contracts can be found in the [KaseiCoinCrowdsale.sol](https://github.com/julianritchey/solidity-homework/blob/main/KaseiCoinCrowdsale.sol) file.
- All screenshots used in this assignment can be found in the [Evaluation_Evidence](https://github.com/julianritchey/solidity-homework/tree/main/Evaluation_Evidence) folder.