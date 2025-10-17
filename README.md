# 🗳️ Decentralized Election Platform

A secure, transparent, and tamper-proof blockchain-based voting system built on Ethereum. This platform enables commissioners to create and manage multiple election sessions while providing voters with a trustless, verifiable voting experience.

![Solidity](https://img.shields.io/badge/Solidity-0.8.19-363636?style=flat-square&logo=solidity)
![Ethereum](https://img.shields.io/badge/Ethereum-Sepolia-3C3C3D?style=flat-square&logo=ethereum)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

## ✨ Features

### For Commissioners
- **Multi-Election Management**: Create and manage unlimited election sessions
- **Flexible Configuration**: Set custom registration and voting periods
- **Candidate Management**: Add candidates with descriptions and qualifications
- **Real-time Monitoring**: Track votes, participation, and election status
- **Result Finalization**: Declare winners with cryptographic proof
- **Dynamic Timing**: Update election schedules before voting begins

### For Voters
- **Self-Registration**: Register during the designated period
- **Secure Voting**: One person, one vote with cryptographic verification
- **Transparency**: View all candidates and real-time vote counts
- **Status Tracking**: Check registration and voting status
- **Anonymous Participation**: Vote without revealing identity

### Technical Features
- **Factory Pattern**: Deploy independent election contracts on-demand
- **Role-Based Access**: Automatic detection of commissioner vs voter roles
- **Gas Optimized**: Efficient smart contract design
- **Event Logging**: Complete audit trail of all actions
- **Time-Locked Voting**: Period-based access control
- **Minimalist UI**: Clean, dark-themed interface with modern typography

## 🏗️ Architecture

```
┌─────────────────────────────────────────────┐
│ ElectionFactory Contract │
│ (Deploys and manages election instances) │
└─────────────────┬───────────────────────────┘
│
├── Creates
│
┌────────▼──────────┐
│ Election Instance │
│ - Candidates │
│ - Voters │
│ - Voting Logic │
└────────────────────┘
```

## 🚀 Quick Start

### Prerequisites

- [MetaMask](https://metamask.io/) browser extension
- Sepolia testnet ETH ([Get from faucet](https://sepoliafaucet.com))
- Modern web browser (Chrome, Firefox, Brave)

### Installation

1. **Clone the repository**

```
git clone https://github.com/yourusername/decentralized-election-platform.git
cd decentralized-election-platform
```

2. **Deploy Smart Contracts**
   - Open [Remix IDE](https://remix.ethereum.org)
   - Copy `contracts/ElectionFactory.sol`
   - Compile with Solidity 0.8.19
   - Deploy to Sepolia testnet via MetaMask
   - Copy the deployed factory address

3. **Configure Frontend**
   - Open `app.js`
   - Update `FACTORY_ADDRESS` with your deployed address:

```
const FACTORY_ADDRESS = "0xYourFactoryAddress";
```


4. **Run the Application**
- Open `index.html` in your browser
- Connect MetaMask to Sepolia testnet
- Start creating elections!

## 📁 Project Structure

```
decentralized-election-platform/
├── contracts/
│ └── ElectionFactory.sol # Smart contract code
├── index.html # Main HTML structure
├── styles.css # Dark theme styling
├── app.js # Web3 integration logic
└── README.md # Documentation
```


## 🔧 Technology Stack

**Smart Contracts:**
- Solidity ^0.8.19
- OpenZeppelin patterns (Factory, Access Control)

**Frontend:**
- Vanilla JavaScript (ES6+)
- Ethers.js v6.7.0
- HTML5 & CSS3
- Google Fonts (Inter, JetBrains Mono)

**Blockchain:**
- Ethereum (Sepolia Testnet)
- MetaMask Wallet Integration
- Event-driven architecture

## 📖 Usage Guide

### As a Commissioner

1. **Connect Wallet**: Click "Connect Wallet" and approve MetaMask
2. **Create Election**: Click "+ New Election"
3. **Initialize Election**:
   - Enter title and description
   - Set registration period (start/end)
   - Set voting period (start/end)
   - Click "Initialize"
4. **Add Candidates**:
   - Go to "Candidates" tab
   - Enter candidate name and description
   - Click "Add Candidate"
5. **Monitor Progress**: Track registrations and votes in real-time
6. **Finalize Results**: Click "Finalize Election" after voting ends

### As a Voter

1. **Connect Wallet**: Connect your MetaMask wallet
2. **Browse Elections**: View all available elections
3. **Select Election**: Click on an election card
4. **Register**: Click "Register to Vote" during registration period
5. **Cast Vote**:
   - Review all candidates
   - Click "Vote" on your chosen candidate
   - Confirm transaction in MetaMask
6. **Verify**: Check your status shows "Already voted"

## 🔐 Security Features

- **Immutable Records**: All votes stored permanently on blockchain
- **Time-Locked Access**: Period-based registration and voting
- **Single Vote Enforcement**: Smart contract prevents double voting
- **Commissioner-Only Actions**: Role-based access control
- **Transparent Audit Trail**: All events logged on-chain
- **No Vote Manipulation**: Finalized results cannot be altered

## 🎨 UI/UX Highlights

- **Dark Mode Only**: Eye-friendly minimalist design
- **Responsive Layout**: Works on desktop and mobile
- **Real-time Updates**: Automatic status synchronization
- **Clear Status Badges**: Visual indicators for election phases
- **Smooth Transitions**: Polished animations and interactions
- **Monospace Addresses**: Easy-to-read contract addresses

## 🧪 Testing

**Test on Sepolia Testnet:**
1. Get test ETH from [Sepolia Faucet](https://sepoliafaucet.com)
2. Create a test election with short time periods
3. Use multiple MetaMask accounts to simulate voters
4. Test all flows: register → vote → finalize

**Common Test Scenarios:**
- Register multiple voters
- Attempt double voting (should fail)
- Try voting without registration (should fail)
- Update timings before voting starts
- Finalize election and verify winner

## 🐛 Troubleshooting

**Issue**: "Please install MetaMask"
- **Solution**: Install MetaMask browser extension

**Issue**: "Wrong network" error
- **Solution**: Switch MetaMask to Sepolia testnet

**Issue**: "Insufficient ETH" error
- **Solution**: Get test ETH from Sepolia faucet

**Issue**: Transaction fails during election creation
- **Solution**: Increase gas limit or check contract address

**Issue**: Can't see my elections
- **Solution**: Refresh page and reconnect wallet

## 🗺️ Roadmap

- [ ] NFT voting badges for participation proof
- [ ] Quadratic voting mechanism
- [ ] Delegated voting (liquid democracy)
- [ ] Multi-language support
- [ ] Mobile app (React Native)
- [ ] IPFS integration for candidate profiles
- [ ] DAO governance integration
- [ ] Cross-chain deployment (Polygon, Arbitrum)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- Ethereum Foundation for blockchain infrastructure
- OpenZeppelin for smart contract patterns
- MetaMask for wallet connectivity
- Ethers.js for Web3 integration

## 📊 Project Status

🟢 **Active Development** - Currently in beta testing phase

**⭐ Star this repo if you find it useful!**

Made with ❤️ and ☕ by Atharva Landge.
