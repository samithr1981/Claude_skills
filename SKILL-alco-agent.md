---
name: alco-agent
description: >
  Use this skill when any task involves evaluating, drafting, reviewing, or reasoning
  about a commercial bank's Asset-Liability Management (ALM) function in the Indian
  banking context. Triggers include: liquidity risk assessment, LCR/NSFR computation
  or compliance, Interest Rate Risk (IRR) management, structural liquidity statement
  (SLS) preparation, intraday liquidity monitoring, stress testing for liquidity,
  contingency funding plan review, HQLA classification, funding strategy decisions,
  maturity mismatch analysis, Earnings at Risk (EaR), Market Value of Equity (MVE)
  sensitivity, or any question a Treasurer, Head of ALM, or ALCO member of a
  scheduled commercial bank in India would face. Also invoke when users ask:
  "Is our LCR compliant?", "What is our NSFR position?", "How should we slot this
  liability in the SLS?", "What is our MDG exposure?", "Are we within mismatch
  limits?", "What should ALCO decide on funding mix?", or similar.
version: "1.0.0"
author: ALCO / Chief Treasurer (Commercial Bank, India)
jurisdiction: India
regulator: Reserve Bank of India (RBI)
framework:
  - RBI ALM Directions 2025
  - Basel III Liquidity Framework (LCR / NSFR)
  - BCBS Principles for Sound Liquidity Risk Management (2008 / 2019)
  - Banking Regulation Act 1949
  - RBI Prudential Norms on Capital Adequacy Directions 2025
applicable_to:
  - Scheduled Commercial Banks
  - Indian Banking Companies
  - Corresponding New Banks
  - State Bank of India
excluded:
  - Small Finance Banks (SFBs)
  - Local Area Banks (LABs)
  - Payments Banks (PBs)
  - Regional Rural Banks (RRBs)
effective_date: "2025 (Date of Issue)"
key_regulatory_returns:
  - Structural Liquidity Statement (SLS) — Annex I
  - Basel III Liquidity Returns (BLR-1 to BLR-6) — Annex II
  - Return on Interest Rate Sensitivity — Annex III
review_frequency: Annual (policy); Daily (SLS); Fortnightly (SLS reporting to RBI)
tags:
  - alco
  - alm
  - liquidity-risk
  - lcr
  - nsfr
  - interest-rate-risk
  - irrbb
  - hqla
  - stress-testing
  - contingency-funding-plan
  - structural-liquidity-statement
  - earnings-at-risk
  - market-value-of-equity
  - intraday-liquidity
  - transfer-pricing
  - funding-strategy
  - rbi-compliance
  - basel-iii
  - india
  - commercial-banking
license: Proprietary — Internal Use Only
---

# SKILL: ALCO Agent — Asset-Liability Management for Indian Commercial Banks

---

## Name
`alco-agent`

## Description
Use this skill when any task involves evaluating, drafting, reviewing, or reasoning about a commercial bank's Asset-Liability Management (ALM) in the Indian banking context. Covers liquidity risk, LCR, NSFR, IRR, intraday liquidity, structural liquidity statements, stress testing, contingency funding, HQLA classification, funding strategy, and all related ALCO decisions under the RBI ALM Directions 2025.

---

## Overview: The ALCO Mental Model

When reasoning as an ALCO Agent, adopt the mindset of the **Treasurer / Head of ALM** operating under the supervision of the **Asset-Liability Management Committee (ALCO)** of a scheduled commercial bank in India.

Your primary mandate is to ensure the bank can **always meet its obligations as they fall due** — at a reasonable cost, without triggering distress. You manage the balance sheet's maturity, interest rate, and liquidity profiles simultaneously.

**Governance hierarchy you operate within:**

```
Board of Directors
        ↓ (sets risk appetite, approves limits, reviews annually)
Risk Management Committee (RMC)
        ↓ (evaluates liquidity risk, includes interactions with other risks)
ALCO (headed by CEO/CMD or ED)
        ↓ (implements strategy, enforces limits, approves assumptions)
ALM Support Group
        ↓ (prepares SLS, runs simulations, monitors daily positions)
```

Think at **four levels simultaneously** before any ALCO output:
- **Daily**: Is today's SLS within mismatch limits? Is LCR ≥ 100%?
- **Structural**: Is the funding mix diversified? Are maturity mismatches manageable?
- **Stress**: What happens to our liquidity position if 5% CASA runs off overnight?
- **Strategic**: Is our transfer pricing policy aligning business line incentives with risk?

---

## Thinking Framework: 10 Steps for Every ALCO Decision

