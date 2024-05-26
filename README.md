# nft-transfer

This README outlines the steps to generate, store, deploy, and bridge a 5-item NFT collection using DALLE 2 or Midjourney, IPFS, Ethereum Testnet, and the Polygon Mumbai network.

## Table of Contents
1. [Introduction](#introduction)
2. [Prerequisites](#prerequisites)
3. [Generate and Store Images](#generate-and-store-images)
4. [Deploying the NFT Contract](#deploying-the-nft-contract)
5. [Mapping NFT Collection on Polygon](#mapping-nft-collection-on-polygon)
6. [Batch Minting NFTs](#batch-minting-nfts)
7. [Transferring NFTs to Polygon](#transferring-nfts-to-polygon)
8. [Testing on Polygon Mumbai](#testing-on-polygon-mumbai)
9. [Resources](#resources)

## Introduction
This guide will walk you through the process of creating a 5-item NFT collection, storing the images on IPFS, deploying an NFT contract on the Ethereum Testnet, and transferring the NFTs to the Polygon Mumbai network.

## Prerequisites
- Access to DALLE 2 or Midjourney for generating images
- An account on [pinata.cloud](https://pinata.cloud/) for storing items on IPFS
- Hardhat installed and configured
- MetaMask wallet installed and connected to Goerli Testnet and Polygon Mumbai
- Basic knowledge of Solidity and Ethereum development

## Generate and Store Images
1. **Generate Images:** Use DALLE 2 or Midjourney to generate 5 unique images for your collection.
2. **Store Images on IPFS:** 
   - Sign up for an account on [pinata.cloud](https://pinata.cloud/).
   - Upload the images to IPFS via Pinata and obtain the IPFS URLs for each image.

## Deploying the NFT Contract
1. **Create ERC721 or ERC1155 Contract:**
   - Write a smart contract with a `promptDescription` function that returns the prompt used to generate the images.
   - Example contract can be found in our detailed guide.
2. **Deploy to Testnet:**
   - Use Hardhat to deploy the contract.
   - Ensure the contract includes metadata linking to the IPFS URLs.

## Mapping NFT Collection on Polygon
1. **Map Your Collection:**
   - Use the Polygon network token mapper to visualize your NFT collection. This step is optional but helpful for tracking and managing your NFTs.

## Batch Minting NFTs
1. **Write a Hardhat Script:**
   - Use Hardhat and the ERC721A standard for optimal batch minting.
   - Script should mint all 5 NFTs in a single transaction.

## Transferring NFTs to Polygon
1. **Approve NFTs for Transfer:**
   - Write a script to approve the NFTs for transfer to the Polygon network using the FxPortal Bridge.
2. **Deposit NFTs to the Bridge:**
   - Use Hardhat to interact with the FxPortal Bridge contract to transfer NFTs from Ethereum to Polygon Mumbai.
3. **Test on Mumbai:**
   - Verify the NFTs have been transferred by checking the balance on the Polygon Mumbai network using `balanceOf`.

## Resources
- [Pinata Cloud](https://pinata.cloud/)
- [Hardhat Documentation](https://hardhat.org/getting-started/)
- [ERC721A Documentation](https://www.erc721a.org/)
- [FxPortal Bridge Documentation](https://docs.polygon.technology/docs/develop/ethereum-polygon/pos/getting-started/)

Follow this guide step-by-step to successfully create, deploy, and bridge your NFT collection from the Ethereum Goerli Testnet to the Polygon Mumbai network.
