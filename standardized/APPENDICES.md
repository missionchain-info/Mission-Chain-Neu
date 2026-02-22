# Mission Chain - Appendices (Standardized)

Version: v1.0 (Standardized Draft)
Date: 2026-02-21

## Appendix A - Seed Round / Private Sale

### A.1 Purpose
Private strategic round to fund protocol foundation and align long-term participants.

### A.2 Allocation and Pricing
- Allocation: 3.25% of total MIC supply
- Token amount: 227,500,000 MIC
- Price: USD 0.0025 per MIC
- Mathematical raise cap: USD 568,750

### A.3 Participation Packages
- Pack 1: USD 1,000 -> 400,000 MIC + 20 MFP-NFT allocations
- Pack 2: USD 5,000 -> 2,000,000 MIC + 120 MFP-NFT allocations
- Pack 3: USD 10,000 -> 4,000,000 MIC + 300 MFP-NFT allocations
- Pack 4: USD 20,000 -> 8,000,000 MIC + 750 MFP-NFT allocations

### A.4 MFP-NFT Rule
- MFP-NFTs are governance/stewardship role assets.
- They are not equity, profit rights, or guaranteed returns.
- Seed allocation reserve cap: 14,000 MFP-NFT units.

### A.5 Vesting (Seed)
- Fixed TGE: none
- Cliff: 6 months
- Initial unlock: 10%
- Monthly unlock: 2.5%
- Vesting start: individual purchase date

### A.6 Incentive Restrictions
- Referral: not applied
- Group bonus: not applied
- Network commission: not applied
- Seed participation is excluded from runtime protocol incentive programs.

### A.7 Compliance
No guaranteed returns, no equity rights, and no intended security offering.

---

## Appendix B - Pre-Sale (Community and Platform Expansion)

### B.1 Purpose
Controlled ecosystem activation and early user acquisition.

### B.2 Allocation and Pricing
- Allocation: 4.50% of total MIC supply
- Token amount: 315,000,000 MIC
- Price: USD 0.005 per MIC
- Hard cap from token math: USD 1,575,000
- Operational planning target may be lower (e.g., USD 1,500,000) by treasury decision.

### B.3 Vesting (Pre-Sale)
- Fixed TGE: none
- Cliff: 6 months
- Initial unlock: 10%
- Monthly unlock: 2.5%
- Vesting start: individual purchase date

### B.4 Allocation Flexibility
- Seed + Pre-Sale combined cap: <= 8.25% of total supply
- Total pre-issued cap: fixed at 15%
- All adjustments require transparent disclosure.

### B.5 Referral Incentives (Pre-Sale Only)
- Level 1 direct: 10% (USDT)
- Level 2 indirect: 5% (USDT)
- Total referral payout cap: <= 15% of Pre-Sale gross proceeds

### B.6 Group Performance Bonus (Pre-Sale Only)
- Maximum rate cap: 8%
- Differential override applies only to direct groups.
- Fixed USD 1,000 tier at USD 25,000 group volume is standalone and non-differential.

### B.7 Credential Consistency Rule
Performance programs do not mint governance/reputation credentials directly. Any non-cash promotional benefit is treated as onboarding or education credit and has no governance weight.

---

## Appendix C - MICE Sale Structure

### C.1 Instrument Definition
MICE (Mission Algorithm Mining License) is a time-bound access license for mining distribution participation. It is not a token, not equity, and not a yield guarantee.

### C.2 Supply and Lifecycle
- Cap: 100,000 MICE
- Activation period: 360 days
- Expiry: automatic
- Recycling: expired licenses may be reissued

### C.3 Pricing Bands (Liquidity-Aware)
- < USD 200,000 liquidity: USD 100
- USD 200,000 to < USD 1,000,000: USD 200
- USD 1,000,000 to < USD 5,000,000: USD 300
- USD 5,000,000 to < USD 15,000,000: USD 400
- >= USD 15,000,000: USD 500

### C.4 Payment Structure
- 50% in USDT
- 50% in MIC (TWAP-based valuation at activation)

### C.5 Mining Distribution Link
MICE affects participation share only. It does not modify total emission or supply cap.

### C.6 Incentive Policy (MICE Sale Phase)
- Referral cap: up to 15% of gross sales
- Group bonus cap: up to 8% of gross sales
- Incentives are phase-limited acquisition costs, not protocol runtime rewards.

### C.7 Revenue Allocation (USDT Portion)
- Referral incentives: 15%
- Group performance bonus (cap): up to 8%
- Marketing/community growth: 10%
- Liquidity provision: 35%
- Reward pools (Community + MFP): 20%
- DAO treasury/operations: 12%