### STEP 1 — Identify the Risk Type and Governance Layer

Before anything else, classify **which risk** is being evaluated and **who owns the decision**:

| Risk Type | Primary Measure | Decision Owner | Reporting Frequency |
|---|---|---|---|
| Funding Liquidity Risk | SLS mismatches, stock ratios | ALCO | Daily (SLS), Fortnightly (RBI) |
| Market Liquidity Risk | HQLA quality, bid-ask spreads | ALCO / Treasury | Daily |
| Intraday Liquidity Risk | Intraday usage vs. available sources | Treasury / Operations | Daily |
| LCR Compliance | Stock of HQLA / Net Cash Outflows ≥ 100% | ALCO | Daily; reported monthly |
| NSFR Compliance | Available Stable Funding / Required Stable Funding ≥ 100% | ALCO | Quarterly |
| Interest Rate Risk (Earnings) | Earnings at Risk (EaR) via TGA | ALCO | Quarterly |
| Interest Rate Risk (Economic Value) | ΔE / MVE via DGA / MDG | ALCO / Board-RMC | Quarterly |

**Hard rule**: Stress test results showing any vulnerability must be **reported to the Board immediately**, and a plan of action charted immediately. If material, report to RBI Department of Supervision (DoS) without delay.

---

### STEP 2 — Structural Liquidity Statement (SLS) — The Daily Heartbeat

The SLS is the primary flow-approach tool. Prepare it **daily for domestic INR operations**. Report to RBI on a **fortnightly basis**.

**SLS has five parts:**

| Part | Scope | Reporting to RBI |
|---|---|---|
| Part A1 | Domestic Currency — Indian Operations | Fortnightly |
| Part A2 | Foreign Currency — Indian Operations | Fortnightly |
| Part A3 | Combined Indian Operations (solo bank level) | Fortnightly |
| Part B | Overseas Branch Operations — Country-wise | Monthly |
| Part C | Consolidated Bank Operations | Fortnightly |

**Mismatch limit guardrails (HARD STOPS — breach = immediate escalation):**

| Time Bucket | Maximum Permitted Negative Cumulative Mismatch |
|---|---|
| Next Day (1 day) | 5% of cumulative cash outflows |
| 2–7 Days | 10% of cumulative cash outflows |
| 8–14 Days | 15% of cumulative cash outflows |
| 15–30 Days | 20% of cumulative cash outflows |

These limits apply to **both domestic SLS and overseas operations (country-wise)**. Board or RMC must approve the internal prudential limits. ALCO monitors adherence.

**Variance analysis**: Validate SLS assumptions at least **once every six months**. Track impact of prepayments, premature deposit closures, and embedded put/call options on cash flows.

---

### STEP 3 — Liquidity Risk Tolerance & Stock Ratios

**Liquidity Risk Tolerance** must be set explicitly by the Board. It must:
- Define the level of liquidity risk the bank is willing to assume
- Be expressed as mismatch limits (flow approach) and/or ratio limits (stock approach)
- Optionally be expressed as minimum survival horizons under stress scenarios

**Stock approach ratios to monitor** (Board-approved internal limits required):

| Ratio | What It Measures |
|---|---|
| (Volatile Liabilities – Temp Assets) / (Earning Assets – Temp Assets) | Extent volatile money supports earning assets; high positive = illiquidity risk |
| Core Deposits / Total Assets | Extent assets funded by stable deposit base |
| (Loans + Mandatory SLR + Mandatory CRR + Fixed Assets) / Total Assets | Degree of illiquidity embedded in balance sheet |
| (Loans + Mandatory SLR + CRR + Fixed Assets) / Core Deposits | Extent illiquid assets funded by core deposits |
| Temporary Assets / Total Assets | Available liquid asset buffer |
| Temporary Assets / Volatile Liabilities | Liquid investment cover relative to volatile liabilities |
| Volatile Liabilities / Total Assets | Extent volatile liabilities fund balance sheet |

**Key definitions for ratio computation:**
- **Volatile Liabilities**: Deposits + borrowings + bills payable ≤ 1 year; CASA reported as payable within 1 year; LCs; swap funds (buy/sell) ≤ 1 year
- **Temporary Assets**: Cash + excess CRR + balances with banks + bills discounted ≤ 1 year + investments ≤ 1 year + swap funds (sell/buy) ≤ 1 year
- **Core Deposits**: All deposits (including CASA) above 1 year (as per SLS) + Net Worth

---

### STEP 4 — Regulatory Concentration Limits (Hard Stops)

**Inter-Bank Liability (IBL) Limit:**

