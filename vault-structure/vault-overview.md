# District Vault Overview

The District vault is an ERC-7540 compliant smart contract pool built on the Centrifuge Protocol, designed to facilitate transparent, secure lending to U.S. small and medium-sized businesses.

## Vault Specifications

### Basic Information

- **Asset Type**: Private Credit (Senior Secured Loans)
- **Target APY**: 11-13%
- **Minimum Investment**: $10,000 USDC
- **Network**: Ethereum (ERC-20)
- **Token Standard**: ERC-7540
- **Vault Token**: DISTRICT
- **Deposit Currency**: USDC
- **Investor Type**: Non-U.S. Investors
- **Pool Structure**: Revolving

### Infrastructure

- **Protocol**: Centrifuge
- **Custody**: Safe (Multi-signature wallet)
- **Vault Manager**: Zeonix Services - FZCO
- **Financial Operator**: Coinbase
- **Lending Syndicate**: Washington, D.C. Consortium

## How the Vault Works

### Deposit Flow

1. **Connect Wallet**: Connect your Ethereum wallet to the District app
2. **Deposit USDC**: Transfer USDC from your wallet to the vault
3. **Receive DISTRICT Tokens**: Instantly receive vault shares (DISTRICT tokens)
4. **Conversion**: USDC is converted to USD via Coinbase
5. **Deployment**: USD is lent to vetted SMBs through FDIC-insured banks

### Yield Accrual

1. **Loan Interest**: Borrowers pay monthly interest (typically 11-15%)
2. **Principal Repayment**: Loans repaid over 12-36 month terms
3. **Conversion**: USD converted back to USDC via Coinbase
4. **Distribution**: Yield flows to vault, increasing DISTRICT token value
5. **Compounding**: Yield automatically reinvested unless redeemed

### Redemption Flow

1. **Request Redemption**: Submit redemption request through the app
2. **Queue Processing**: Request enters redemption queue
3. **Liquidity Check**: Fulfilled from reserve pool or loan repayments
4. **Token Burn**: DISTRICT tokens burned upon redemption
5. **USDC Return**: Receive USDC back to your wallet

## Vault Architecture

### Capital Allocation

The vault maintains a balanced allocation strategy:

**Active Loans (80-90%)**
- Senior secured business loans
- $500K-$2M per loan
- 12-36 month terms
- Diversified across sectors

**Reserve Pool (10-20%)**
- U.S. Treasury Bills
- High-grade stablecoins
- Provides redemption liquidity
- Earns base yield (4-5%)

### Risk Layers

**Layer 1: Loan Selection**
- Rigorous underwriting by 30-year veteran team
- Only cash-flow positive businesses
- Established operations (2+ years)
- Strong management teams

**Layer 2: Collateralization**
- Real estate and business assets
- LTV ratios of 50-70%
- Independent appraisals
- Regular revaluations

**Layer 3: Legal Protection**
- Full recourse to borrower
- Personal guarantees from owners
- UCC filings on business assets
- First lien position on collateral

**Layer 4: Diversification**
- Maximum 15% to single borrower
- Maximum 30% to single industry
- Minimum 10 active loans
- Geographic concentration limits

**Layer 5: Reserve Pool**
- Liquid assets for redemptions
- Reduces forced loan sales
- Provides stability during stress

## Vault Metrics

### Performance Indicators

**Total Value Locked (TVL)**
- Current vault size in USD
- Updated in real-time on-chain
- Includes deployed loans + reserves

**Active Loans**
- Number of current loans
- Total principal outstanding
- Average loan size
- Sector breakdown

**Yield Metrics**
- Current APY
- Historical APY
- Yield distribution history
- Fee breakdown

**Risk Metrics**
- Average LTV ratio
- Weighted average maturity
- Concentration ratios
- Default rate

### Historical Performance

Since inception:
- Loans Originated: [Updated monthly]
- Total Interest Paid: [Updated monthly]
- Default Rate: <1.5% (historical consortium rate)
- Recovery Rate: 85%+ on defaults

## Vault Token (DISTRICT)

### Token Characteristics

**ERC-7540 Standard**
- Asynchronous deposit/redemption
- Request-based processing
- On-chain transparency
- Standardized interface

**Yield-Bearing**
- Value increases with vault performance
- Automatic yield compounding
- No manual claiming required
- Real-time NAV calculation

