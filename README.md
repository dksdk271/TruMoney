# Treasure NFT - Starter Project
This is a starter scaffold for a "Treasure NFT" app:
- Frontend: React Native (Expo)
- Backend: Node.js + Express (mock endpoints)
- Smart Contract: Solidity ERC-721 (sample)

## What's included
- frontend/ : Expo React Native app (basic screens)
- backend/  : Node.js Express server (hunts API, mock mint)
- contracts/: Solidity ERC-721 contract (sample)

## Quick start (frontend)
1. Install Expo CLI: `npm install -g expo-cli`
2. Open `frontend/` and run:
   ```
   npm install
   expo start
   ```

## Quick start (backend)
1. Open `backend/` and run:
   ```
   npm install
   node server.js
   ```

## Smart contract
- `contracts/TreasureNFT.sol` is a simple ERC-721 contract.
- Use Hardhat or Truffle to compile & deploy to a testnet (Polygon Mumbai recommended).

## Notes
This is a minimal starter to help you get going. Customize hunt logic, wallet integration (WalletConnect / MetaMask), IPFS storage, and real minting flows as needed.

## Added features in this updated starter
- Frontend: WalletConnect scaffold and wallet connection UI (uses @walletconnect/react-native-dapp)
- Backend: /api/claim endpoint now uploads metadata to NFT.Storage (if NFT_STORAGE_KEY provided) and attempts on-chain mint via ethers.
- Contracts: Hardhat deploy scaffold and instructions.
- .env.example added in backend for RPC/PRIVATE_KEY/CONTRACT_ADDRESS/NFT_STORAGE_KEY.

## How to test full flow locally (recommended)
1. Backend:
   - cd backend
   - npm install
   - copy .env.example to .env and fill or leave blank to use mock flow
   - node server.js
2. Frontend:
   - cd frontend
   - npm install
   - expo start
   - Use a WalletConnect-capable wallet to connect (or test connector in emulator)
3. Deploy contract (optional for real minting) using Hardhat scaffold in contracts/hardhat.
