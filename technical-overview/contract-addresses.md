# Contract Addresses

All District smart contracts are deployed on Ethereum Mainnet and verified on Etherscan for full transparency.

## Core Vault Contracts

### District Vault (ERC-7540)

**Contract Address**
```
0x314d8aeb02bb5f6b86d2ac1fef4c5fc1771e6817
```

**Etherscan**
[View on Etherscan](https://etherscan.io/address/0x314d8aeb02bb5f6b86d2ac1fef4c5fc1771e6817)

**Description**
Main vault contract that handles deposits, redemptions, and vault share accounting.

**Key Functions**
- `requestDeposit()` - Request to deposit USDC
- `deposit()` - Complete deposit and mint DISTRICT tokens
- `requestRedeem()` - Request to redeem DISTRICT tokens
- `redeem()` - Complete redemption and receive USDC
- `balanceOf()` - Check DISTRICT token balance

---

### DISTRICT Token (Vault Shares)

**Token Address**
```
0x623587E3b66969D455c5A974Ca9596d66cb60034
```

**Etherscan**
[View on Etherscan](https://etherscan.io/token/0x623587E3b66969D455c5A974Ca9596d66cb60034)

**Token Details**
- **Name**: District Vault Token
- **Symbol**: DISTRICT
- **Decimals**: 18
- **Standard**: ERC-7540
- **Type**: Yield-bearing vault share

---

### Vault Manager

**Manager Address**
```
0x1133815B8c64DB3202A5F80C909771B3bfA33745
```

**Etherscan**
[View on Etherscan](https://etherscan.io/address/0x1133815B8c64DB3202A5F80C909771B3bfA33745)

**Description**
Administrative contract for vault management and parameter updates.

---

## Centrifuge Protocol Contracts

### Investment Manager

**Contract Address**
```
[To be added - Centrifuge investment manager contract]
```

**Description**
Handles the investment logic and asset deployment for the vault.

---

### Pool Manager

**Contract Address**
```
[To be added - Centrifuge pool manager contract]
```

**Description**
Manages the overall pool configuration and loan tokenization.

---

## Asset Contracts

### USDC (Deposit Asset)

**Token Address**
```
0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48
```

**Etherscan**
[View on Etherscan](https://etherscan.io/token/0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48)

**Token Details**
- **Name**: USD Coin
- **Symbol**: USDC
- **Decimals**: 6
- **Issuer**: Circle

---

## Custody & Security

### Safe Multi-Sig Wallet

**Safe Address**
```
[To be added - Safe multi-sig address]
```

**Description**
Multi-signature wallet used for vault fund custody and administrative operations.

**Configuration**
- Required signatures: [X of Y]
- Signers: [Number] authorized signers
- Time-lock: [Duration] for critical operations

---

## Oracle Contracts

### Price Feeds

**NAV Oracle**
```
[To be added - NAV calculation oracle]
```

**Description**
Provides real-time Net Asset Value calculations for the vault.

---

## Integration Contracts

### Router Contract

**Address**
```
[To be added - Router contract for integrations]
```

**Description**
Facilitates integrations with other DeFi protocols and aggregators.

---

## Deprecated Contracts

### Previous Versions

If applicable, previous contract versions will be listed here with migration information.

---

## Contract Verification

All contracts are:
- ✅ Verified on Etherscan
- ✅ Open source code available
- ✅ Audited by multiple firms
- ✅ Formally verified (critical functions)

## Security Audits

View all audit reports:
- [Centrifuge Protocol Audits](https://docs.centrifuge.io/developer/protocol/security/)
- [District-Specific Audits](../technical-overview/audits.md)

## Contract Interaction

### For Developers

**Web3 Integration**
```javascript
// Example: Connect to District Vault
const vaultAddress = "0x314d8aeb02bb5f6b86d2ac1fef4c5fc1771e6817";
const vaultABI = [...]; // ERC-7540 ABI

const vault = new ethers.Contract(vaultAddress, vaultABI, provider);

// Request deposit
const depositAmount = ethers.utils.parseUnits("10000", 6); // 10,000 USDC
await vault.requestDeposit(depositAmount, userAddress);
```

**ABI Files**
- [Vault ABI](https://github.com/districtcapital/contracts/blob/main/abi/Vault.json)
- [Token ABI](https://github.com/districtcapital/contracts/blob/main/abi/Token.json)

### For Users

**Recommended Interaction**
- Use the official District app: [app.district.capital](https://app.district.capital)
- Avoid direct contract interaction unless you're an experienced developer
- Always verify contract addresses before interacting

## Network Information

**Ethereum Mainnet**
- Chain ID: 1
- RPC: https://eth.llamarpc.com
- Explorer: https://etherscan.io

**Gas Considerations**
- Deposit: ~150,000 gas
- Redeem: ~120,000 gas
- Claim: ~80,000 gas

Actual gas usage may vary based on network conditions.

## Emergency Contacts

**Security Issues**
- Email: security@district.capital
- Bug Bounty: [bounty.district.capital](https://bounty.district.capital)

**Technical Support**
- Email: dev@district.capital
- Telegram: [Developer Chat](https://t.me/districtdevs)

---

**Important**: Always verify contract addresses through multiple official sources before interacting. Never trust addresses from unofficial sources.

Last updated: January 2025