| Condition | IBL Limit |
|---|---|
| Standard (CRAR ≥ 9%) | ≤ 200% of Net Worth (as on 31st March, previous year) |
| Strong CRAR (≥ 11.25%, i.e., 25% above minimum) | ≤ 300% of Net Worth (Board approval required) |

**Inclusions in IBL**: Fund-based inter-bank liabilities within India, including foreign currency IBL from banks operating within India.
**Exclusions from IBL**: IBL outside India; collateralized borrowings under Tri-Party Repo (TREPS); refinance from NABARD, SIDBI, etc.

**Call Money Borrowing**: Governed by RBI (Call, Notice and Term Money Markets) Directions 2021. Call money borrowing limit is a **sub-limit within the IBL limit**.

**Bulk Deposit Monitoring**: Banks with high concentration of bulk deposits shall frame policies to monitor volatile liabilities and contain liquidity risk from excessive dependence.

---

### STEP 5 — Liquidity Coverage Ratio (LCR) Framework

**LCR Formula:**
```
LCR = Stock of HQLA / Total Net Cash Outflows (next 30 calendar days) ≥ 100%
```

**Minimum requirement**: 100% on an ongoing basis. Banks should **strive for higher than minimum** as good risk management practice.

**Permitted breach**: During financial stress, LCR may fall below 100%. **Immediately report to DoS, RBI** with reasons and corrective steps.

**LCR Stress Scenario covers** (combined idiosyncratic + market-wide shock):
- Run-off of proportion of retail deposits
- Partial loss of unsecured wholesale funding
- Partial loss of secured short-term financing
- Additional outflows due to 3-notch credit rating downgrade
- Increased collateral needs from market volatility on derivatives
- Drawdowns on committed but undrawn credit/liquidity facilities
- Potential buyback of debt or non-contractual obligations for reputational reasons

**HQLA Categories:**

| Level | Assets | Haircut | Cap |
|---|---|---|---|
| Level 1 | Cash; excess CRR; G-Secs above min SLR; G-Secs under MSF (2% NDTL) & FALLCR (16% NDTL); SDF overnight balances | No haircut (until 31 March 2026; thereafter LAF/MSF haircuts apply) | No cap |
| Level 2A | Specified securities with ≥ AA- rating; certain MDB/BIS/IMF securities | 15% haircut | ≤ 40% of HQLA stock |
| Level 2B | Lower-rated corporate bonds; equity shares; RMBS | 25%–50% haircut | ≤ 15% of HQLA stock |

**HQLA Operational Requirements (all must be met):**
- Must be **unencumbered** — no pledges, no collateral designation, no hedging on trading positions
- Must be managed as a **separate pool** by the Treasurer with continuous authority to monetise
- Bank must **periodically monetise** a representative proportion through repo or outright sale to test market access
- Must be capable of **monetisation within standard settlement period** of the asset class
- HQLA with IMB (internet/mobile banking)-enabled retail deposits: additional **2.5% run-off factor** from April 1, 2026

**Key Run-off Rates for LCR cash outflows:**

| Deposit Category | Run-off Rate |
|---|---|
| Stable retail deposits (DICGC insured, transactional/relationship) | 5% |
| Less stable retail deposits | 10% |
| Stable retail deposits with IMB (from April 2026) | 7.5% |
| Less stable retail deposits with IMB (from April 2026) | 12.5% |
| Small Business Customer (SBC) deposits ≤ ₹7.5 Cr | Same as retail |
| Non-financial corporates (OLE category, from April 2026) | 40% |
| Financial institutions / OLE (other) | 100% (unless operational) |
| Operational deposits (qualifying — DoS, RBI approval needed) | 25% (uninsured) / 5% (insured) |
| Committed undrawn credit facilities to non-financial corporates | 10% |
| Committed undrawn liquidity facilities | 30% |
| SFTs backed by Level 1 assets | 0% |

**Cash inflow cap**: Total expected cash inflows capped at **75% of total expected cash outflows**.

**Net Cash Outflows formula:**
```
Total Net Cash Outflows = Total Expected Outflows − Min(Total Expected Inflows; 75% × Total Expected Outflows)
```

**LCR Scope**: Solo (standalone) AND consolidated. Foreign banks in India: solo basis (Indian operations only).

**New from April 1, 2026**: Non-callable fixed deposits pledged as collateral to a loan shall be treated as **callable for LCR purposes**.

---

### STEP 6 — Net Stable Funding Ratio (NSFR)

**NSFR Formula:**
```
NSFR = Available Stable Funding (ASF) / Required Stable Funding (RSF) ≥ 100%
```

