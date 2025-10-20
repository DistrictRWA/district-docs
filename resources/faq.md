# Frequently Asked Questions

## General Questions

### What is District?

District is a real-world asset (RWA) protocol built on Centrifuge that enables global investors to gain tokenized exposure to the U.S. private credit lending market—specifically Senior Secured Business Loans. By connecting stablecoin deposits to off-chain lending, District provides access to institutional-grade private credit through blockchain technology.

### How do I earn yield?

When you deposit USDC into the District vault, you receive DISTRICT tokens representing your vault shares. Your funds are converted to USD via Coinbase and lent to vetted Washington, D.C. area small and medium-sized businesses (SMBs). As borrowers repay their loans with interest, capital flows back into the vault, and you earn yield paid in USDC. The vault targets 11-13% APY for depositors.

### What makes District different from other DeFi protocols?

District combines traditional finance expertise with blockchain infrastructure:

- **Real-world assets**: Loans backed by real estate and business cash flows, not crypto
- **Proven track record**: 30 years of lending experience with <1.5% default rate
- **Institutional quality**: Same loan standards used by traditional private credit funds
- **Full transparency**: Every loan visible on-chain with real-time performance data
- **Professional management**: Experienced team handling all operations
- **Regulatory compliance**: Full compliance framework with proper licensing

### Who can invest in District?

District is currently available to **non-U.S. investors** who meet the minimum investment requirement of $10,000 USDC. You must:

- Be a non-U.S. person (individual or entity)
- Have an Ethereum wallet
- Meet the $10K minimum investment

U.S. persons are currently not eligible due to regulatory considerations.

## Deposits & Withdrawals

### What cryptocurrencies can I deposit?

The District vault accepts **USDC on Ethereum (ERC-20)** for deposits. Other stablecoins and networks may be supported in the future.

### What is the minimum investment?

The minimum investment is **$10,000 USDC**. This ensures the vault can efficiently deploy capital into appropriately sized loans while maintaining diversification.

### How do I deposit?

1. Connect your Ethereum wallet to app.district.capital
2. Ensure you have at least $10,000 USDC in your wallet
3. Click "Deposit" and enter the amount
4. Approve the transaction in your wallet
5. Receive DISTRICT tokens immediately

Your USDC is converted to USD via Coinbase and deployed into loans.

### How long does it take to deposit?

Deposits are processed immediately upon blockchain confirmation (typically 1-5 minutes). You receive DISTRICT tokens instantly, though it may take 1-2 business days for the USDC to be converted to USD and deployed into loans.

### Can I withdraw my funds anytime?

Yes, you can request a redemption at any time. However, fulfillment depends on available liquidity:

- **Reserve pool**: 1-3 days (if sufficient reserves)
- **Loan repayments**: 1-4 weeks (typical)
- **Large redemptions**: 4-8 weeks (may require multiple loan repayments)

District maintains a reserve pool (10-20% of vault) in liquid assets to facilitate redemptions.

### Is there a lock-up period?

No, there is no mandatory lock-up period. You can request redemption at any time. However, as an illiquid asset class, redemptions are subject to available liquidity from the reserve pool or loan repayments.

### How do I withdraw?

1. Go to app.district.capital
2. Click "Redeem"
3. Enter the amount of DISTRICT tokens to redeem
4. Submit your redemption request
5. Wait for processing (1-4 weeks typically)
6. Receive USDC back to your wallet

## Yield & Returns

### What is the target APY?

District targets **11-13% APY** for depositors, paid in USDC. This is net of all fees.

### How is yield calculated?

Yield comes from interest paid by borrowers on their loans:

```
Borrower Interest Rate: 11-15% (varies by loan)
- Performance Fee: 15% of interest income
- Centrifuge Fee: 0.50% of AUM annually
= Net Yield to Depositors: 11-13% APY
```

### When do I receive yield?

Yield accrues continuously as borrowers make interest payments. The value of your DISTRICT tokens increases automatically—you don't need to claim anything. When you redeem, you receive your principal plus all accrued yield in USDC.

### Is the yield guaranteed?

No, the 11-13% APY is a target, not a guarantee. Actual returns depend on:

- Loan performance (interest payments received)
- Default rates (historically <1.5%)
- Reserve pool allocation (earns lower base yield)
- Fee structure

Historical performance of the lending syndicate suggests the target is achievable, but past performance doesn't guarantee future results.

### How does yield compare to other options?

| Investment | Typical Yield | Risk Level |
|------------|--------------|------------|
| U.S. Savings Account | 0.5-1% | Very Low |
| U.S. Treasury Bills | 4-5% | Very Low |
| Corporate Bonds | 5-7% | Low-Medium |
| **District Vault** | **11-13%** | **Low-Medium** |
| DeFi Lending | 3-15% | Medium-High |
| Crypto Staking | 5-20% | High |

## Fees & Costs

### What are the fees?

**Performance Fee: 15%**
- Applied to net interest income only
- Covers operational expenses, audits, and development
- Only charged when the vault generates yield

**Centrifuge Protocol Fee: 0.50%**
- Annual fee on total assets under management
- Paid to Centrifuge for infrastructure
- Deducted from vault assets

**No Other Fees:**
- No deposit fees
- No redemption fees
- No management fees beyond the above

### How are fees deducted?

Fees are automatically deducted from the vault's assets before yield is distributed to DISTRICT token holders. You don't need to pay anything separately—the net APY you see already accounts for all fees.

### Can fees change?

The Vault Manager can adjust fees within predefined limits, subject to a 30-day notice period and community feedback. Any material fee changes will be clearly communicated to all depositors.

## Risks & Security

