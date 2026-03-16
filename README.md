### 3. Smart Contracts: `green-anchor-contracts` (Soroban/Rust)

```markdown
# GreenAnchor Soroban Contracts 🦀

The trustless logic layer of the GreenAnchor Protocol, built on Stellar's Soroban smart contract platform.

## 🛠️ Tech Stack
- **Language:** Rust
- **Platform:** Soroban (Stellar Smart Contracts)
- **Testing:** Soroban SDK Test Framework

## 📜 Included Contracts
### 1. `OffsetRetirement.wasm`
Handles the logic for "burning" or permanently locking carbon credit tokens. It ensures that once a credit is claimed for ESG compliance, it can never be traded again.

### 2. `CreditFractionalizer.wasm`
Allows for the micro-segmentation of carbon credits, enabling SMEs to purchase offsets as small as 0.0001 tons.

### 3. `ImpactOracle.wasm`
A permissioned contract that stores verified environmental data points from our NestJS Oracle service.

## 🧪 Testing & Deployment
**Build:**
`soroban contract build`

**Test:**
`cargo test`

**Deploy to Testnet:**
`soroban contract deploy --wasm target/wasm32-unknown-unknown/release/green_anchor.wasm --source admin --network testnet`

## 🛡️ Security
- **Auth:** Implements Soroban's native authentication host functions.
- **Storage:** Efficient use of `Temporary` vs `Persistent` storage to minimize ledger fees.
