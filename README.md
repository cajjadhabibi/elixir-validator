
# elixir-validator
Here's a simplified and GitHub-ready version of the Elixir Testnet v3 Validator Setup Guide:
# Elixir Testnet v3 Validator Setup Guide

## Overview
This guide explains how to set up a validator on the Elixir Network's Testnet v3 to support secure and effective orderbook construction.

## Requirements
- **Hardware**: 8GB RAM, 100GB storage, reliable 100Mbit internet.
- **Software**: Docker installed and running.

## Setup Steps

### 1. Generate a Private Key
Create a new wallet using MetaMask and export the private key. This key will be used exclusively for the validator.

### 2. Configure Validator Environment
Download the [validator environment template](#) and edit it with the following details:
- **STRATEGY_EXECUTOR_DISPLAY_NAME**: Public-facing name.
- **STRATEGY_EXECUTOR_BENEFICIARY**: Wallet address for receiving rewards.
- **SIGNER_PRIVATE_KEY**: Your generated private key (without `0x`).

### 3. Validator Enrollment
- **Mint MOCK Tokens**: Use Sepolia ETH to mint 1,000 MOCK tokens on the Elixir Dashboard.
- **Stake Tokens**: Approve and stake your MOCK tokens.
- **Enroll Validator**: Delegate your validator on the Elixir Dashboard.

### 4. Run Validator
Pull the Docker image and start the validator:
```bash
docker pull elixirprotocol/validator:v3
docker run -d --env-file /path/to/validator.env --name elixir --restart unless-stopped elixirprotocol/validator:v3
5. Optional Configurations
Apple/ARM Silicon: Add --platform linux/amd64.
Health Checks & Metrics: Open port 17690.
6. Upgrade Validator
To upgrade, stop the container, pull the latest image, and restart the validator.

Support
Discord: Join the community for announcements and peer support.
Bug Reports: Submit issues via the Testnet v3 Issue Tracker.

This guide is now streamlined for publication on GitHub and includes essential setup instructions.
