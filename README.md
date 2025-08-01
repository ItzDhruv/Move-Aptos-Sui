# Move Mastery Suite: Smart Contract Collection (Aptos/Sui)

Welcome to the **Move Mastery Suite**, a curated collection of five high-impact, well-scoped smart contract products written in **Move language**. Each module is designed to teach best practices and advanced design patterns on **Aptos and Sui** blockchains.

---

## 📦 Repo Structure

Each sub-folder contains one project with the following files:

* `sources/` – Core Move modules
* `tests/` – End-to-end and property-based tests
* `Move.toml` – Project config
* `README.md` – Project-specific instructions

---

## 📘 Project Index

### 1. 🌀 FlowStream – Real-Time Token Streaming Protocol

* **Use Cases:** Payroll, grants, subscriptions
* **Core Features:** `create_stream`, `withdraw_streamed`, `cancel_stream`, `top_up`
* **Highlights:** Time-based withdrawals, rate math, timestamp integration
* **Aptos:** `0x1::timestamp`
* **Sui:** `0x3::clock` (ms-precision)
* 📁 Folder: `flowstream`

### 2. 🏪 Rentable – NFT Rental Marketplace

* **Use Cases:** In-game item rentals, metaverse land leases
* **Core Features:** `list_for_rent`, `rent_nft`, `return_nft_early`, `claim_expired_nft`
* **Highlights:** Time-limited rental rights, optional collateral, auto-return
* **Aptos:** Tables, capability tokens
* **Sui:** Object wrapping/unwrapping
* 📁 Folder: `rentable`

### 3. 🏛️ MoveDAO – On-Chain Governance Framework

* **Use Cases:** DAO voting, treasury control
* **Core Features:** `create_proposal`, `vote`, `queue`, `execute`
* **Highlights:** Modular strategy plugins, timelock queueing, multi-asset vaults
* **Aptos:** Multi-agent transaction batching
* **Sui:** Delegation with dynamic fields
* 📁 Folder: `movedao`

### 4. 🌐 NodeStaker – DePIN Staking & Reward Protocol

* **Use Cases:** IoT sensor reward system
* **Core Features:** `stake`, `submit_data_proof`, `distribute_rewards`, `slash`
* **Highlights:** Epoch-based accounting, capability staking, slashing
* **Aptos:** On-chain ed25519 verification
* **Sui:** Off-chain proof scoring via indexers
* 📁 Folder: `nodestaker`

### 5. 🔁 MoveBridge – Cross-Chain Token & Message Bridge

* **Use Cases:** Liquidity transfer, inter-chain comms
* **Core Features:** `lock`, `mint_wrapped`, `burn`, `release`, `relay_message`
* **Highlights:** Merkle proof verification, relayer network, object-mint bridging
* **Aptos ↔ Sui** bridging via light clients
* 📁 Folder: `movebridge`

### 6. 📊 MoveETF – Tokenized Index Fund (Bonus)

* **Use Cases:** DeFi index tracking, DAO treasury parking
* **Core Features:** `mint_shares`, `redeem_shares`, `rebalance`, `collect_fees`
* **Highlights:** Multi-token vault, rebalance incentives, streaming fees
* 📁 Folder: `moveetf`

---

## 🧪 Test Coverage & Simulation

* ✅ Unit and property tests for every core logic path
* ⏱️ Time-warp and expiry simulations for rental/stream logic
* 🔁 Rebalance and reward fuzzers

---

## 🚀 Get Started

```bash
# Clone repo
$ git clone https://github.com/itzdhruv/move-aptos-sui.git
$ cd move-master-suite

# Run tests for FlowStream
$ cd flowstream
$ aptos move test
```

---

## 👩‍🏫 Educational Value

Each project emphasizes a distinct design skill:

| Skill                 | Project              |
| --------------------- | -------------------- |
| Resource accounting   | FlowStream, MoveETF  |
| Capability-based auth | Rentable, NodeStaker |
| Governance flows      | MoveDAO              |
| Cross-chain mechanics | MoveBridge           |

---

## 🛡️ Security Practices

* Access control with capability/resource ownership
* Timestamp safe math with `math64`
* Invariant enforcement: balances, caps, rights
* No reentrancy (inherent in Move)

---

## 📜 License

MIT

---

Built for Move learners, by Move builders 💪