### C.8 MIC Portion Allocation Principle
MIC received from MICE activations is routed by DAO policy to burn, liquidity, and treasury pathways within published governance bounds. MIC-side flows are not counted as immediate fiat/USDT runway.

### C.9 Compliance Guardrails
No guaranteed returns, no post-activation refund entitlement, no emission manipulation, and full on-chain auditability.

---

## Appendix D - Financial Projections and Capital Allocation

### D.1 Funding Model
Mission Chain uses realized cash accounting and conservative planning assumptions.

### D.2 Seed Financials (Planning Example)
- Gross target: USD 500,000
- Estimated sales/fundraising costs: 15% (USD 75,000)
- Net cash: USD 425,000

### D.3 Pre-Sale Financials (Planning Example)
- Operational target: USD 1,500,000
- Estimated costs: 33% (USD 495,000)
- Net cash: USD 1,005,000

### D.4 Operating Burn (Phase I Baseline)
- Salaries and contractors: USD 35,000/month
- Infrastructure/security/audits: USD 15,000/month
- Operations and miscellaneous: USD 5,000/month
- Total monthly burn: USD 55,000

### D.5 MICE Year-1 Conservative Scenario
- Activated MICE: 20,000
- Average price: USD 250
- Gross volume: USD 5,000,000
- USDT portion: USD 2,500,000
- Net operational USDT (after structured allocation): USD 300,000

### D.6 Consolidated Net Cash (Planning Scenario)
- Seed net: USD 425,000
- Pre-Sale net: USD 1,005,000
- MICE Year-1 net operational USDT: USD 300,000
- Total net cash: USD 1,730,000

Estimated runway at USD 55,000/month: approximately 31.5 months.

### D.7 Reporting Standard
Runway projections use realized USD/USDT only. No unrealized MIC valuation is counted as guaranteed operational runway.

---

## Appendix E - Economic Formal Specification

### E.1 Immutable Constants
- `S_max = 7,000,000,000`
- `S_pre = 1,050,000,000`
- `S_mining = 5,950,000,000`
- `T = 2,920`

### E.2 Emission Weights
- `B(t) = 2.5 * 0.95^(t/90)`
- `L(t) = clamp((TWAP7d(L_t) / L_ref)^alpha, 0.85, 1.15)`
- `w_now(t) = B(t) * L(t)`

### E.3 Cap-Safe Daily Emission
- `W_hat(t) = w_now(t) + sum_{k=t+1}^{T-1} B(k)` (future liquidity neutral assumption `L=1`)
- `E(t) = min(S_remaining(t), floor(S_remaining(t) * w_now(t) / W_hat(t)))`
- Terminal settlement: `E(T-1) = S_remaining(T-1)`

This enforces budget compliance over the mining horizon while remaining implementable without future liquidity inputs.

### E.4 Daily Allocation
- MICE participants: `0.65 * E(t)`
- DAO treasury: `0.15 * E(t)`
- MFP-NFT pool: `0.10 * E(t)`
- Community pool: `0.10 * E(t)`

### E.5 Participant Reward Equations
- MICE participant i:
  - `R_MICE_i(t) = (M_i / N_t) * 0.65 * E(t)`
- Community pool participant i:
  - `R_COMM_i(t) = (S_i / sum(S_eff)) * 0.10 * E(t)`
- MFP pool participant i:
  - `R_MFP_i(t) = (S_i / sum(S_MFP)) * 0.10 * E(t)`

---

## Appendix F - SBT and Reputation Mechanism

### F.1 Community Credentials
Silver/Gold/Platinum credentials are non-transferable, time-bound, and behavior-derived reputation credentials.

### F.2 Issuance Basis
Credentials are issued through validated competence and contribution, not purchased through sales programs.

### F.3 Lifecycle
Mint -> Validate -> Upgrade/Downgrade -> Expire/Revocation (under defined abuse and quality conditions).

### F.4 Functional Roles
Credentials gate work eligibility, governance participation scope, and review authority. They do not mint MIC and do not bypass staking rules.

---

## Appendix G - AI Governor and Economic Oracle

### G.1 Role
The Economic Oracle provides observability and advisory scenarios. It does not autonomously execute governance changes.

### G.2 Inputs
Emission/burn ratios, liquidity depth, reward concentration, staking distribution, and MICE activity.

### G.3 Human-in-the-Loop Governance
Detect -> Recommend bounded options -> DAO vote -> timelocked on-chain execution.

### G.4 Hard Limits
The Oracle cannot:
- alter supply cap,
- alter mining budget,
- bypass DAO votes,
- execute unauthorized actions.

### G.5 Optional ZK Verifiability
Future upgrades may include ZK proofs for model integrity and parameter-bound compliance without exposing sensitive internals.
