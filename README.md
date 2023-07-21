# advanced-solidity-homework
Module 21 Challenge: Martian Token Crowdsale

## Evaluation evidence
### Ganache initialized
![Ganache initialized](Evaluation_Evidence/ganache_initialized.png)  
The addresses used in this demonstration were obtained from a Ganache workspace and imported into MetaMask on a network connected to the Ganache workspace.

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

The KaseiCoinCrowdsaleDeployer contract was initialized using the following inputs and values found in the `DEPLOY` function in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE:
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
#### Contract loaded
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

| ![First token purchase initialized](Evaluation_Evidence/token_purchase_1_initialized.png) | ![First token purchase confirmed](Evaluation_Evidence/token_purchase_1_purchase_confirmed.png) |
| --- | --- |

The first token purchase was initialized using the following inputs:
- `VALUE` => `10` and `Ether`
- `beneficiary` => `0x325e7365f2208Cf281d2AE62F6E3f2FE933b8F5e`
> **Note:** The `beneficiary` address was taken from address index `1` in Ganache.

The `VALUE` inputs are located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The `beneficiary` input is located in the `buyTokens` function of the `KaseiCoinCrowdsale` contract.

Upon clicking the `transact` button in the `buyTokens` function, a transaction confirmation prompt was provided by MetaMask.

#### Token purchase completed
![First token purchase completed](Evaluation_Evidence/token_purchase_1_completed.png)  
Upon clicking the `Confirm` button in the Metamask prompt, the token purchase was completed.

#### Crowdsale confirmation
![First token purchase crowdsale confirmation](Evaluation_Evidence/token_purchase_1_crowdsale_confirmation.png)  
Crowdsale confirmation of the token purchase was obtained using the `weiRaised` function of the `KaseiCoinCrowdsale` contract. Upon clicking the `weiRaised` button, the value of Wei raised from the purchase was displayed.
> **Note:** The value of Wei raised from the purchase was 10000000000000000000.

#### Beneficiary confirmation
![First token purchase beneficiary confirmation](Evaluation_Evidence/token_purchase_1_beneficiary_confirmation.png)  
Beneficiary confirmation of the token purchase was obtained using the `balanceOf` function of the `KaseiCoin` contract. The address entered in the `account` input was the `beneficiary` address used to initialize the token purchase. Upon clicking the `call` button in the `balanceOf` function, the value of the token purchase in Wei was displayed.
> **Note:** The Wei value of 10 Ether is 10000000000000000000.

### Second token purchase
#### Token purchase initialized and confirmed

| ![Second token purchase initialized](Evaluation_Evidence/token_purchase_2_initialized.png) | ![Second token purchase confirmed](Evaluation_Evidence/token_purchase_2_confirmed.png) |
| --- | --- |

The second token purchase was initialized using the following inputs:
- `VALUE` => `31500000000000000000` and `Wei`
- `beneficiary` => `0x4564415Df66508974afbf630Cd1a44196AA8d30f`
> **Note:** The `beneficiary` address was taken from address index `0` in Ganache.

The `VALUE` inputs are located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The `beneficiary` input is located in the `buyTokens` function of the `KaseiCoinCrowdsale` contract.

Upon clicking the `transact` button in the `buyTokens` function, a transaction confirmation prompt was provided by MetaMask.

#### Token purchase completed
![Second token purchase completed](Evaluation_Evidence/token_purchase_2_completed.png)  
Upon clicking the `Confirm` button in the Metamask prompt, the token purchase was completed.

#### Crowdsale confirmation
![Second token purchase crowdsale confirmation](Evaluation_Evidence/token_purchase_2_crowdsale_confirmation.png)  
Crowdsale confirmation of the token purchase was obtained using the `weiRaised` function of the `KaseiCoinCrowdsale` contract. Upon clicking the `weiRaised` button, the value of Wei raised from the first two purchases was displayed.
> **Note:** The value of Wei raised from the first two purchases was 41500000000000000000.

