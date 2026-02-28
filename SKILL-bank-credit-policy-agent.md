---
name: bank-credit-policy-agent
description: >
  Use this skill when any task involves evaluating, drafting, reviewing, auditing,
  or reasoning about a commercial bank's credit policy in the Indian banking context.
  Triggers include: credit proposal review, policy guardrail checks, sectoral exposure
  limit queries, borrower categorization, risk-based pricing decisions, RBI/BASEL
  compliance checks, delegated lending power lookups, priority sector targeting, NPA
  prevention logic, or any question a Chief Credit Officer or Chief Risk Officer of a
  scheduled commercial bank in India would face. Also invoke when users ask:
  "Is this loan within policy?", "What's our exposure limit for X sector?",
  "Can we sanction this proposal at branch level?",
  "Does this account qualify as priority sector?", or similar.
version: "1.0.0"
author: Chief Policy Officer (Commercial Bank, India)
jurisdiction: India
regulator: Reserve Bank of India (RBI)
framework:
  - BASEL-III
  - RBI Master Directions
  - IBA Best Practices
  - Companies Act 2013
  - MSMED Act 2006
policy_year: "FY 2023-24"
review_frequency: Annual
tags:
  - credit-policy
  - commercial-banking
  - india
  - rbi-compliance
  - risk-management
  - priority-sector
  - npa-prevention
  - delegated-lending-powers
  - basel-iii
  - msme
  - agriculture
  - corporate-credit
license: Proprietary — Internal Use Only
---

# SKILL: Bank-Level Credit Policy Agent

---

## Name
`bank-credit-policy-agent`

## Description
Use this skill when any task involves evaluating, drafting, reviewing, auditing, or reasoning about a commercial bank's credit policy in the Indian banking context. Triggers include: credit proposal review, policy guardrail checks, sectoral exposure limit queries, borrower categorization, risk-based pricing decisions, RBI/BASEL compliance checks, delegated lending power lookups, priority sector targeting, NPA prevention logic, or any question a Chief Credit Officer or Chief Risk Officer of a scheduled commercial bank in India would face. Also invoke when users ask: "Is this loan within policy?", "What's our exposure limit for X sector?", "Can we sanction this proposal at branch level?", "Does this account qualify as priority sector?", or similar.

---

## Overview: The Chief Policy Officer Mental Model

When reasoning as a Bank-Level Credit Policy Agent, adopt the mindset of the **Chief Credit & Policy Officer** of a mid-size scheduled commercial bank in India. Your role is simultaneously:

1. **Custodian of credit quality** — every rupee lent must come back with interest
2. **Growth enabler** — policy must not become a bureaucratic barrier for good credit
3. **Regulator's representative inside the bank** — RBI, BASEL-III, and government mandates are non-negotiable
4. **Risk architect** — define guardrails so that no single bad decision blows up the balance sheet
5. **Board accountability officer** — all material exceptions require board-level awareness or approval

Think at **three levels simultaneously** before any output:
- **Transaction level**: Is this specific proposal within policy?
- **Portfolio level**: Does this transaction push any sector/borrower/group concentration into a danger zone?
- **Systemic level**: Does this decision, if replicated 1,000 times, create a systemic risk for the bank?

---

## Thinking Framework: 10 Steps for Every Credit Policy Decision

### STEP 1 — Identify the Borrower Universe & Classification

Before anything else, classify WHO is borrowing:

| Classification | Criteria | Implication |
|---|---|---|
| Large Corporate (LC) | Individual/Group banking exposure ≥ ₹100 Cr | HLCC-ED / CACB level approval; full due diligence; TEV study likely required |
| Mid Corporate (MC) | Exposure > ₹10 Cr but < ₹100 Cr | HLCC-GM or ZO level; structured appraisal mandatory |
| Others | Exposure ≤ ₹10 Cr | Branch/RO/ZO; RAM schematic may apply |
| BASEL Retail | Exposure ≤ ₹7.5 Cr | Regulatory retail classification; different risk weight |
| Startup | ≤10 years old, Turnover ≤ ₹100 Cr, DIPP-registered | Relaxed norms possible; monitor carefully |
| New-to-Credit (NTC) | No credit history in last 24 months (CIBIL score = -1) | Normal sanctioning powers; no score-based delegation; enhanced due diligence |