### What are the main risks?

**Credit Risk**: Borrowers may default on loans. Mitigated by:
- Rigorous underwriting (30-year track record)
- Overcollateralization (LTV ≤ 70%)
- Full recourse to borrowers and guarantors
- Diversification across multiple loans

**Liquidity Risk**: Redemptions depend on loan repayments. Mitigated by:
- Reserve pool (10-20% of vault)
- Staggered loan maturities
- Flexible redemption queue

**Smart Contract Risk**: Bugs or exploits in code. Mitigated by:
- Built on audited Centrifuge Protocol
- Multiple independent security audits
- Bug bounty program
- Emergency pause mechanism

**Operational Risk**: Management or process failures. Mitigated by:
- Experienced 30-year lending team
- Multi-signature custody
- Regular audits and oversight
- Transparent reporting

See [Risks & Mitigants](../vault-structure/risks-mitigants.md) for detailed information.

### Has District been audited?

Yes. The District vault is built on the Centrifuge Protocol, which has been audited by:
- Spearbit
- SRLabs
- Code4rena
- Least Authority
- Consensys Diligence
- Trail of Bits

Additionally, District conducts regular operational and financial audits. All audit reports are publicly available.

### How are my funds protected?

**Smart Contract Level:**
- Audited code
- Multi-signature custody (Safe)
- Emergency pause mechanism
- Time-locked transactions

**Loan Level:**
- Overcollateralized loans (LTV ≤ 70%)
- Real estate and business asset backing
- Full recourse to borrowers
- Legal documentation and UCC filings

**Operational Level:**
- Experienced management team
- Regular audits
- Transparent reporting
- Insurance coverage (where available)

### What happens if a borrower defaults?

The lending syndicate has extensive experience managing defaults:

1. **Early intervention**: Proactive communication with struggling borrowers
2. **Restructuring**: Modify terms to help borrower recover
3. **Collateral liquidation**: Sell collateral if necessary
4. **Legal action**: Pursue guarantors and other recourse
5. **Recovery**: Historical 85%+ recovery rate on defaults

The vault's diversification means a single default has minimal impact on overall returns.

## Loans & Lending

### What types of loans does District make?

District provides **Senior Secured Business Loans** to Washington, D.C. area SMBs:

**Loan Characteristics:**
- Size: $500K-$2M
- Term: 12-36 months
- Interest: 11-15%
- LTV: 50-70%
- Collateral: Real estate + business assets
- Recourse: Full recourse to borrower and guarantors

**Borrower Types:**
- Healthcare practices
- Technology companies
- Real estate investors
- Professional services firms

### How are borrowers vetted?

The Washington, D.C. Consortium conducts rigorous due diligence:

1. **Initial screening**: Business history, financials, management
2. **Credit analysis**: Cash flow, debt service coverage, credit history
3. **Collateral appraisal**: Independent valuation of assets
4. **Legal review**: Corporate structure, liens, litigation
5. **Personal guarantees**: Owner background checks and net worth verification
6. **Final approval**: Committee review and approval

Only 10-15% of loan applications are approved.

### Can I see individual loans?

Yes! All loans are tokenized on-chain via Centrifuge. You can view:
- Loan amount and terms
- Collateral type and value
- Interest rate and maturity
- Payment history
- Current status

Borrower identities are anonymized for privacy, but all financial details are transparent.

### What happens to my money between loans?

When not deployed in loans, vault capital is held in the reserve pool:
- U.S. Treasury Bills (primary)
- USDC (secondary)

This ensures your capital is always productive while maintaining liquidity for redemptions.

## Technical Questions

### What blockchain is District on?

District operates on **Ethereum mainnet**. The vault accepts USDC (ERC-20) deposits and issues DISTRICT tokens (ERC-7540 standard).

### What is ERC-7540?

ERC-7540 is a token standard designed for real-world asset vaults. It provides:
- Asynchronous deposit/redemption (request-based)
- Standardized interface for RWA vaults
- On-chain transparency
- Compatibility with DeFi protocols

### What wallet do I need?

Any Ethereum-compatible wallet works:
- MetaMask (most popular)
- Coinbase Wallet
- WalletConnect-compatible wallets
- Hardware wallets (Ledger, Trezor)

### Can I use District with other DeFi protocols?

DISTRICT tokens are ERC-7540 compliant and can potentially be used in compatible DeFi protocols.

### Where are the smart contracts?

All contract addresses are available in the [Contract Addresses](../technical-overview/contract-addresses.md) section. The contracts are verified on Etherscan for full transparency.

## Support & Contact

### How do I get help?

**Support Channels:**
- Email: support@district.capital
- Documentation: docs.district.capital
- Twitter: @district_rwa

**Response Times:**
- Email: 24-48 hours
- Critical issues: Immediate escalation

### Where can I learn more?

- **Website**: [district.capital](https://district.capital)
- **Documentation**: This GitBook
- **Twitter**: [@district_rwa](https://twitter.com/district_rwa)

### How do I report a bug or security issue?

**Security Issues:**
- Email: security@district.capital
- Bug Bounty: [bounty.district.capital](https://bounty.district.capital)
- Responsible disclosure appreciated

**General Bugs:**
- Email: support@district.capital
- GitHub: [github.com/districtcapital](https://github.com/districtcapital)

### Can I invest on behalf of a company or fund?

Yes, institutional investors are welcome. Please contact:
- Email: support@district.capital
- Include: Entity type, jurisdiction, intended investment size

We can discuss:
- Custom terms for large deposits
- Reporting requirements
- Legal documentation
- Integration options

---

**Still have questions?** Contact us at support@district.capital

Last updated: January 2025
