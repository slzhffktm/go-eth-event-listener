# Deploying Hello World Smart Contract

This is following the [Alchemy Hello World Smart Contract tutorial](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract).

## Getting Started

1. Follow step 1-5 from the [Alchemy tutorial](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract#create-and-deploy-your-smart-contract-using-hardhat)
2. Make sure you have `npm` installed
3. Run `npm install` to install the dependencies
4. Copy the `.env.example` file to `.env` and fill in the values, excluding the `CONTRACT_ADDRESS`
5. Compile the contract by running `npx hardhat compile`
6. Deploy the contract by running `npx hardhat run scripts/deploy.js --network goerli`
7. You should then see something like `Contract deployed to address: 0x6cd7d44516a20882cEa2DE9f205bF401c0d23570`
8. Copy the address and fill in the `CONTRACT_ADDRESS` in the `.env` file

Congrats! You just deployed a smart contract to the Ethereum chain 🎉

To understand what’s going on under the hood, let’s navigate to the Explorer tab in your [Alchemy dashboard](https://dashboard.alchemyapi.io/explorer).

## Interacting with The Deployed Smart Contract

This is following the [Alchemy interacting with a Smart Contract tutorial](https://docs.alchemy.com/alchemy/tutorials/hello-world-smart-contract/interacting-with-a-smart-contract).

We deployed our contract with the `initMessage = "Hello world!"` 

We are now going to read and print to console, then update the message stored in our smart contract.

- Go to `scripts/interact.js` and change the message at line 24 with the message you want to update to. 
  ```
    const tx = await helloWorldContract.update("<Put your new message here>");
  ```
- Run `npx hardhat run scripts/interact.js`

While you are running that script, you may notice that the `Updating the message...` 
step takes a while to load before the new message is set. That is due to the mining process!

Congrats! You just interacted with the smart contract that you deployed! 🎉
