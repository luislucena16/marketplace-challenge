# NFT Marketplace

This is a fullstack DApp NFT Marketplace built as a Challenge project about blockchain and smart contract development.  
Made with NodeJS, Hardhat, Solidity, ReactJS, NextJS.

# Market basic actions

You can `create` (mint) new tokens, uploading their image and metadata on [IPFS](https://ipfs.io/) using [Pinata](https://www.pinata.cloud/).  
If you've created or bought an NFT, you may also `sell` it by setting a price and paying a listing fee.  
When `buying` an NFT, the price will be transferred to the seller and the listing fee to the NFT Marketplace owner.  
It's also possible to `cancel` a market item, transferring it back to the owner.

# Easy Deployment

Contracts have to be manually deployed to keep a better control on them. By having the contracts deployed you can interact with the frontend automatically.
Follow the instructions:

# How to run

- Copy `.env.local.example` to `.env.local` and fill it with environment variables
- Run `npm run node` to start a local EVM blockchain testnet
- Run `npm run setup` to deploy NFT and Marketplace contracts and perform some initial actions to the local blockchain
- Run `npm run dev` to start frontend application
- Make sure to use `Localhost 8545` as the Metamask's network
- Make sure to import local Account #0 and #1 into Metamask accounts.

# Running test

Use `npm run test`

# Troubleshooting
## Nouce is too high

Reset your Metamask account transaction history:

- Go to `Settings`
- Then to `Advanced`
- Finally to `Clear activity tab data`