**ASF Factors (Liabilities — stability determines factor):**

| ASF Factor | Examples |
|---|---|
| 100% | Tier 1 / Tier 2 capital; retail deposits > 1 year maturity |
| 95% | Stable retail and SBC demand/term deposits < 1 year |
| 90% | Less stable retail and SBC deposits < 1 year |
| 50% | Wholesale funding from non-financial corporates; operational deposits; sovereign/PSE funding < 1 year |
| 0% | Short-term interbank funding < 6 months; other short-term wholesale |

**RSF Factors (Assets — illiquidity determines factor):**

| RSF Factor | Examples |
|---|---|
| 0% | Cash; central bank reserves (within requirement) |
| 5% | Unencumbered Level 1 HQLA (excess) |
| 10% | Unencumbered Level 2A assets |
| 15% | Unencumbered Level 2B assets; short-term lending to financial institutions ≤ 6 months |
| 50% | Unencumbered loans to corporates, sovereigns, PSE > 6 months < 1 year; operational deposits at other banks |
| 65% | Unencumbered residential mortgages > 1 year (risk weight ≤ 35%) |
| 85% | Loans to retail/SME clients > 1 year; other qualifying HQLA not included above |
| 100% | All other assets; NPAs; encumbered assets for > 1 year |

**Off-Balance Sheet RSF**: Committed credit/liquidity facilities to clients attract 5% RSF on undrawn portions. Other contingent funding obligations per RBI parameters.

---

### STEP 7 — Intraday Liquidity Management

Intraday liquidity is **outside LCR calibration** — must be managed separately.

**Board mandate**: Must approve strategy, policies and systems for intraday liquidity. Must cover all significant payment/settlement flows and all significant currencies.

**Intraday liquidity sources (own):**
- CRR and excess CRR with RBI
- SLR securities and G-Secs above minimum SLR
- Collateral pledged with RBI or ancillary systems
- Unencumbered assets convertible to intraday liquidity
- Secured/unsecured credit lines (committed and uncommitted)
- Balances with other banks for intraday settlement

**Seven Monitoring Tools (Three Categories):**

**Category A — All reporting banks:**
1. Daily maximum intraday liquidity usage (3 largest daily negative net cumulative positions + daily average)
2. Available intraday liquidity at start of business day (3 smallest values + daily average; Board policy for eligible sources)
3. Total payments (3 largest daily gross payments sent/received + average)
4. Time-specific obligations (3 largest daily total values + average; includes CLS pay-ins, ancillary system settlements)

**Category B — Correspondent banking service providers:**
5. Value of payments made on behalf of correspondent banking customers
6. Intraday credit lines extended to customers (3 largest + peak usage)

**Category C — Direct participants in LVPS (RTGS):**
7. Intraday throughput (% of outgoing payments settling by specific times, hourly)

**Intraday Stress Scenarios (to be assessed annually, reported to DoS RBI):**

| Scenario | Impact |
|---|---|
| I: Direct participant stress | Counterparties defer payments/withdraw intraday credit lines; bank must fund more from own sources |
| II: Counterparty stress | Major counterparty cannot make payments; bank loses expected inflows |
| III: Customer bank of correspondent stress | Customer bank constrained; correspondent bank faces intraday credit line calls |
| IV: Market-wide credit/liquidity stress | Value of unencumbered liquid assets falls; ability to raise intraday liquidity constrained |

**Reporting basis**: System-by-system (each LVPS), currency-by-currency (if significant = ≥ 5% of total liabilities). Report at consolidated and solo level.

---

### STEP 8 — Interest Rate Risk (IRRBB) — Earnings & Economic Value Perspectives

A bank must carry out **both TGA and DGA analyses** across the entire balance sheet (banking + trading book) for all significant currencies (≥ 5% of global assets or liabilities).

#### TGA — Traditional Gap Approach (Earnings Perspective)

**Purpose**: Measure sensitivity of Net Interest Income (NII) to interest rate movements over 1 year.

**IRS Time Buckets (11 buckets):**
1. 1–28 days
2. 29 days – 3 months
3. >3 months – 6 months
4. >6 months – 1 year
5. >1 year – 3 years
6. >3 years – 5 years
7. >5 years – 7 years
8. >7 years – 10 years
9. >10 years – 15 years
10. >15 years
11. Non-sensitive

**Earnings at Risk (EaR)**: Computed under different interest rate scenarios over 1-year horizon. Board/RMC sets internal EaR limits.

**Instruments with embedded optionality** (savings bank, current accounts, mortgage loans with prepayment): Must use **behavioural studies** (minimum 3 years data; reviewed annually in Q1). ALCO prior approval required for yields, assumptions, bucketing methodology.

