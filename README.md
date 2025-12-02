# Orbion Network Smart Contract

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Solidity](https://img.shields.io/badge/Solidity-0.8.28-blue.svg)](https://soliditylang.org/)
[![Hardhat](https://img.shields.io/badge/Hardhat-3.0.6-orange.svg)](https://hardhat.org/)

A comprehensive ERC-20 token implementation for the Orbion Network, designed with a validator-first philosophy and full EVM compatibility. This project provides a robust foundation for decentralized applications, governance systems, and network-level innovation.

## 🌐 Project Links

- **Website**: [https://orbionchain.com/](https://orbionchain.com/)
- **Telegram**: [https://t.me/OrbionNetwork](https://t.me/OrbionNetwork)
- **Twitter**: [https://x.com/OrbionNetwork](https://x.com/OrbionNetwork)

## 📋 Table of Contents

- [Features](#features)
- [Token Specifications](#token-specifications)
- [Smart Contract Features](#smart-contract-features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Testing](#testing)
- [Deployment](#deployment)
- [Architecture](#architecture)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## ✨ Features

- **ERC-20 Compliant**: Full implementation of the ERC-20 standard
- **Automated Market Maker Integration**: Built-in Uniswap V2 integration
- **Dynamic Fee Structure**: Configurable buy/sell fees with maximum limits
- **Anti-Whale Protection**: Maximum wallet and transaction limits
- **Automated Liquidity Management**: Automatic token-to-BNB conversion and marketing wallet distribution
- **Fee Exemption System**: Configurable fee exemptions for specific addresses
- **Ownership Management**: Secure ownership transfer and renunciation capabilities
- **Hardhat Development Environment**: Complete development, testing, and deployment setup

## 🪙 Token Specifications

| Property | Value |
|----------|-------|
| **Name** | Orbion Network |
| **Symbol** | ORB |
| **Decimals** | 18 |
| **Total Supply** | 100,000,000 ORB |
| **Network** | BSC (Binance Smart Chain) |
| **Contract Address** | [Verified on BscScan](https://bscscan.com/) |

## 🔧 Smart Contract Features

### Fee Management
- **Buy Fee**: 15% (configurable, max 30%)
- **Sell Fee**: 15% (configurable, max 30%)
- **Fee Exemptions**: Owner, contract, and marketing addresses
- **Dynamic Fee Updates**: Owner can modify fees within limits

### Transaction Limits
- **Max Wallet Hold**: 2% of total supply
- **Max Transaction**: 2% of total supply
- **Configurable Limits**: Owner can adjust limits as needed

### Automated Features
- **Auto-Liquidity**: Automatic conversion of collected fees to BNB
- **Marketing Distribution**: Automatic BNB distribution to marketing wallet
- **Swap Trigger**: Configurable transaction count before liquidity processing

## 🛠 Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- [Git](https://git-scm.com/)

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone <this-repo-url>
   cd Orbion-Network-smart-contract
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Verify installation**
   ```bash
   npx hardhat --version
   ```

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the root directory:

```env
SEPOLIA_RPC_URL=your_sepolia_rpc_url
SEPOLIA_PRIVATE_KEY=your_private_key
```

### Hardhat Configuration

The project is configured for multiple networks:

- **Hardhat Mainnet**: EDR-simulated L1 chain
- **Hardhat OP**: EDR-simulated Optimism chain
- **Sepolia**: Ethereum testnet

## 🚀 Usage

### Compile Contracts
```bash
npx hardhat compile
```

### Run Tests
```bash
npx hardhat test
```

### Deploy Contracts
```bash
# Deploy to local network
npx hardhat ignition deploy ignition/modules/Counter.ts --network hardhat

# Deploy to Sepolia testnet
npx hardhat ignition deploy ignition/modules/Counter.ts --network sepolia
```

### Run Scripts
```bash
# Send OP transaction
npx hardhat run scripts/send-op-tx.ts --network hardhatOp
```

## 🧪 Testing

The project includes comprehensive test suites:

- **Unit Tests**: Core functionality testing
- **Integration Tests**: Contract interaction testing
- **Event Testing**: Event emission verification

Run tests with:
```bash
npm test
```

## 🏗 Architecture

### Contract Structure

```
OrbionNetwork.sol
├── IERC20 Interface
├── SafeMath Library
├── Address Library
├── Context Abstract Contract
├── Ownable Abstract Contract
├── Uniswap V2 Interfaces
└── OrbionNetwork Main Contract
```

### Key Components

1. **Token Management**: ERC-20 standard implementation
2. **Fee System**: Dynamic fee calculation and collection
3. **Liquidity Management**: Automated Uniswap integration
4. **Access Control**: Owner-based permission system
5. **Anti-Whale Protection**: Transaction and wallet limits

## 🔒 Security

### Security Features

- **Ownership Control**: Secure ownership management
- **Fee Limits**: Maximum fee caps to prevent abuse
- **Input Validation**: Comprehensive parameter validation
- **Reentrancy Protection**: Lock mechanisms for critical functions
- **Access Control**: Role-based function access

### Audit Status

- Contract verified on BscScan
- MIT License for open-source transparency
- Community review encouraged

## 📁 Project Structure

```
├── contracts/
│   └── OrbionNetwork.sol          # Network contract
├── hardhat.config.ts              # Hardhat configuration
├── package.json                   # Dependencies
├── tsconfig.json                  # TypeScript configuration
└── README.md                      # Readme
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow Solidity style guidelines
- Add tests for new features
- Update documentation as needed
- Ensure all tests pass before submitting

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


---

**Disclaimer**: This software is provided "as is" without warranty. Use at your own risk. Always conduct thorough testing before deploying to mainnet.