# 🎨 Ethereum NFT Marketplace

A full-featured decentralized NFT marketplace built with React, TypeScript, Moralis, and Web3. This platform enables users to mint, list, buy, and sell NFTs with support for multiple collections and ERC20 tokens.

## ✨ Features

### For Users
- 🔐 **Web3 Authentication** - Connect with MetaMask, WalletConnect, or Web3Auth
- 🖼️ **NFT Gallery** - Browse and view your NFT collection
- 🛒 **NFT Marketplace** - Buy and sell NFTs with ease
- 💰 **Multi-Currency Support** - Trade with native tokens or ERC20 tokens
- 📊 **User Dashboard** - Track your NFTs and transaction history
- 🔍 **NFT Balance Tracking** - Real-time balance updates across chains

### For Admins
- 🎯 **Protocol Management** - Deploy and manage marketplace contracts
- 🏭 **NFT Collection Factory** - Create and deploy new NFT collections
- 🪙 **Token Factory** - Deploy custom ERC20 tokens
- 📝 **NFT Minting** - Mint NFTs with IPFS metadata storage
- 📋 **Module System** - Add and manage marketplace modules
- 👑 **Role-Based Access Control** - Granular permission management
- 💸 **Royalty Withdrawal** - Collect marketplace fees and royalties

## 🛠️ Tech Stack

- **Frontend**: React 17, TypeScript
- **Web3**: Moralis SDK, Web3.js, React-Moralis
- **UI Framework**: Ant Design (antd), Web3UIKit, Styled Components
- **Wallet Integration**: MetaMask, WalletConnect, Web3Auth, Magic SDK
- **Storage**: IPFS (via Moralis)
- **Smart Contracts**: ERC721, ERC20, Marketplace Protocol
- **Routing**: React Router v5

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm or yarn
- MetaMask or another Web3 wallet
- A Moralis account ([Sign up here](https://moralis.io))

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/superdev947/ethereum-nft-marketplace.git
cd ethereum-nft-marketplace
```

### 2. Install Dependencies

```bash
npm install
# or
yarn install
```

### 3. Configure Moralis

1. Create an account at [Moralis.io](https://moralis.io)
2. Create a new Moralis server
3. Copy your server URL and Application ID
4. Update your Moralis credentials in `src/index.tsx`

### 4. Start the Development Server

```bash
npm start
# or
yarn start
```

The application will open at [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
ethereum-nft-marketplace/
├── public/                    # Static files
├── src/
│   ├── components/           # Reusable React components
│   │   ├── AdminRoute.tsx   # Protected admin routes
│   │   └── HeaderMenu.tsx   # Navigation header
│   ├── views/
│   │   └── Admin/           # Admin panel
│   │       ├── Dashboard/   # Admin dashboard
│   │       ├── Forms/       # Contract deployment forms
│   │       │   ├── MarketplaceForm.tsx
│   │       │   ├── NFTMinter.tsx
│   │       │   ├── NFTLister.tsx
│   │       │   └── TokenForm.tsx
│   │       └── Module/      # Module management
│   │           ├── contracts/    # Smart contract hooks
│   │           └── Adder/       # Module addition UI
│   ├── web3Components/      # Web3-specific components
│   │   ├── NFTBalance.tsx
│   │   ├── NativeBalance.jsx
│   │   └── User/
│   │       └── UserDashboard.jsx
│   ├── hooks/               # Custom React hooks
│   │   ├── useERC20.ts
│   │   ├── useERC721.ts
│   │   ├── useIPFS.js
│   │   └── useTokenPrice.js
│   ├── helpers/             # Utility functions
│   │   ├── formatters.js
│   │   ├── modules.js
│   │   └── networks.js
│   ├── uikit/              # UI components library
│   └── App.tsx             # Main application component
└── package.json
```

## 🎯 Key Components

### Protocol System
The marketplace is built on a modular protocol system that allows:
- Dynamic module addition (NFT collections, tokens, marketplaces)
- Role-based permissions
- Forwarder contract support for meta-transactions
- Royalty collection and distribution

### Smart Contract Interactions
The app includes hooks for interacting with:
- **Protocol Contract**: Core protocol management
- **Registry Contract**: Project and module registry
- **Marketplace Contract**: NFT trading logic
- **ERC721 Collections**: NFT collections with minting and transfers
- **ERC20 Tokens**: Custom token support

## 👨‍💼 Admin Features

### Access Admin Panel
1. Connect your wallet
2. If your address matches the protocol admin, you'll be redirected to `/admin`

### Deploy Contracts
- **NFT Collection**: Deploy ERC721 contracts with custom metadata
- **Marketplace**: Deploy marketplace contracts with customizable fees
- **ERC20 Token**: Deploy custom tokens for marketplace transactions

### Manage Modules
- Add modules to your protocol
- View installed modules
- Manage permissions and roles
- Withdraw accumulated fees and royalties

## 🌐 Supported Networks

The application supports multiple Ethereum networks:
- Ethereum Mainnet
- Polygon (Matic)
- Binance Smart Chain
- Avalanche
- Fantom
- Testnet networks (Rinkeby, Mumbai, etc.)

Configure networks in `src/helpers/networks.js`

## 🔧 Available Scripts

- `npm start` - Start development server
- `npm build` - Build production bundle
- `npm test` - Run tests
- `npm run connect` - Connect to Moralis local devchain
- `npm run deploypage` - Deploy to GitHub Pages
- `npm run clean` - Clean GitHub Pages cache

## 🔐 Security Considerations

- Never commit private keys or sensitive credentials
- Always verify smart contract addresses before transactions
- Use testnet for development and testing
- Implement proper access control for admin functions
- Audit smart contracts before mainnet deployment

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