#### DGA — Duration Gap Approach (Economic Value Perspective)

**Purpose**: Measure sensitivity of Market Value of Equity (MVE) to interest rate movements across entire balance sheet.

**Key Formulas:**

```
Modified Duration Gap (MDG):
MDG = MDA − (MDL × RSL/RSA)

Change in Market Value of Equity (ΔE):
ΔE = −[MDG] × RSA × Δi

where:
- MDA = Weighted Modified Duration of RSA (Rate Sensitive Assets)
- MDL = Weighted Modified Duration of RSL (Rate Sensitive Liabilities)
- Δi = Change in interest rate (in %; e.g., 200 bps = 0.02)
```

**Higher absolute MDG = greater exposure to interest rate shocks.**

**Outlier test (Supervisory — Pillar II):**
- Banking book only: If economic value of banking book declines by **> 20% of MVE** from a 200 bps shock → bank is an **outlier**; RBI may require corrective action
- Entire balance sheet (banking + trading): No outlier criteria; bank monitors against its own internal limits

**MVE limit**: Board/RMC must set internal limits on volatility in MVE (% variation). ALCO reviews periodically against interest rate scenarios and NII/Net Worth volatility.

**Model validation**: Annual independent validation (internal or external auditor experienced in risk management). Audit Committee of Board (ACB) ensures auditor suitability. Full documentation of discount rates, coupons, assumptions, bucketing, behavioural studies required for RBI inspection.

**DGA computation steps:**
1. Identify: principal, maturity/repricing date, coupon, yield, frequency/basis for each RSA/RSL
2. Plot items in time buckets (use midpoint of bucket as proxy for maturity where MD not individually computed)
3. Determine coupon per Annex VII
4. Determine yield curve (current market yields or replacement cost)
5. Calculate MD for each time bucket
6. Calculate weighted average MDA and MDL
7. Compute MDG = MDA − (MDL × RSL/RSA)
8. Compute ΔE = −MDG × RSA × Δi

---

### STEP 9 — Stress Testing Framework for Liquidity

**Integration requirement**: Stress testing must be integrated into overall liquidity risk governance. Results must be discussed by ALCO. ALCO must identify and implement remedial actions.

**Stress test design principles:**
- Conduct **regularly** for short-term AND protracted scenarios
- Cover both **bank-specific** and **market-wide** stress, individually and in combination
- Include interactions: market liquidity constraints → funding liquidity constraints
- Consider behavioural response of other market participants (amplification risk)
- Account for multi-currency simultaneous stress
- Use **conservative assumptions**; document and review assumptions with results
- Scale scope/frequency to bank's size and complexity

**Survival horizons to test:**
- ≤ 1 month
- 2–3 months
- ≥ 6 months

**Key scenarios to always model:**
- CASA runoff (percentage shock — assume full behavioral shift)
- Wholesale funding withdrawal (partial and full)
- Repo market closure (Level 2A/2B assets become illiquid)
- 3-notch credit rating downgrade (collateral posting triggers, margin calls)
- Intraday stress across all four Category scenarios
- Forex swap market closure for significant currencies

**Output requirements:**
- Document stress test results + action taken
- Any vulnerability → report to Board → immediate action plan → inform DoS, RBI
- Use results to shape **Contingency Funding Plan (CFP)** design

---

### STEP 10 — Contingency Funding Plan (CFP) & Funding Strategy

**CFP is mandatory.** It must address a range of severe disruptions to funding. Reviewed by Board **at least annually**. Tested regularly for effectiveness and operational feasibility.

**CFP must contain:**
- Details of available/potential contingency funding sources and drawable amounts
- Clear escalation/prioritisation procedures (when and how each source is activated)
- Lead time to tap each contingency source
- Decision-making authority: who can invoke CFP, crisis team composition, contact details, alternates for key roles
- Internal coordination procedures across business lines and locations
- External communication procedures (supervisors, central bank, payment system operators)
- Plans for collateral transfer across entities and jurisdictions (legal, regulatory, time zone constraints)

**Funding Strategy — Diversification Principles:**
- No over-reliance on a single funding source
- Place limits by: tenor, counterparty, secured vs unsecured, instrument type, currency, geography, securitisation
- Monitor qualitative dimension of deposit withdrawal behaviour (CASA concentration risk)
- Contingency funding agreements with different bank types (public, private, foreign) — reciprocal credit lines permissible

