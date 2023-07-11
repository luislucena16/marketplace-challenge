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

# How to deploy

- Set ACCOUNT_PRIVATE_KEY in `.env.local` and send it some Polygon's Testnet [Matic](https://faucet.polygon.technology/) tokens
- Run `npm run deploy:mumbai` to deploy contracts to Polygon`s Testnet (Mumbai)
- Do the same for ACCOUNT2_PRIVATE_KEY env and run `npm run setup-marketplace:mumbai` to setup the marketplace with existing tokens and sales.
- Add in `.env.local` your contract address of NFT and Marketplace, or copy and use this addresses:
```bash
MARKETPLACE_CONTRACT_ADDRESS_MUMBAI=0xA6D779781E15FAe73809F8Bafc48cC859013Ca2d
NFT_CONTRACT_ADDRESS_MUMBAI=0x433f2605CD7d4671C2466EB35Aba6C30d753ee00
```
- Make sure to use `Polygon Testnet Mumbai` as Metamask's network

# Running test

- `npm run test`

# Clean cache

- `npx hardhat clean`

# Troubleshooting
## Nouce is too high

Reset your Metamask account transaction history:

- Go to `Settings`
- Then to `Advanced`
- Finally to `Clear activity tab data`