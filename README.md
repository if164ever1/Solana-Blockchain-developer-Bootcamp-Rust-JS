# Solana Blockchain Developer Bootcamp with Rust and JavaScript

Welcome to the **Solana Blockchain Developer Bootcamp with Rust and JavaScript** repository! This repository includes various projects that will help you dive deep into blockchain development on the Solana network using Rust, JavaScript, and other essential tools. Whether you are just starting or looking to improve your skills, this repository will provide you with all the necessary resources and projects to build decentralized applications (dApps) on Solana.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation Instructions](#installation-instructions)
  - [System Requirements](#system-requirements)
  - [Install Node.js and NPM](#install-nodejs-and-npm)
  - [Install Solana CLI](#install-solana-cli)
  - [Install Rust](#install-rust)
- [Project Breakdown](#project-breakdown)
  - [Airdrop Project (Sola)](#airdrop-project-sola)
- [Project Setup](#project-setup)
  - [Running the Airdrop Project](#running-the-airdrop-project)
  - [Testing & Development](#testing--development)
- [Resources](#resources)
- [Contributing](#contributing)
- [License](#license)

---

## Prerequisites

Before diving into the projects, you need to ensure that your development environment is set up properly. You will be working with Solana's blockchain, so you'll need to install a few key tools and packages.

### System Requirements

- **Operating System**: Linux, macOS, or Windows Subsystem for Linux (WSL)
- **Hardware**: Minimum 4GB RAM, 10GB disk space (for Solana CLI tools and running a local validator, if necessary)
- **Internet**: Stable connection for downloading dependencies and interacting with the Solana blockchain

---

## Installation Instructions

Follow the steps below to install all necessary tools.

### Install Node.js and NPM

1. **Install Node.js**:
   - Node.js is a JavaScript runtime used to run JavaScript code on the server-side and interact with Solana blockchain.
   - Visit the [Node.js official site](https://nodejs.org/) and download the LTS version (Long-Term Support).

2. **Verify the Installation**:
   Open your terminal and run the following commands to verify that Node.js and NPM are installed:

   ```bash
   node -v
   npm -v
   ```

   If both commands return a version number, you've installed them correctly.

### Install Solana CLI

Solana CLI is required for interacting with the Solana blockchain directly from your command line.

1. **Install Solana CLI**:
   Run the following command to install Solana CLI:

   ```bash
   sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
   ```

2. **Verify the Installation**:
   Run this command to verify the Solana CLI installation:

   ```bash
   solana --version
   ```

   It should return the current version of Solana.

### Install Rust

Rust is used for developing on Solana's blockchain (smart contracts, on-chain programs, etc.). You'll need to install Rust to start writing your Solana programs.

1. **Install Rust**:
   Visit the official Rust website: [Rust Install](https://www.rust-lang.org/tools/install) or run the following command:

   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

2. **Verify the Installation**:
   Run the following command to check that Rust is installed properly:

   ```bash
   rustc --version
   ```

---

## Project Breakdown

This repository includes several key projects. Let's start with the **Airdrop Project (Sola)**.

### Airdrop Project (Sola)

The **Airdrop Project (Sola)** is a basic Solana dApp built to distribute tokens to multiple wallet addresses. It demonstrates how to interact with the Solana blockchain using JavaScript and the Solana Web3.js library. This project will give you a hands-on understanding of Solana's token system, wallet management, and basic transactions.

---

## Project Setup

### Running the Airdrop Project

To run the **Airdrop Project (Sola)**, follow these steps:

1. **Clone the Repository**:
   If you haven’t already cloned the repository, run the following command:

   ```bash
   git clone https://github.com/yourusername/solana-blockchain-bootcamp.git
   ```

2. **Navigate to the Project Directory**:
   
   ```bash
   cd solana-blockchain-bootcamp/airdrop-project
   ```

3. **Install the Project Dependencies**:
   Use NPM to install all necessary dependencies for the project:

   ```bash
   npm install
   ```

4. **Configure the Solana CLI**:
   Before running the airdrop script, ensure that your Solana CLI is configured with a wallet and testnet (or devnet) network. You can set the Solana cluster with the following command:

   ```bash
   solana config set --url devnet
   ```

   Check your Solana configuration with:

   ```bash
   solana config get
   ```

5. **Fund Your Wallet (Devnet) for Testing**:
   If you’re using Solana’s Devnet, you can request airdrop tokens to your wallet for testing purposes. Run:

   ```bash
   solana airdrop 2
   ```

   This will send 2 SOL to your wallet on the devnet.

6. **Run the Airdrop Script**:
   Once everything is set up, you can run the airdrop script to distribute tokens to various addresses. Ensure you have the `recipientAddresses.json` file configured with the addresses to which the airdrop should be sent.

   To start the airdrop:

   ```bash
   npm run airdrop
   ```

   The script will interact with Solana's blockchain and perform the airdrop operation.

---

## Testing & Development

1. **Unit Testing**:
   Unit testing in Solana is typically done using `mocha` and `chai` in JavaScript. For Rust-based projects, you can write tests using Solana's test framework.

2. **Run Tests**:
   To run the tests for your project, run:

   ```bash
   npm test
   ```

3. **Deploying to Solana**:
   Once you’re ready to deploy your project, you can use the Solana CLI to deploy the smart contracts you’ve written in Rust, or interact with Solana's blockchain directly from JavaScript.

   Example to deploy a Solana smart contract:

   ```bash
   solana program deploy /path/to/your/compiled_program.so
   ```

---

## Resources

- **Solana Documentation**: [https://docs.solana.com](https://docs.solana.com)
- **Solana Web3.js Documentation**: [https://solana-labs.github.io/solana-web3.js/](https://solana-labs.github.io/solana-web3.js/)
- **Rust Documentation**: [https://doc.rust-lang.org/](https://doc.rust-lang.org/)

---

## Contributing

We welcome contributions to this repository. If you have suggestions or improvements, please feel free to fork the repository and submit a pull request. You can also open an issue for any bugs or questions.

To contribute:

1. Fork this repository
2. Create a new branch (`git checkout -b feature-name`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add feature'`)
5. Push to the branch (`git push origin feature-name`)
6. Open a pull request

---

## License

This repository is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

Special thanks to the Solana community and the developers who have contributed to the Solana ecosystem. This bootcamp is designed to empower developers to understand blockchain development on Solana, and we hope you find the resources useful!