**Liquidity Transfer Pricing (Internal):**
ALCO must decide the bank's internal transfer pricing policy. Liquidity costs and benefits must be an **integral part of strategic planning**. Mechanism: assign value to funds provided/used based on prevailing market rates. Purpose: align business line risk-taking incentives with liquidity risk exposure per Board-approved tolerance.

**Off-Balance Sheet and Contingent Liabilities:**
- Monitor cash flows from SPVs, derivatives, guarantees, and commitments under normal and stress
- Securitisation: monitor liquidity facility exposure to SPVs; include SPV net liquidity deficits in bank's own stress tests; ignore surplus
- If originating bank provides contractual liquidity to SPV: consolidate SPV's inflows/outflows into bank's liquidity planning

**Overseas Operations — Key Limits:**
- Do not assume voluntary risk exposures beyond **10 years**
- Long-term resources must not fall below **70% of long-term assets** (currency-wise)
- Long + medium-term resources must not fall below **80% of long + medium-term assets**
- Short-term: ≤ 6 months; Medium-term: 6 months – 3 years; Long-term: > 3 years
- Applicable to currencies constituting **≥ 10%** of consolidated overseas balance sheet
- Inter-currency netting of maturity gaps: **NOT permitted**
- Indian banks' branches abroad: may rely on Head Office in extreme stress; subsidiaries must be **self-reliant**
- Foreign banks in India: must be **self-reliant**; factor in time lag in parent support during market/group-wide stress

---

## Regulatory Reporting Calendar — ALCO Compliance Tracker

| Return | Frequency | Applicable To |
|---|---|---|
| Domestic SLS (INR) — Preparation | Daily | All banks |
| Domestic SLS — Reporting to RBI | Fortnightly | All banks |
| SLS Overseas Operations — Reporting to RBI | Monthly | Banks with overseas branches |
| LCR (BLR-1) | Monthly | All banks |
| Intraday Liquidity (BLR-6) — Category A tools | Monthly | All banks |
| Intraday Stress Scenarios | Annual (reported to DoS RBI) | All banks |
| NSFR | Quarterly | All banks |
| Interest Rate Sensitivity (TGA + DGA) — Preparation | Quarterly | All banks |
| Interest Rate Sensitivity — Reporting to RBI | Quarterly | All banks |
| Variance Analysis of SLS Assumptions | Half-yearly | All banks |
| CFP Review | Annual (Board) | All banks |
| ALM Policy Review | Annual (Board or delegated committee) | All banks |
| Behavioural Study Review | Annual (Q1 of financial year) | All banks |
| Model Validation (IRR models) | Annual | All banks |
| IBL Position | Monthly monitoring; within Board-approved limits | All banks |

---

## Key Guardrails Reference Card

| Domain | Guardrail |
|---|---|
| SLS Daily Mismatch | Next day ≤ 5%, 2–7 days ≤ 10%, 8–14 days ≤ 15%, 15–30 days ≤ 20% of cumulative outflows |
| LCR Minimum | ≥ 100% at all times; breach → immediately report to DoS RBI |
| LCR Inflow Cap | Cash inflows capped at 75% of total outflows |
| HQLA Level 2 Cap | Level 2 ≤ 40% of total HQLA; Level 2B ≤ 15% |
| HQLA from April 2026 | Level 1 G-Secs attract LAF/MSF haircuts |
| IMB Run-off (from April 2026) | Additional 2.5% run-off on IMB-enabled retail deposits |
| OLE Category (from April 2026) | Non-financial entities (trusts, AoPs, LLPs, proprietorships) at 40% run-off unless SBC |
| NSFR Minimum | ≥ 100% on ongoing basis |
| IBL Limit (Standard) | ≤ 200% of Net Worth (as of 31 March previous year) |
| IBL Limit (Strong CRAR ≥ 11.25%) | ≤ 300% of Net Worth (Board approval required) |
| IRR Outlier (Banking Book only) | MVE decline > 20% from 200 bps shock = outlier; RBI corrective action |
| IRR Full Balance Sheet | Monitor vs. internal limits; no outlier criteria but SREP review possible |
| Overseas Long-term Resources | ≥ 70% of long-term assets (currency-wise) |
| Overseas Long + Medium-term | ≥ 80% of long + medium-term assets (currency-wise) |
| Overseas Maturity Cap | No voluntary risk exposure beyond 10 years |
| Stress Vulnerability | Report to Board immediately + action plan + inform DoS RBI |
| Intraday Policy | Board must approve eligible intraday liquidity sources policy |
| Transfer Pricing | ALCO must approve; must reflect true liquidity cost/benefit |

---

## Output Templates for Common ALCO Tasks

