# HomeWork21
Unit 21: You sure can attract a crowd!
![image](https://user-images.githubusercontent.com/68974271/110379673-1f2b2a80-8025-11eb-9052-a15a8a8d4ba7.png)


Background
Your company has decided to crowdsale their PupperCoin token in order to help fund the network development.
This network will be used to track the dog breeding activity across the globe in a decentralized way, and allow humans to track the genetic trail of their pets. You have already worked with the necessary legal bodies and have the green light on creating a crowdsale open to the public. However, you are required to enable refunds if the crowdsale is successful and the goal is met, and you are only allowed to raise a maximum of 300 Ether. The crowdsale will run for 24 weeks.
You will need to create an ERC20 token that will be minted through a Crowdsale contract that you can leverage from the OpenZeppelin Solidity library.
This crowdsale contract will manage the entire process, allowing users to send ETH and get back PUP (PupperCoin).
This contract will mint the tokens automatically and distribute them to buyers in one transaction.
It will need to inherit Crowdsale, CappedCrowdsale, TimedCrowdsale, RefundableCrowdsale, and MintedCrowdsale.
You will conduct the crowdsale on the Kovan or Ropsten testnet in order to get a real-world pre-production test in.

Instructions

Creating your project
Using Remix, create a file called PupperCoin.sol and create a standard ERC20Mintable token. Since you're already an expert at this, you can simply use this starter code.
![image](https://user-images.githubusercontent.com/68974271/110378319-73350f80-8023-11eb-96cb-01161b9d1663.png)

Create a new contract named PupperCoinCrowdsale.sol, and prepare it like a standard crowdsale.
![image](https://user-images.githubusercontent.com/68974271/110378395-8f38b100-8023-11eb-8541-116d54ae5428.png)

Designing the contracts

ERC20 PupperCoin
You will need to simply use a standard ERC20Mintable and ERC20Detailed contract, hardcoding 18 as the decimals parameter, and leaving the initial_supply parameter alone.
You don't need to hardcode the decimals, however since most use-cases match Ethereum's default, you may do so.
Simply fill in the PupperCoin.sol file with this starter code, which contains the complete contract you'll need to work with in the Crowdsale.

PupperCoinCrowdsale
Leverage the Crowdsale starter code, saving the file in Remix as Crowdsale.sol.
You will need to bootstrap the contract by inheriting the following OpenZeppelin contracts:


Crowdsale


MintedCrowdsale


CappedCrowdsale


TimedCrowdsale


RefundablePostDeliveryCrowdsale



PupperCoinCrowdsaleDeployer
In this contract, you will model the deployment based off of the ArcadeTokenCrowdsaleDeployer you built previously. Leverage the OpenZeppelin Crowdsale Documentation for an example of a contract deploying another, as well as the starter code provided in Crowdsale.sol.
![image](https://user-images.githubusercontent.com/68974271/110378653-d626a680-8023-11eb-9907-33f1c92c8ae6.png)
Or look at vi1
![image](https://user-images.githubusercontent.com/68974271/110378841-17b75180-8024-11eb-8c58-a88a7ad7b9f6.png)
Or look at vi2

Testing the Crowdsale
Test the crowdsale by sending Ether to the crowdsale from a different account (not the same account that is raising funds)
![image](https://user-images.githubusercontent.com/68974271/110378932-34538980-8024-11eb-99ba-20da528fe35b.png)
Or look at vi3




Deploy the crowdsale to the Kovan or Ropsten testnet, and store the deployed address for later. Switch MetaMask to your desired network, and use the Deploy tab in Remix to deploy your contracts. Take note of the total gas cost, and compare it to how costly it would be in reality. Since you are deploying to a network that you don't have control over, faucets will not likely give out 300 test Ether. You can simply reduce the goal when deploying to a testnet to an amount much smaller, like 10,000 wei.

![image](https://user-images.githubusercontent.com/68974271/110379166-77adf800-8024-11eb-9f44-ce091d846cda.png)
Or look at vi4
![image](https://user-images.githubusercontent.com/68974271/110379227-8d232200-8024-11eb-958e-b92040e25beb.png)
Or look at vi5

Submission
Create a Github repo, and a README.md file explaining the process for purchasing PupperCoin (or whatever name you came up with).
Also, please provide screenshots to illustrate the functionality (e.g. how you send Ether to the contract, how you add the token to MyCrypto and test a transaction, and how you test the time functionality etc.). Alternatively, you can also record your interactions with the contract as a gif (e.g. https://www.screentogif.com/)
Ensure that anyone can run the steps and add the token to MyCrypto, or a similar wallet.
Include information such as the token parameters, token name, crowdsale cap, etc.
