# Advanced ERC20 Token Implementation with Hardhat

A highly secure, gas-optimized, and fully compliant ERC20 smart contract implementation written in Solidity ^0.8.27. This project demonstrates advanced ownership management, custom error handling, and a robust deployment pipeline using Hardhat and Ethers.js v6.

## 🚀 Key Features

- **Full ERC20 & ERC165 Compliance:** Implements all standard functions and interface detection.
- **Two-Step Ownership Transfer:** Secure `setPendingOwner` and `changeOwner` mechanism to prevent accidental ownership loss.
- **Advanced Security:**
  - Zero-Address Protection across all critical functions.
  - Custom Errors (e.g., `OnlyOwner`, `ZerpPendingOwner`) for gas-efficient reverts.
  - Overflow/Underflow protection using Solidity 0.8+ native checks.
- **Gas Optimization:** Utilizes `unchecked` blocks for safe arithmetic operations to reduce gas consumption.
- **Mint/Burn Mechanics:** Owner-exclusive minting and user-initiated token burning.

## 🛠️ Tech Stack

- **Smart Contracts:** Solidity ^0.8.27
- **Development Environment:** Hardhat
- **Blockchain Interaction:** Ethers.js v6
- **Language:** TypeScript / JavaScript

## 📂 Project Structure

- `contracts/`: Contains the core Solidity smart contracts (`ERC20.sol`, interfaces).
- `scripts/`: Deployment scripts (e.g., `deploy.js`) for interacting with testnets/mainnet.
- `hardhat.config.ts`: Network configurations, compiler settings, and plugin integrations.

## ⚙️ Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn

### Installation
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd <repo-name>