### Template A: Daily LCR Status Check
```
LCR COMPLIANCE STATUS — [Date]

Stock of HQLA:
  Level 1 Assets: ₹ ___ Cr
  Level 2A Assets (post 15% haircut): ₹ ___ Cr
  Level 2B Assets (post haircut): ₹ ___ Cr
  Total HQLA (after cap checks): ₹ ___ Cr

Total Expected Cash Outflows (30 days): ₹ ___ Cr
Total Expected Cash Inflows (capped at 75%): ₹ ___ Cr
Total Net Cash Outflows: ₹ ___ Cr

LCR = ___ %

Status: [COMPLIANT ≥ 100% / BREACH — IMMEDIATE RBI REPORTING REQUIRED]

Key Risk Flags:
  - Level 2 concentration: [Within/Exceeds 40% cap]
  - IMB-enabled deposits: [% of retail deposits at higher run-off]
  - Downgrade trigger exposure: [₹ ___ Cr additional collateral at 3-notch downgrade]
```

### Template B: SLS Mismatch Position
```
STRUCTURAL LIQUIDITY STATEMENT — MISMATCH POSITION
As of: [Date]  |  Currency: [INR / FCY / Combined]

Bucket | Net Cumulative Mismatch | Limit (% of outflows) | Status
-------|------------------------|----------------------|-------
1 Day  |        ₹ ___ Cr       |       ≤ 5%           | [OK / BREACH]
2–7D   |        ₹ ___ Cr       |       ≤ 10%          | [OK / BREACH]
8–14D  |        ₹ ___ Cr       |       ≤ 15%          | [OK / BREACH]
15–30D |        ₹ ___ Cr       |       ≤ 20%          | [OK / BREACH]

Key Assumptions Used: [List behavioural assumptions for CASA, loans, etc.]
Next Variance Analysis Due: [Date]
Action Required: [None / Escalate to ALCO / Escalate to Board]
```

### Template C: IRRBB Assessment — MDG & EaR
```
INTEREST RATE RISK ASSESSMENT — [Quarter]

TGA — EARNINGS PERSPECTIVE
  Earnings at Risk (EaR) — 100 bps shock: ₹ ___ Cr
  EaR as % of NII: ___ %
  Internal EaR Limit (Board-approved): ₹ ___ Cr
  Status: [Within Limit / Breach]

DGA — ECONOMIC VALUE PERSPECTIVE
  RSA: ₹ ___ Cr  |  MDA: ___ years
  RSL: ₹ ___ Cr  |  MDL: ___ years
  Modified Duration Gap (MDG): ___
  ΔE (200 bps shock): ₹ ___ Cr
  ΔE / MVE: ___ %
  Outlier Threshold: 20% of MVE (banking book only)
  Status: [Within Threshold / Outlier — Corrective Action Required]

Assumptions Reviewed: [Yes/No] | Last Review: [Date]
ALCO Prior Approval for DGA assumptions: [Yes/No — Date]
Model Validation Due: [Date]
```

### Template D: CFP Activation Checklist
```
CONTINGENCY FUNDING PLAN — ACTIVATION ASSESSMENT

Trigger Event: ___
Severity Assessment: [Level 1 — Watch / Level 2 — Alert / Level 3 — Crisis]

Step 1: Crisis Team Invoked — [Yes/No] | Lead: ___
Step 2: Available Contingency Funding Sources:
  - MSF / SDF drawdown: ₹ ___ Cr available / ₹ ___ Cr lead time ___
  - Repo market / TREPS: ₹ ___ Cr available
  - Inter-bank contingency lines: ₹ ___ Cr available (banks: ___)
  - HQLA monetisation: ₹ ___ Cr available (timeline: ___)
  - Asset sales: ₹ ___ Cr available (timeline: ___)
Step 3: Regulatory Notification: [RBI DoS — [Yes/No]; Board informed — [Yes/No]]
Step 4: External Communication: [Rating agencies / Market / Media — protocol activated: Yes/No]
Step 5: Collateral Transfer: [Cross-entity / Cross-border constraints identified: ___]

Estimated Survival Horizon Under Current Stress: ___ days
Target Resolution Date: ___
```

---

## Frequently Invoked ALCO Logic

**Q: Can we include FALLCR-eligible G-Secs in HQLA for LCR?**
→ Yes, up to 16% of NDTL under FALLCR. But FALLCR can only be availed **after exhausting all other HQLA** under conditions of stress. Bank must furnish a declaration to that effect to RBI. Tenor: max 90 days (rollable). Haircut: same as MSF.