#### Beneficiary confirmation
![Second token purchase beneficiary confirmation](Evaluation_Evidence/token_purchase_2_beneficiary_confirmation.png)  
Beneficiary confirmation of the token purchase was obtained using the `balanceOf` function of the `KaseiCoin` contract. The address entered in the `account` input was the `beneficiary` address used to initialize the token purchase. Upon clicking the `call` button in the `balanceOf` function, the value of the token purchase in Wei was displayed.

### Total supply confirmation
![Total supply confirmation](Evaluation_Evidence/total_supply_confirmation.png)  
The total supply of purchased tokens was obtained using the `totalSupply` function of the `KaseiCoin` contract. Upon clicking the `totalSupply` button, the value of the total supply in Wei was displayed.
> **Note:** The value of the total supply in Wei was 41500000000000000000.

### Ganache results
![Ganache results](Evaluation_Evidence/ganache_results.png)  
The result of all contract functions performed was visible in the Ganache workspace.

## Optional: Extend the crowdsale contract by using OpenZeppelin
### Ganache initialized
![Optional: Ganache initialized](Evaluation_Evidence/optional_ganache_initialized.png)  
The addresses used in this demonstration were obtained from a Ganache workspace.

### KaseiCoinCrowdsale and KaseiCoinCrowdsaleDeployer contracts extended
![Optional: KaseiCoinCrowdsale and KaseiCoinCrowdsaleDeployer contracts extended](Evaluation_Evidence/optional_kasei_coin_crowdsale_contracts_extended.png)  
To accommodate the functions of a capped crowdsale, a timed crowdsale, and a crowdsale refund, the KaseiCoinCrowdsale contract was extended to incorporate the `CappedCrowdsale`, `TimedCrowdsale` and `RefundablePostDeliveryCrowdsale` contracts.

### KaseiCoinCrowdsaleDeployer contract initialized, confirmed and deployed
#### Contract initialized and confirmed

| ![Optional: KaseiCoinCrowdsaleDeployer contract initialized](Evaluation_Evidence/optional_kasei_coin_crowdsale_deployer_contract_initialized.png) | ![Optional: KaseiCoinCrowdsaleDeployer contract confirmed](Evaluation_Evidence/optional_kasei_coin_crowdsale_deployer_contract_confirmed.png) |
| --- | --- |

The KaseiCoinCrowdsaleDeployer contract was initialized using the following inputs and values found in the `DEPLOY` function in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE:
- `NAME` => `KaseiCoin`
- `SYMBOL` => `KSC`
- `WALLET` => `0xD90aFeC47BD8e33A18233759869a5dA598F9673B`
> **Note:** The `WALLET` address was taken from address index `2` in Ganache.

Upon clicking the `transact` button, a transaction confirmation prompt was provided by MetaMask.
#### Contract deployed
![Optional: KaseiCoinCrowdsaleDeployer contract deployed](Evaluation_Evidence/optional_kasei_coin_crowdsale_deployer_contract_deployed.png)  
The KaseiCoinCrowdsaleDeployer contract was deployed using the following inputs and values found in the `DEPLOY` function in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE:
- `NAME` => `KaseiCoin`
- `SYMBOL` => `KSC`
- `WALLET` => `0xD90aFeC47BD8e33A18233759869a5dA598F9673B`
- `GOAL` => `100000000000000000000`
> **Note:** The `WALLET` address was taken from address index `3` in Ganache. The `GOAL` value is displayed in Wei and equates to 100 Ether.

Upon clicking the `transact` button, a transaction confirmation prompt was provided by MetaMask. Upon clicking the `Confirm` button in the Metamask prompt, the contract was deployed.

#### Contract functions
![Optional: KaseiCoinCrowdsaleDeployer contract functions](Evaluation_Evidence/optional_kasei_coin_crowdsale_deployer_contract_functions.png)  
The deployed contract contains two functions:
- `kasei_crowdsale_address`
- `kasei_token_address`

#### Kasei crowdsale address
![Optional: Kasei crowdsale address](Evaluation_Evidence/optional_kasei_crowdsale_address.png)  
The Kasei crowdsale address can be obtained using the `kasei_crowdsale_address` function.
> **Note:** The Kasei crowdsale address is: `0x262cd8BF5F0E79c4f0Bc1112A20417166a964970`

