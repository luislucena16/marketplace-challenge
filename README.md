# NFT Marketplace

This is a fullstack DApp NFT Marketplace built as a Challenge project about blockchain and smart contract development.  
Made with NodeJS, Hardhat, Solidity, ReactJS, NextJS.

# Market basic actions

You can `create` (mint) new tokens, uploading their image and metadata on [IPFS](https://ipfs.io/) using [Pinata](https://www.pinata.cloud/).  
If you've created or bought an NFT, you may also `sell` it by setting a price and paying a listing fee.  
When `buying` an NFT, the price will be transferred to the seller and the listing fee to the NFT Marketplace owner.  
It's also possible to `cancel` a market item, transferring it back to the owner.

# Easy Deployment

Frontend is automatically deployed using Vercel's Github integration, but contracts have to be manually deployed to keep a better control on them.  
However, new deployed contract addresses can be updated on the frontend simply by running a script that modifies Vercel's project environment variables and triggers a new frontend deployment.

# How to run

- Copy `.env.local.example` to `.env.local` and fill it with environment variables
- Run `npm run node` to start a local EVM blockchain testnet
- Run `npm run setup` to deploy NFT and Marketplace contracts and perform some initial actions to the local blockchain
- Run `npm run dev` to start frontend application
- Make sure to use `Localhost 8545` as the Metamask's network
- Make sure to import local Account #0 and #1 into Metamask accounts.

# Troubleshooting

## Mumbai marketplace setup command is breaking with a 'estimate gas failed' error

Try changing `hardhat.config.js` mumbai gas values.  
I'm using the ones I've found here:  
https://forum.moralis.io/t/deploy-to-polygon-matic-mumbai-fails/700

## Nouce is too high

Reset your Metamask account transaction history.  
Find out more on:  
https://medium.com/@thelasthash/solved-nonce-too-high-error-with-metamask-and-hardhat-adc66f092cd
