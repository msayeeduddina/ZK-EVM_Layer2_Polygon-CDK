# README

## Overview

This guide walks you through creating your own ZK-powered Layer 2 blockchain using the Polygon Chain Development Kit (CDK). Specifically, it covers how to deploy a ZK-EVM Validium chain with Polygon CDK, deploy smart contracts on it, and build decentralized applications (dApps) that interact with your chain.

## Technologies Used

- **Polygon CDK**: A toolkit for creating custom Layer 2 chains with Polygon's underlying technology.
- **ZK-EVM Validium**: Zero-Knowledge Ethereum Virtual Machine using Validium data availability.
- **Gateway FM**: Implementation provider to deploy and manage your blockchain infrastructure.
- **Thirdweb CLI**: Tool to create and deploy smart contracts.
- **Hardhat**: Ethereum development environment for compiling, testing, and deploying smart contracts.
- **Metamask**: Wallet to interact with the blockchain.

## Prerequisites

- Google account for signing into Gateway FM.
- Node.js (preferably version 18, managed via NVM if needed).
- Yarn or npm package manager.
- Metamask wallet installed in your browser.
- Visual Studio Code or any preferred code editor.

## Step 1: Deploy Your Layer 2 Blockchain

1. Visit the [Polygon CDK GitHub repository](https://github.com/polygon-technology/polygon-cdk) to explore the source code and documentation.
2. Instead of manual deployment, use an implementation partner like **Gateway FM** for easier deployment.
3. Sign up or log in to Gateway FM using your Google account.
4. In the Gateway FM dashboard, click **Add New** to create a new chain.
5. Select the desired chain customization:
   - Choose **Validium on Ethereum** testnet.
   - Select hosting environment (e.g., "Stockhome" or "On-premise").
   - Choose **ETH** as the default gas token.
6. Click **Create** to start deployment.
7. Wait a few minutes while Gateway FM provisions your blockchain infrastructure on AWS or your chosen cloud provider.
8. Once deployed, you will receive an email confirmation and see your chain details on the Gateway FM dashboard, including RPC endpoints, chain ID, faucet, bridge, and block explorer URLs.

## Step 2: Set Up Smart Contract Development Environment

1. Open your terminal and run:

   ```bash
   npx thirdweb@latest create contract
   ```

2. Follow the prompts:
   - Update CLI if requested.
   - Choose your project name (e.g., `contract`).
   - Select **Hardhat** as the development environment.
   - Choose to start with an empty contract.

3. If you encounter Node.js version issues, use NVM to switch to Node.js 18:

   ```bash
   nvm install 18
   nvm use 18
   ```

4. Install dependencies with Yarn or npm inside your project directory:

   ```bash
   yarn install
   # or
   npm install
   ```

5. Open the project in your code editor. Inside the `contracts` folder, you will find a Solidity contract file (e.g., `Contract.sol`).

6. Replace the empty contract with your own Solidity smart contract code or use the example "Grea" contract provided.

## Step 3: Deploy Your Smart Contract to Your Chain

1. In your project directory, deploy the contract using:

   ```bash
   yarn deploy
   # or
   npm run deploy
   ```

2. This will compile your contract and generate a deployment command.
3. The deployment process will open the Thirdweb dashboard in your browser.
4. Connect your wallet (e.g., Metamask) and sign in.
5. Fill in any constructor parameters if required.
6. Select your deployed Layer 2 chain as the target network.
7. Confirm the deployment transaction.

## Step 4: Interact with Your Blockchain and DApps

- Use the Gateway FM dashboard to access RPC URLs, block explorer, faucet, and bridge.
- Develop decentralized applications that connect to your chain using standard Ethereum tools and libraries since your chain is EVM-compatible.
- Deploy additional smart contracts or upgrade existing ones as needed.

## Additional Resources

- For in-depth understanding of Polygon 2.0, Polygon CDK, and the interrupt layer connecting L2 chains, refer to Polygon's official documentation and related videos.
- Reach out to the Polygon team or implementation partners for tailored support and advanced customization.
- Explore the Polygon CDK repositories on GitHub for source code and contribution opportunities.

---

This README provides a comprehensive step-by-step process to create, deploy, and interact with your own ZK-powered Layer 2 blockchain using Polygon CDK and related tools.