**Redeemable**
- Request redemption anytime
- Subject to liquidity availability
- Processed from reserve pool
- No lock-up periods

### Token Value Calculation

```
DISTRICT Token Value = (Total Vault Assets) / (Total DISTRICT Supply)

Total Vault Assets = 
  + Outstanding Loan Principal
  + Accrued Interest
  + Reserve Pool Assets
  - Pending Redemptions
  - Accrued Fees
```

### Token Supply Dynamics

**Minting (Increases Supply)**
- New deposits create new DISTRICT tokens
- Proportional to deposit amount
- Instant upon deposit confirmation

**Burning (Decreases Supply)**
- Redemptions burn DISTRICT tokens
- Proportional to redemption amount
- Occurs upon redemption fulfillment

## Fee Structure

### Performance Fee: 15%

- Applied to net interest income
- Covers operational expenses
- Funds ongoing development
- Supports audits and security

### Centrifuge Protocol Fee: 0.50%

- Annual fee on total AUM
- Paid to Centrifuge Protocol
- Covers infrastructure costs
- Supports protocol development

### Net Yield to Depositors

```
Gross Yield: 13% (average loan rate)
- Performance Fee: 1.95% (15% of 13%)
- Centrifuge Fee: 0.50%
= Net Yield: 10.55% to depositors

Target Range: 11-13% APY
```

## Liquidity Management

### Reserve Pool Strategy

**Target Allocation**: 10-20% of vault
**Assets Held**: 
- U.S. Treasury Bills (primary)
- USDC (secondary)
- High-grade money market instruments

**Purpose**:
- Fulfill redemption requests
- Provide stability
- Earn base yield
- Reduce forced sales

### Redemption Processing

**Priority System**:
1. Reserve pool assets (immediate)
2. Scheduled loan repayments (days-weeks)
3. Early loan payoffs (negotiated)
4. Secondary market sales (if needed)

**Typical Timeline**:
- Reserve pool: 1-3 days
- Loan repayments: 1-4 weeks
- Large redemptions: 4-8 weeks

## Vault Security

### Smart Contract Security

- Built on audited Centrifuge Protocol
- Multiple independent audits
- Formal verification of critical functions
- Bug bounty program
- Emergency pause mechanism

### Custody Security

- Safe multi-signature wallet
- Multiple signers required
- Hardware wallet integration
- Time-locked transactions
- Segregated accounts

### Operational Security

- Regular security audits
- Penetration testing
- Incident response plan
- Insurance coverage (where available)
- 24/7 monitoring

## Vault Governance

### Parameter Management

**Adjustable Parameters**:
- Reserve pool target percentage
- Maximum loan size
- Concentration limits
- Fee structure (within bounds)

**Change Process**:
- Proposed by Vault Manager
- 30-day notice period
- Community feedback
- Transparent implementation

### Emergency Procedures

**Pause Mechanism**:
- Can halt deposits/redemptions
- Requires multi-sig approval
- Used only in emergencies
- Transparent communication

**Recovery Procedures**:
- Defined escalation process
- External expert consultation
- Token holder communication
- Gradual resumption

## Comparison with Other Vaults

### vs. Traditional Money Market Funds

| Feature | Money Market | District Vault |
|---------|-------------|----------------|
| Yield | 4-5% | 11-13% |
| Liquidity | Same day | 1-4 weeks |
| Minimum | $1K | $10K |
| Risk | Very low | Low-medium |
| Transparency | Quarterly | Real-time |

### vs. DeFi Lending Protocols

| Feature | DeFi Lending | District Vault |
|---------|--------------|----------------|
| Collateral | Crypto | Real estate |
| Yield Source | Crypto borrowing | Business cash flow |
| Risk | High volatility | Stable assets |
| Regulation | Minimal | Full compliance |
| Default Protection | Liquidation | Legal recourse |

### vs. Other RWA Protocols

| Feature | Other RWA | District Vault |
|---------|-----------|----------------|
| Track Record | New | 30 years |
| Asset Type | Various | Senior secured |
| Transparency | Varies | Full on-chain |
| Minimum | Varies | $10K |
| Management | Varies | Proven team |

## Getting Started

Ready to deposit? Follow these steps:

1. [Read the Risks](risks-mitigants.md)
2. [Understand Fees](fee-structure.md)
3. [Review the Deposit Process](deposit-redemption.md)
4. [Connect Your Wallet](../app-guide/getting-started.md)

---

Last updated: January 2025