#### Kasei token address
![Optional: Kasei token address](Evaluation_Evidence/optional_kasei_token_address.png)  
The Kasei token address can be obtained using the `kasei_token_address` function.
> **Note:** The Kasei token address is: `0x9c64F30E5cfaEC6e82f03aa8732C0854a423CF62`

### KaseiCoinCrowdsale contract loaded
#### Contract loaded
![Optional: KaseiCoinCrowdsale contract loaded](Evaluation_Evidence/optional_kasei_coin_crowdsale_contract_loaded.png)  
The KaseiCoinCrowdsale contract was loaded using the `Load contract from Address` function located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The address entered in the input was the Kasei crowdsale address. Upon clicking the `At Address` button, the contract was loaded.

#### Contract functions
![Optional: KaseiCoinCrowdsale contract functions](Evaluation_Evidence/optional_kasei_coin_crowdsale_contract_functions.png)  
The deployed contract contains 18 functions:
- `buyTokens`
- `claimRefund`
- `finalize`
- `withdrawTokens`
- `balanceOf`
- `cap`
- `capReached`
- `closingTime`
- `finalized`
- `goal`
- `goalReached`
- `hasClosed`
- `isOpen`
- `openingTime`
- `rate`
- `token`
- `wallet`
- `weiRaised`

### KaseiCoin contract loaded
#### Contract initialized
![Optional: KaseiCoin contract loaded](Evaluation_Evidence/optional_kasei_coin_contract_loaded.png)  
The KaseiCoin contract was loaded using the `Load contract from Address` function located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The address entered in the input was the Kasei token address. Upon clicking the `At Address` button, the contract was loaded.

#### Contract functions
![Optional: KaseiCoin contract functions](Evaluation_Evidence/optional_kasei_coin_contract_functions.png)  
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

### Token purchase
#### Token purchase initialized and confirmed

| ![Optional: Token purchase initialized](Evaluation_Evidence/optional_token_purchase_initialized.png) | ![Optional: Token purchase confirmed](Evaluation_Evidence/optional_token_purchase_confirmed.png) |
| --- | --- |

In this demonstration, three token purchases were performed. The purchases were initialized using the following inputs:
- Token purchase 1
  - `VALUE` => `40` and `Ether`
  - `beneficiary` => `0xB218A34D86085c21D0d773eF75661a74081C0065`
  > **Note:** The `beneficiary` address was taken from address index `2` in Ganache.
- Token purchase 2
  - `VALUE` => `40` and `Ether`
  - `beneficiary` => `0x8e5e57b2De2D520376c428A020adAB0b7B6Df860`
  > **Note:** The `beneficiary` address was taken from address index `1` in Ganache.
- Token purchase 3
  - `VALUE` => `20` and `Ether`
  - `beneficiary` => `0x34C1900E54F3849c39a9BC8202b6eE50C3567FA7`
  > **Note:** The `beneficiary` address was taken from address index `0` in Ganache.

The `VALUE` inputs are located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE. The `beneficiary` input is located in the `buyTokens` function of the `KaseiCoinCrowdsale` contract.

Upon clicking the `transact` button in the `buyTokens` function, a transaction confirmation prompt was provided by MetaMask.

#### Token purchase completed
![Optional: Token purchase completed](Evaluation_Evidence/optional_token_purchase_completed.png)  
Upon clicking the `Confirm` button in the Metamask prompt, the token purchase was completed.

#### Beneficiary confirmation
![Optional: Token purchase beneficiary confirmation](Evaluation_Evidence/optional_token_purchase_beneficiary_confirmation.png)  
Beneficiary confirmation of each token purchase was obtained using the `balanceOf` function of the `KaseiCoin` contract. The address entered in the `account` input was the `beneficiary` address used to initialize the token purchase. Upon clicking the `call` button in the `balanceOf` function, the value of the token purchase in Wei was displayed.
> **Note:** The Wei value of 40 Ether is 40000000000000000000.

#### Crowdsale confirmation
![Optional: Token purchase crowdsale confirmation](Evaluation_Evidence/optional_token_purchase_crowdsale_confirmation.png)  
Crowdsale confirmation of each token purchase was obtained using the `weiRaised` function of the `KaseiCoinCrowdsale` contract. Upon clicking the `weiRaised` button, the value of Wei raised from the purchase was displayed.
> **Note:** The value of Wei raised from all purchases was 100000000000000000000.

