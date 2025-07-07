# Foundry FundMe Project

A fully tested and configurable **FundMe** smart contract built using the **Foundry framework**, utilizing **Chainlink price feeds**, and integrated with **mock deployments** for local testing environments.

**Created by: [Manzoor](https://github.com/Manzoorblockchaindev)** — a dedicated **class 9 student** who is actively learning **blockchain development** and building real Web3 projects to gain hands-on experience 


---

## Project Overview

This smart contract allows users to fund the contract with **ETH**. It uses **Chainlink price feeds** to ensure users contribute **at least $5 USD** worth of ETH. Only the contract **owner** can withdraw the funds.

### Key Highlights:
- Chainlink price feed integration (Mainnet, Sepolia, or mocked locally)
- Gas-optimized withdrawal via `cheapWithdraw`
- Full test coverage with Foundry’s testing tools
- Scripts for deployment, funding, and withdrawal

---

## Features

- ✅ Minimum $5 funding in USD (via Chainlink)
- ✅ Owner-only withdrawal with error handling
- ✅ Gas-optimized `cheapWithdraw()` function
- ✅ `fallback()` and `receive()` to handle ETH
- ✅ Automated deploy/fund/withdraw scripts
- ✅ Unit + Integration tests with mocks

---

## Quick Start

### Prerequisites

- [Foundry](https://book.getfoundry.sh/)
- Git & Node.js
- (Optional) RPC provider like Sepolia

### Install

```bash
git clone https://github.com/Manzoorblockchaindev/foundry-fundme.git
cd foundry-fundme
forge install

### Run Tests

```bash
forge test

### Deploy Locally

anvil
forge script script/DeployFundMe.s.sol --fork-url http://127.0.0.1:8545 --broadcast --ffi

### Deploy to Sepolia
forge script script/DeployFundMe.s.sol --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY --broadcast --verify