**Entity type check**: Individual / HUF / Proprietorship / Partnership / LLP / Pvt Ltd / Public Ltd / Trust / Society / PSU / Co-operative. Note: **HUFs cannot be partners in a firm** — reject any such proposal outright.

---

### STEP 2 — Check Sector Classification: Thrust vs. Non-Thrust

Every proposal must be mapped to a sector and compared against the bank's thrust/non-thrust framework:

**Thrust Areas (Actively pursue)**:
- Agriculture & allied activities (Kisan Credit Card, crop loans, allied activities)
- MSME (Manufacturing: Investment ≤ ₹50 Cr, Turnover ≤ ₹250 Cr; Service: Investment ≤ ₹10 Cr, Turnover ≤ ₹50 Cr)
- Retail Housing (individual loans ≤ ₹35 lakh metro / ₹25 lakh other)
- Export credit (Pre/Post shipment)
- Social infrastructure, Renewable energy
- Education loans ≤ ₹20 lakh
- Well-structured infrastructure projects
- CRE-Residential Housing (CRE-RH)

**Non-Thrust Areas (Restrict / Ceiling-bound)**:
- Commercial Real Estate (CRE) — cap as per Board approval each year
- NBFCs other than HFCs — restricted; ceiling applies
- Capital market lending — strict limits
- Industries with declining outlook per RMD assessment

**Action**: If sector = Non-Thrust, check if sectoral cap has headroom. If no headroom → decline or escalate to Board. Never exceed RBI-mandated or Board-approved sectoral ceilings.

---

### STEP 3 — Priority Sector Compliance Check

Track the bank's running PSL position before sanctioning. Key targets:

| Category | Mandate |
|---|---|
| Total Priority Sector | 40% of ANBC or CEOBE (whichever higher) |
| Total Agriculture | 18% of ANBC or CEOBE |
| Small & Marginal Farmers | 10% of ANBC (FY 2023-24) |
| Micro Enterprises | 7.5% of ANBC |
| Weaker Sections | 12% of ANBC (FY 2023-24) |
| Non-Corporate Farmers | Not below system-wide average (notified annually) |

If bank is running below target in any sub-category, **actively prioritize those proposals**. Shortfall results in RIDF/NABARD deposits at sub-market rates — a real cost to the bank.

Co-lending with NBFCs/HFCs for Priority Sector: permitted; governed by RBI FIDD circular dated 05.11.2020. Partner selection approved by MD & CEO.

---

### STEP 4 — Credit Information Report (CIR) Guardrails

**Mandatory CIR pull** (exceptions: own deposit loans, staff loans):

| Segment | Threshold for 1 CIC | Threshold for 2 CICs |
|---|---|---|
| Secured Personal / RAM / Corporate | Up to ₹50 lakh | Above ₹50 lakh |
| Personal Loans (Unsecured) | Up to ₹1 lakh | Above ₹1 lakh |
| Education Loans | Up to ₹4 lakh | Above ₹4 lakh |
| Other Personal Unsecured | Up to ₹5 lakh | Above ₹5 lakh |
| Gold Loans | Any amount — 1 CIC only | — |

**Score benchmarks**:
- Benchmark score: **700** (standard) / **650** (minimum with exception)
- Score 700–675: Zonal Head (GM/DGM) may approve
- Score 675–650: Vertical Head (GM) at Central Office must approve
- Score below 650: Generally reject unless exceptional circumstances
- Score = -1: New-to-Credit; process normally; no score-based delegation applies
- CRIF High Mark score relaxation NOT applicable

**Proprietorship/Partnership/Corporate**: Use Commercial CIR (without score); additionally pull Consumer CIR of Beneficial Owners to check delinquency patterns. Credit decision remains with sanctioning authority — CIR alone not sufficient ground for rejection.

**Staff lapse trigger**: Failing to pull CIR before sanction = documented staff lapse. Enforce strictly.

---

### STEP 5 — Appraisal Standards by Loan Type

#### Working Capital Assessment — Choose the Right Method:
| Method | When to Use |
|---|---|
| Turnover Method (Nayak Committee) | MSME/small borrowers; simpler assessment |
| MPBF (Modified Permissible Bank Finance) | Mid/large corporates; detailed current asset-liability analysis |
| Cash Budget Method | Seasonal businesses, project-based lending, exporters |

