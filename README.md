# 🧪 FoundryProject251

A modular smart contract monorepo powered by [Foundry](https://book.getfoundry.sh/), built for testing, experimentation, and learning.  
This repo contains multiple self-contained Solidity projects, including zkSync experiments and Chainlink-integrated dApps.

---

## �� Monorepo Structure

```
foundry-projects/
├── foundry-fund-me-f25/        → Chainlink + Crowdfunding
├── foundry-simple-storage-f23/ → Beginner storage contract
├── foundry-zksync/             → zkSync test suite and experiments
├── .gitignore
└── .env                        (not committed)
```

Each subproject is independently runnable with its own scripts, tests, and deployments.

---

## 🚀 Quickstart

### 1. Install Foundry

```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### 2. Clone & Enter

```bash
git clone git@github.com:ShahilRoy/FoundryProject251.git
cd FoundryProject251
```

### 3. Install Dependencies

```bash
forge install
```

### 4. Run Tests

```bash
forge test -vvv
```

---

## ⚙️ Project Details

### ✅ `foundry-fund-me-f25/`
A decentralized funding app using Chainlink price feeds.

- ✔️ Chainlink AggregatorV3
- ✔️ Minimum USD contribution logic
- ✔️ Funders data structure tests
- ✔️ Sepolia + Local deployment

### 🧱 `foundry-simple-storage-f23/`
A learning project focused on core Foundry concepts.

- Simple `uint256` storage
- Scripted deployment
- Unit tests with Foundry standard library

### 🔒 `foundry-zksync/`
Experimental contracts + tests for working with zkSync L2.

- Solidity tests under zkSync constraints
- Testdata-driven testing (`testdata/zk`)
- Compatible with `zksync-up`

---

## 🔐 `.env` Setup

Create a `.env` file in root with the following:

```dotenv
SEPOLIA_RPC_URL=https://...
PRIVATE_KEY=0xabc...
ETHERSCAN_API_KEY=key
```

---

## 📜 Scripts

Each project contains deployment scripts under `script/`:

```bash
forge script script/DeployFundMe.s.sol \
  --rpc-url $SEPOLIA_RPC_URL \
  --private-key $PRIVATE_KEY \
  --broadcast
```

---

## 📄 License

This repo is licensed under [MIT](LICENSE).

---

## 👨‍💻 Author

Maintained by [Shahil Roy](https://github.com/ShahilRoy) — feel free to star or fork the project!
