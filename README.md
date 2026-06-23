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
- Full ERC20 Compliance: Implements all standard ERC20 functions and events
- ERC20Metadata Support: Includes name, symbol, and decimals functionality
- ERC165 Interface Detection: Supports interface identification standard
- Two-Step Ownership Transfer: Secure ownership management with pending owner mechanism
- Mint/Burn Functionality: Owner can mint tokens, users can burn their own tokens
- Advanced Security: Comprehensive input validation and custom error handling
- Zero Address Protection: Prevents transfers to/from zero addresses
- Balance & Allowance Checks: Built-in validation for sufficient balances and allowances
- Gas Optimized: Uses unchecked arithmetic where safe for gas efficiency
    

## 🛠️ Tech Stack

- **Smart Contracts:** Solidity ^0.8.27
- **Development Environment:** Hardhat
- author: geniusnight
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

   # 🚀 Advanced ERC20 Token Implementation

[![Solidity](https://img.shields.io/badge/Solidity-%5E0.8.27-blue?logo=solidity)](https://soliditylang.org/)
[![Hardhat](https://img.shields.io/badge/Hardhat-2.19.0-orange?logo=ethereum)](https://hardhat.org/)
[![Ethers.js](https://img.shields.io/badge/Ethers.js-v6-blue?logo=ethereum)](https://docs.ethers.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<div align="center">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge" alt="Status">
</div>

---

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Architecture](#-architecture)
- [Installation](#-installation)
- [Usage](#-usage)
- [Smart Contract Diagram](#-smart-contract-diagram)
- [Security](#-security)
- [License](#-license)

---

## 🔍 About

This project implements a **production-grade ERC20 token** with advanced security features, gas optimization, and comprehensive ownership management. Built with Solidity ^0.8.27 and deployed using Hardhat.

**Key Highlights:**
- ✅ Full ERC20 & ERC165 Compliance
- ✅ Two-Step Ownership Transfer
- ✅ Custom Error Handling (Gas Optimized)
- ✅ Mint/Burn Functionality
- ✅ Zero Address Protection

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔐 **Security** | Comprehensive input validation, zero address protection, and custom errors |
| ⚡ **Gas Optimized** | Uses `unchecked` blocks and custom errors for minimal gas consumption |
| 🔄 **Upgradeable** | Two-step ownership transfer prevents accidental ownership loss |
| 📊 **Metadata** | Full ERC20Metadata support (name, symbol, decimals) |
| 🔥 **Burn Mechanism** | Users can burn their own tokens |

---

## 🏗️ Architecture

```mermaid
graph TD
    A[ERC20 Contract] --> B[IERC20 Interface]
    A --> C[IERC165 Interface]
    A --> D[IERC20Metadata Interface]
    A --> E[IERC6093 Errors]
    A --> F[Context Utility]
    
    B --> G[Standard ERC20 Functions]
    C --> H[Interface Detection]
    D --> I[Token Metadata]
    
    G --> J[transfer]
    G --> K[transferFrom]
    G --> L[approve]
    G --> M[balanceOf]
    
    style A fill:#3FE0C5,stroke:#101010,stroke-width:3px
    style B fill:#FFD700,stroke:#101010
    style C fill:#FFD700,stroke:#101010
    style D fill:#FFD700,stroke:#101010