### Crowdsale finalized
![Optional: Crowdsale finalized](Evaluation_Evidence/optional_crowdsale_finalized.png)  
Once the crowdsale goal was reached and the close date had passed, the crowdsale was finalized using the `finalize` function in the `KaseiCoinCrowdsale` contract.

### Tokens withdrawn
![Optional: Tokens withdrawn](Evaluation_Evidence/optional_tokens_withdrawn.png)  
After finalizing the crowdsale, tokens were withdrawn using the `withdrawTokens` function in the `KaseiCoinCrowdsale` contract. Three withdrawals were performed using each of the addresses originally used for purchasing tokens.

### Tokens imported

| ![Optional: Tokens imported 01](Evaluation_Evidence/optional_tokens_imported_01.png) | ![Optional: Tokens imported 02](Evaluation_Evidence/optional_tokens_imported_02.png) |
| --- | --- |

To view the KaseiCoin in a MetaMask wallet, the token was first manually added to MetaMask using the `KaseiCoin` contract address. After confirming the manual addition by clicking the `Add custom token` button, the import was confirmed by clicking the `Import tokens` button on the subsequent screen.

### Ganache results
![Optional: Ganache results](Evaluation_Evidence/optional_ganache_results.png)  
The result of all contract functions performed was visible in the Ganache workspace.

### Process for buying KaseiCoin
The following instructions are strictly for buying KaseiCoin in Remix - Ethereum IDE, and assume the buyer has connected their wallet to Remix - Ethereum IDE.

#### Enter address and amount

| ![Optional: Token purchase initialized](Evaluation_Evidence/optional_token_purchase_initialized.png) | ![Optional: Token purchase confirmed](Evaluation_Evidence/optional_token_purchase_confirmed.png) |
| --- | --- |

To purchase KaseiCoin, a buyer must first enter their wallet address and the Ether value of the amount of KaseiCoin they wish to purchase. The buyer's wallet address must be entered into the `beneficiary` input located in the `buyTokens` function of the `KaseiCoinCrowdsale` contract, and their purchase amount must be entered in the `VALUE` inputs located in the `DEPLOY & RUN TRANSACTIONS` section of Remix - Ethereum IDE.
> In the demonstration, the buyer has entered the following information:
> - `VALUE` => `40` and `Ether`
> - `beneficiary` => `0xB218A34D86085c21D0d773eF75661a74081C0065`
> **Note:** The `beneficiary` address was taken from address index `2` in Ganache.

The buyer may then click the `transact` button in the `buyTokens` function, which will open a transaction confirmation prompt in MetaMask.

#### Token purchase completed
![Optional: Token purchase completed](Evaluation_Evidence/optional_token_purchase_completed.png)  
To confirm the transaction, the buyer must click the `Confirm` button in the Metamask prompt. Upon doing so, the token purchase is complete.

#### Beneficiary confirmation
![Optional: Token purchase beneficiary confirmation](Evaluation_Evidence/optional_token_purchase_beneficiary_confirmation.png)  
The buyer may confirm their purchase of KaseiCoin using the `balanceOf` function of the `KaseiCoin` contract. The address entered in the `account` input must be the address the buyer used to initialize the token purchase. Upon clicking the `call` button in the `balanceOf` function, the value of the buyer's token purchase in Wei is displayed.
> In the demonstration, the value of the buyer's token purchase in Wei is 40000000000000000000.

## Other information
- All work for the KaseiCoin contract can be found in the [KaseiCoin.sol](https://github.com/julianritchey/advanced-solidity-homework/blob/main/KaseiCoin.sol) file.
- All work for the KaseiCoinCrowdsale and KaseiCoinCrowdsaleDeployer contracts can be found in the [KaseiCoinCrowdsale.sol](https://github.com/julianritchey/advanced-solidity-homework/blob/main/KaseiCoinCrowdsale.sol) file.
- All screenshots used in this assignment can be found in the [Evaluation_Evidence](https://github.com/julianritchey/advanced-solidity-homework/tree/main/Evaluation_Evidence) folder.