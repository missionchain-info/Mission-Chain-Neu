# Mission Chain Standardization Decisions (v1.0)

Date: 2026-02-21
Scope: Team Profile, White Paper, Appendices, Executive Portrait Standards
Status: Draft for final owner approval

## 1. Objective
This standardization package resolves structural inconsistencies across the current Mission Chain documents and produces a single coherent source of truth for public communications, investor review, and internal execution.

## 2. Canonical Terminology
- Project name: **Mission Chain**
- Token symbol: **MIC**
- Mining access license: **MICE (Mission Algorithm Mining License)**
- Reputation credentials: **Community Credentials (Silver/Gold/Platinum)**
- Long-term stewardship NFT: **MFP-NFT**
- Governance body: **Mission Chain DAO**

## 3. Canonical Economic Constants
- Maximum MIC supply: `S_max = 7,000,000,000`
- Pre-issued allocation: `S_pre = 1,050,000,000 (15%)`
- Mining allocation: `S_mining = 5,950,000,000 (85%)`
- Emission horizon: `T = 2,920 days` (approximately 8 years)

## 4. Canonical Emission Model (Cap-Safe, On-Chain Computable)
To remove contradictions between adaptive factors and fixed supply cap, the emission model is defined as follows:

- Deterministic decay baseline:
  - `B(t) = B0 * 0.95^(t/90)`
  - Recommended `B0 = 2.5` for moderate early-phase acceleration.
- Liquidity factor:
  - `L(t) = clamp((TWAP7d(L_t) / L_ref)^alpha, 0.85, 1.15)`
- Current-day weight:
  - `w_now(t) = B(t) * L(t)`
- Remaining-weight estimator (future neutrality assumption):
  - `W_hat(t) = w_now(t) + sum_{k=t+1}^{T-1} B(k)` (future `L(k)` assumed `= 1`)
- Daily emission:
  - `E(t) = min(S_remaining(t), floor(S_remaining(t) * w_now(t) / W_hat(t)))`
- Terminal settlement:
  - `E(T-1) = S_remaining(T-1)`

This guarantees:
- Total mined MIC never exceeds `S_mining`.
- Model remains adaptive to liquidity each day.
- Formula is implementable without requiring future liquidity data.
- Residual rounding drift is settled deterministically on the final day.

## 5. Mining Distribution (Unchanged)
- Active MICE miners: 65%
- DAO Treasury: 15%
- MFP-NFT pool: 10%
- Community Credential pool: 10%

## 6. Team Roster Reconciliation
Canonical leadership list includes all names currently spread across Team and White Paper documents:
1. David Truong Chinh
2. James Lee Harstad
3. John Clement
4. Hector Ardon
5. Nirmal Mukherjee
6. James Smith (Ona-Chi)
7. Aniekan Inemesit Essien
8. Melanie Pham
9. Clement Otu
10. Michael Vo

Note: White Paper and Team profiles must display the same canonical roster and role names.

## 7. Incentive Policy Normalization
### 7.1 Protocol vs Sales Incentives
- Referral and group bonuses are **sales-phase customer acquisition costs only**.
- They are not protocol yield, not passive income, and not governance rights.

### 7.2 Pre-Sale / MICE Sales Incentives
- Referral cap: up to 15% of gross sales proceeds.
- Group performance bonus cap: up to 8% of gross sales proceeds.
- Incentive logic remains differential override (direct groups only).

### 7.3 Community Credential Consistency
To avoid conflict with SBT principles:
- Sales incentives must not issue governance/reputation credentials directly.
- Any non-cash promotional reward is treated as **education credits / onboarding vouchers**, not Community Credentials.

## 8. Fundraising and Projection Consistency
- Pre-Sale hard cap from allocation math:
  - `315,000,000 MIC * $0.005 = $1,575,000`
- Financial model may still use a conservative operational target (e.g., $1,500,000), but both figures must be clearly separated:
  - Hard cap (token math)
  - Planning target (internal execution)

## 9. MICE Revenue Allocation Reconciliation
To harmonize Appendix C and D:

### 9.1 USDT Portion Allocation (cash operations)
- Referral incentives: 15%
- Group bonus (cap): up to 8%
- Marketing/community growth: 10%
- Liquidity provision: 35%
- Reward pools (Community + MFP): 20%
- DAO treasury/operations: 12%

### 9.2 MIC Portion Allocation (non-cash)
- Burn, liquidity routing, and treasury allocation are DAO-governed under fixed policy bounds.
- MIC-side allocation is excluded from immediate cash runway calculations.

## 10. Document Structure Normalization
- White Paper ToC must include Appendices **A through G**.
- Section numbering must be continuous and stable.
- Every formula referenced in main text must appear fully in appendices.
- Contact block must not include placeholders like "still updating" in public versions.

## 11. Data Governance for Public Profiles
- Public team profile version should use role, city/country, and official contact channel.
- Private addresses and personal phone numbers should be moved to internal HR/compliance records.

## 12. Portrait Standardization Rules
- One visual style for all executive photos.
- No text printed inside portrait images.
- Unified framing, background, lighting, and export dimensions.