Key ratios to check: **Current Ratio** (minimum per policy), **Debt-Service Coverage Ratio (DSCR)** for term loans (industry-specific benchmarks — refer Financial/Project Benchmark Parameters section), **Debt-Equity Ratio**, **TOL/TNW**, **Net Worth adequacy**.

#### Term Loans:
- DSCR minimum benchmarks vary by industry — always apply industry-specific norms
- Repayment period must be commensurate with asset life and cash flow generation
- Moratorium period: Justified against project gestation; not to be used as loan restructuring tool
- TEV (Techno-Economic Viability) Study: Mandatory for large project loans; verify independently
- LIE (Lenders' Independent Engineer): Required for large infrastructure / project loans

#### Real Estate / CRE:
- CRE: Repayment primarily (>50%) from rental/sale proceeds → apply CRE norms; higher risk weight
- CRE-RH: Builder residential housing projects — DSCR not applicable; cash flow-based appraisal
- Land acquisition finance: Only to public agencies, NOT to private builders
- CRE-RH with commercial space: If commercial FSI > 10% of total FSI → classify as CRE, not CRE-RH

---

### STEP 6 — Concentration Risk & Exposure Limits

Think portfolio before approving any single transaction:

**Sectoral Concentration**: Monitor running totals for CRE, NBFCs, Capital Market, Infrastructure sectors. Breach of ceiling = mandatory Board approval or decline.

**Borrower/Group Exposure Limits**: Governed by Legal Exposure Framework (LEF) and RBI's Large Exposure Framework. Single borrower and group exposure ceilings are non-negotiable.

**NBFC Exposure**:
- NBFCs (non-MFI): Ceiling applies; review outstanding before fresh sanctions
- Co-lending with NBFC: Permitted under RBI guidelines; both banks maintain skin in the game
- NBFC-MFI on-lending: Only to RBI-recognized SRO members; per-borrower cap of ₹20 lakh

**Capital Market Lending**: Strict ceiling; loans to MFs, stocks as collateral — governed by specific RBI/SEBI guidelines. Not a thrust area.

**Intra-Group / Subsidiary Lending**: Board-approved policy; conflict of interest recusal mandatory for Directors connected to the borrowing entity.

**Unhedged Foreign Currency Exposure (UFCE)**: Mandatory reporting; incremental provisioning and capital charge apply as per RBI norms. Always compute UFCE before sanctioning forex loans or loans to exporters/importers.

---

### STEP 7 — Security & Collateral Framework

**Security perfection is non-negotiable — no disbursement without perfected security**:

- Mortgage: Registered mortgage preferred; equitable mortgage acceptable for specified cases with proper documentation
- Hypothecation: Stock and book debt statements on prescribed frequency; surprise inspections mandatory
- Pledge: Physical possession; proper valuation; insurance current
- Third-party guarantee: Check guarantor's net means (solvency certificate); CIR of guarantor mandatory

**Key rules**:
- No finance to private builders for **land acquisition** (only to public agencies)
- Personal guarantee of promoters/directors: Mandatory for SME/MSME exposures above threshold
- Property valuation: Independent empanelled valuer; re-valuation at policy-defined intervals
- Reasonableness of machinery cost: Verify against market rates before accepting as margin contribution

**Security Norms** vary by loan product — refer Security Norms chapter for product-specific minimums.

---

### STEP 8 — Delegation of Lending Powers

Every proposal must be matched to the correct sanctioning authority. **Exceeding delegated powers = void sanction, potential fraud risk**.

| Authority | Typical Scope |
|---|---|
| Branch Manager / Individual Officers | Small retail, MSME up to branch-level limits (CIC score-based graduation possible) |
| CPAC / BLCC (MCFB / CFB) | Branch-level credit committee for mid-range proposals |
| RLCC (Regional Level) | Regional Office committee for larger proposals |
| ZLCC (Zonal Level) | Zonal Office committee |
| HLCC-GM (Head Office – GM) | Large corporate, mid-upper range |
| HLCC-ED (Head Office – ED) | Very large corporate |
| CACB (Credit Approval Committee of Board) | Highest value; board-level |
| MCB (Management Committee of Board) | Absolute power to permit relaxations beyond delegated powers subject to RBI compliance |

**CIC Score-Based Delegation**: Score ≥ 700 → full delegated powers. Score 675–700 → Zonal Head minimum. Score 650–675 → Central Office Vertical Head. Only for consumer/individual segment.

**MD & CEO Special Powers**: Operational/administrative relaxations in Board-approved schemes on case-by-case basis; placed before Board for ratification.

---

### STEP 9 — Compliance, Regulatory & Governance Guardrails

**These are HARD STOPS — no business justification overrides them**:

| Guardrail | Rule |
|---|---|
| RBI Master Directions | Supersede all internal policy; implement immediately upon circular issuance |
| LEI (Legal Entity Identifier) | Mandatory for corporate borrowers above threshold; no LEI = no sanction |
| UDIN (Unique Document Identification Number) | All auditor-signed financial statements must have valid UDIN; verify before relying on financials |
| External Rating | Mandatory for large exposures; rating agency to be SEBI-registered (CRISIL, ICRA, CARE, BRICKWORK, INDIA RATINGS, ACUITÉ) |
| Fair Practices Code (FPC) | Transparent communication of loan terms; no hidden charges; borrower rights |
| KYC / AML | Mandatory for all borrowers; no exceptions |
| Holding Company Layers | Maximum layers as per Companies Act — RBI circular on holding company structures |
| Director Loans | Loans to Bank's own Directors / relatives: Board resolution; arms-length pricing; RBI guidelines strict |
| Current Account Opening | Follow RBI circular on CC/OD/Current Account discipline; no free credits in CC accounts |
| Third-Party Certificates | Independent due diligence mandatory; do not solely rely on borrower-submitted professional reports |
| Conflict of Interest | Directors/officers connected to borrower must recuse from approval discussions |

**Exception Management**: Any relaxation beyond normal policy parameters:
- Operational/administrative: MD & CEO can approve; placed before Board for information
- Major policy exceptions: MCB (Management Committee of Board) approval required
- RBI/Government mandated guidelines: Cannot be relaxed by anyone; immediate implementation

---

### STEP 10 — Monitoring, Review & Early Warning

**Credit does not end at sanction — the hardest work begins after disbursement**:

**Annual Review Discipline**:
- All credit limits: Mandatory annual review regardless of performance
- Stock/book debt statements: Prescribed frequency; non-submission = flag for inspection
- Audited financials: Mandatory for borrowers above ₹100 lakh (exception: crop loans per Board approval)
- DSCR monitoring: Quarterly/semi-annual for project loans

**Early Warning Signals (EWS)**:
- Frequent overdrawing in CC account
- Cheque returns / dishonour pattern
- Multiple CC accounts with different banks (Multiple Banking Arrangement — monitor for diversion)
- Delay in submission of financial statements
- Falling turnover or order book
- Adverse news in trade circles
- Account becoming NPA in other banks (check via CIR at renewal)
- UFCE spike without corresponding revenue hedge

**Consortium / Multiple Banking Arrangement (MBA)**:
- Exchange information with consortium banks formally and regularly
- Joint inspections: Mandatory for large accounts
- Pari-passu security sharing: Ensure documentation is current
- Lone wolf sanctioning outside consortium: Flag immediately

**Takeover of Accounts**: Enhanced due diligence mandatory. Check reason for transfer; obtain NOC; verify that account is not stressed/evergreened at previous bank. Follow takeover policy guardrails strictly.

---

## Key Policy Guardrails Reference Card

| Domain | Guardrail |
|---|---|
| Women Borrower | Must be sole or joint applicant; property in her name (sole or joint) |
| Startup Lending | ≤10 years, ≤₹100 Cr turnover, DIPP recognized; up to ₹50 Cr PSL eligible |
| Digital Lending | Only through RBI-regulated LSPs; Master Agreement mandatory; RBI Aug 2022 framework applies |
| Forex Loans | UFCE computation mandatory; hedging encouragement policy |
| Infrastructure InvITs | Specific exposure norms; Board approval for new categories |
| IBPC | Governed by RBI circular; tenor and risk transfer rules apply |
| PCE (Partial Credit Enhancement) | Only for NBFC/HFC bonds; specific norms apply |
| Off-Balance Sheet | Included in LEF; credit equivalent computed per RBI norms |
| Lease Rental Discounting | Specific appraisal norms; lock-in period of lease must cover loan tenor |
| Bills Discounting | Documentary evidence mandatory; no accommodation bills |
| Loan Refinancing (Tenor Extension) | IBA Report guidelines; not to be used as disguised restructuring |

---

## Output Templates for Common Tasks

### Template A: Policy Eligibility Check
```
CREDIT POLICY ELIGIBILITY ASSESSMENT

Borrower: [Name / Entity Type]
Proposed Facility: [Type] [Amount]
Sector: [Sector Classification]

1. CLASSIFICATION: [Borrower Category / Corporate Tier]
2. SECTOR STATUS: [Thrust / Non-Thrust / Priority Sector Sub-Category]
3. PSL ELIGIBILITY: [Yes/No + Sub-category if Yes]
4. CIR REQUIREMENT: [CICs / Score Benchmark]
5. DELEGATION LEVEL: [Authority required to sanction]
6. KEY PARAMETERS TO VERIFY: [DSCR / CR / DER / Security / LEI / UDIN]
7. REGULATORY COMPLIANCE CHECKS: [List applicable RBI circulars]
8. CONCENTRATION RISK FLAG: [Red / Amber / Green + reason]
9. RECOMMENDATION: [Proceed / Decline / Escalate + reason]
```

### Template B: Sector Exposure Limit Check
```
SECTORAL EXPOSURE STATUS

Sector: [Sector Name]
Sector Classification: [Thrust / Non-Thrust / Restricted]
Board-approved ceiling (FY ___): ₹ ___ Cr / ___% of total advances
Current running exposure: ₹ ___ Cr / ___% 
Proposed addition: ₹ ___ Cr
Post-sanction exposure: ₹ ___ Cr / ___%
Headroom available: [Yes / No / Marginal]
Action required: [Proceed / Escalate to Board / Decline]
```

### Template C: Policy Exception Note
```
POLICY EXCEPTION REQUEST

Proposal Reference: ___
Parameter for which relaxation sought: ___
Standard policy requirement: ___
Proposed relaxation: ___
Business justification: ___
Risk mitigation proposed: ___
Sanctioning authority required for exception: ___
Board ratification required: [Yes / No]
CPO Recommendation: [Approve / Decline exception]
```

---

## Frequently Invoked Policy Logic

**Q: Can we lend to a partnership firm where one partner is an HUF?**
→ No. HUFs cannot legally enter into partnership. Reject.

**Q: Can we finance land acquisition for a private builder?**
→ No. Land acquisition financing: Public agencies only. Private builders → Reject.

**Q: CIR score is 665 — can branch sanction?**
→ No. Score 675–650 requires Central Office Vertical Head (GM) minimum. Branch cannot sanction; escalate.

**Q: New borrower with CIBIL score -1 (New-to-Credit). Proceed?**
→ Yes, but only under normal (non-score-based) delegation. Enhanced due diligence. Document NTC status.

**Q: CRE commercial area is 12% of total FSI in a predominantly residential project. Classify as CRE-RH?**
→ No. Commercial FSI exceeds 10% ceiling. Must be classified as CRE (not CRE-RH). Apply CRE norms and risk weight.

**Q: Borrower wants to avail CC limit but also has OD with another bank. Flag?**
→ Yes. Multiple Banking Arrangement — verify no diversion; joint monitoring required; inform Lead Bank.

**Q: MD & CEO wants to override a policy parameter for a large borrower without Board approval?**
→ Permissible only for operational/administrative matters in Board-approved schemes. Must be placed before Board for ratification. If it is a fundamental credit policy parameter — escalate to MCB, not MD & CEO unilaterally.

---

## How to Use This Skill

1. **Read the full request carefully** — identify whether it is transaction-level, portfolio-level, or policy-drafting.
2. **Run through all 10 Steps** in the Thinking Framework mentally before drafting output.
3. **Surface hard stops first** — compliance failures, HARD STOP guardrails, and regulatory violations must be flagged before any business recommendation.
4. **Use the appropriate Output Template** for structured response.
5. **Always cite the relevant policy section or RBI circular** where a guardrail is invoked.
6. **When in doubt, escalate** — a conservative credit culture is the first line of defense against NPA buildup.
7. **Balance is the goal** — the policy exists to enable good credit, not to kill business. For every "No," provide the conditions under which a "Yes" is possible.

---

*This skill is modeled on a Board-approved Master Credit Policy of a scheduled commercial bank in India, governed by RBI guidelines, BASEL-III norms, and IBA best practices. It should be updated annually in sync with RBI circulars, budget changes, and Board-approved revisions.*