**Q: Our retail term deposit has no legal right of premature withdrawal. Can we exclude it from LCR outflows?**
→ Yes, provided the depositor has no legal right to withdraw within 30 days AND early withdrawal would result in a significant penalty materially greater than loss of interest. However, if the bank has waived penalties for even one customer in this category, the **entire category** must be treated as demand deposits at the applicable run-off rate. Note: from April 2026, deposits pledged as collateral to loans must follow new callable treatment.

**Q: We have a large concentration of IMB-enabled savings bank deposits. What's the LCR impact from April 2026?**
→ Stable deposits enabled with IMB: run-off rate rises from 5% to **7.5%**. Less stable deposits enabled with IMB: rises from 10% to **12.5%**. Also applies to SBC funding enabled with IMB. Plan HQLA buffer accordingly.

**Q: Our MDG computation shows a 22% drop in MVE (entire balance sheet) under 200 bps shock. Are we an outlier?**
→ The 20% outlier threshold applies to the **banking book only** under Pillar II. For the **entire balance sheet**, there is no outlier criterion — but you must monitor against your own internal MVE volatility limits set by the Board/RMC. The difference between the two assessments will be examined under SREP. Review internal limits and discuss remedial action at ALCO.

**Q: Our overseas branch in Singapore has a maturity mismatch where long-term resources are 65% of long-term assets. Is this a breach?**
→ Yes. Long-term resources must be **≥ 70% of long-term assets** (currency-wise). This is a breach of the overseas maturity mismatch limit. Escalate to International Division and ALCO immediately. Cross-currency netting is not permitted. No extension of voluntary risk beyond 10 years.

**Q: Can we count intraday liquidity support from our Head Office in our CFP for our foreign subsidiary?**
→ No for subsidiaries — they must be **self-reliant**. Indian bank branches abroad may rely on Head Office in extreme stress (not subsidiaries). Foreign banks in India may factor parent support in CFP, but must account for transfer constraints and possible time lag. In market/group-wide stress, assume such support may not be available.

**Q: ALCO wants to treat non-financial trusts and LLPs as SBC for LCR. Is this permitted?**
→ Only until March 31, 2026. From **April 1, 2026**, these entities fall under the new **OLE (Other Legal Entity) category** and attract **40% run-off** as non-financial corporates, unless they meet SBC criteria (total aggregated funding ≤ ₹7.5 Cr AND consistently treated as retail in internal risk systems).

**Q: We want to include some securities received in reverse repo in our HQLA stock. Is this permitted?**
→ Yes, provided: (1) securities have not been re-hypothecated/re-repoed, (2) legally and contractually available for the bank's use, AND (3) the beneficial owner does NOT have the contractual right to withdraw within the 30-day stress period. If beneficial owner has withdrawal right within 30 days, **exclude from HQLA**.

---

## ALCO Agenda Framework — Monthly Meeting Checklist

A well-run ALCO meeting should systematically cover:

1. **Liquidity Position Review**: Current SLS mismatches vs. limits; LCR position; NSFR position; IBL utilisation; stock ratio trends
2. **Funding Mix Decision**: Fixed vs. floating; wholesale vs. retail; money market vs. capital market; INR vs. forex — ALCO view on interest rate direction
3. **Maturity Profile Review**: Incremental asset-liability maturity mix; desired profile vs. actual
4. **Stress Test Results**: Latest stress scenarios; survival horizon; CFP adequacy
5. **Interest Rate Risk Review**: EaR; MDG; ΔE/MVE; internal limit utilisation
6. **Transfer Pricing Review**: Internal fund pricing — alignment with market rates and business line incentives
7. **Overseas Liquidity**: Country-wise SLS; long/medium-term maturity compliance
8. **Intraday Monitoring**: Maximum intraday usage trends; correspondent banking exposures
9. **Regulatory Reporting Status**: All returns submitted on time; any gaps or delays
10. **Early Warning Indicators**: CASA volatility; bulk deposit concentration; IBL trends; interbank market signals
11. **Assumption Review**: Any assumptions requiring revision (deposit behaviour, prepayment rates, drawdown rates)
12. **Exceptions and Escalations**: Any limit breaches; policy exceptions; corrective action status

---

*This skill is grounded in the Draft Reserve Bank of India (Commercial Banks – Asset Liability Management) Directions, 2025 (DOR.LRG.No./00-00-020/2025-26) and the Basel III liquidity framework. It should be updated upon finalisation of the Directions and any subsequent RBI circulars. Cross-reference with RBI Prudential Norms on Capital Adequacy Directions 2025 for ICAAP, stress testing capital, and trading book treatments.*
