# CrowdFunder DApp

This repository contains the full decentralized application (DApp) for CrowdFunder, including both the smart contract backend and the React frontend. The `smart_contract` folder holds the Solidity smart contracts and Hardhat configuration, while the `client` folder contains the React application for interacting with the smart contracts.

## Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/en/)
- [Yarn](https://yarnpkg.com/getting-started/install) 
- An Ethereum wallet like [MetaMask](https://metamask.io/) configured for the Sepolia network.

## Setting Up the Environment

1. Clone this repository and navigate into it:
   ```bash
   git clone https://your-repository-url.git
   cd your-repository-directory
   ```

2. Install dependencies in both the smart contract and client directories:
   ```bash
   # Install dependencies for the smart contract
   cd smart_contract
   npm install

   # Install dependencies for the client
   cd ../client
   npm install
   ```

## Smart Contract Usage

### Configuration

1. Copy the `.env.example` file to a new file named `.env` and fill in the necessary environment variables:
   ```plaintext
   PRIVATE_KEY=<Your-Sepolia-Wallet-Private-Key>
   ETHERSCAN_API=<Your-Etherscan-API-Key>
   ```

### Compiling the Contract

1. Navigate to the `smart_contract` folder and run the following command to compile the smart contract:
   ```bash
   npx hardhat compile
   ```

### Deploying the Contract

1. To deploy the contract to the Sepolia network:
   ```bash
   npx hardhat run scripts/deploy.js --network sepolia
   ```
   Note the contract address output by this script; you'll need it for the client setup.

## Client Application Setup

### Configuring the Contract Address

1. In the `client` directory, navigate to the `src/constants/index.jsx` file.
2. Open the file and update it with the contract address you obtained during the deployment.

### Starting the React Application

1. Make sure you are still in the `client` directory.
2. Start the React development server:
   ```bash
   npm start
   ```
   This will launch the application on [http://localhost:3000](http://localhost:3000).

### Interacting with the DApp

1. Ensure your MetaMask is connected to the Sepolia network.
2. Use the React application to interact with your deployed smart contract.


