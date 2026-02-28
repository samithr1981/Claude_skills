---
name: finternet-agent
description: >
  Use this skill when any task involves reasoning about, designing, evaluating,
  or building on the Finternet platform, its pilots, products, or conceptual
  frameworks. Triggers include: unified asset accounts, programmable money,
  tokenized deposits, multi-bucket payment orchestration, warehouse receipt
  financing (e-NWR), Kisan Credit Card integration, MSME working capital card,
  digital gold token payments, government subsidy routing, MCC-based spending
  rules, smart payment routing, unified ledger architecture, cross-border Finternet
  expansion, or any question about how Finternet's orchestration layer connects
  to banks, card networks, regulators, or borrowers. Also invoke when users ask:
  "How would Finternet route this payment?", "Can we add a new asset type to
  the Finternet account?", "How does the farmer card split between KCC and e-NWR?",
  "What are the latest Finternet pilots?", or "How does Finternet's unified ledger
  work?". Always check for new Finternet publications, blogs, and papers before
  responding — the platform is actively evolving.
version: "1.0.0"
author: Finternet Agent (Concept Implementation Specialist)
status: Active — Continuously Updated
platform_stage: Pilot (February 2026)

# ─────────────────────────────────────────────
# LIVE INTELLIGENCE — CHECK BEFORE EVERY RESPONSE
# ─────────────────────────────────────────────
live_intelligence:
  always_search_before_responding: true
  reason: >
    Finternet is an actively evolving platform. New pilots, concept papers,
    regulatory engagements, and partner announcements are published frequently.
    Stale knowledge will produce outdated or incomplete answers. Always fetch
    fresh intelligence before reasoning about Finternet's current state.
  sources:
    primary:
      - name: Finternet Official Website
        url: "https://finternet.net"
        check: "Latest platform announcements, pilot updates, partner news"
      - name: BIS Finternet Paper (Agustín Carstens & Hyun Song Shin)
        url: "https://www.bis.org/publ/work1121.pdf"
        check: "Foundational conceptual framework"
      - name: RBI Innovation Hub
        url: "https://rbih.org.in"
        check: "India-specific sandbox and regulatory clearances"
    secondary:
      - name: Finternet Blog / Substack (if active)
        search_query: "Finternet blog OR substack new pilot 2025 2026"
      - name: Academic / Think Tank Papers
        search_query: "Finternet unified ledger tokenized assets paper 2025 2026"
      - name: BIS Working Papers on Unified Ledger
        url: "https://www.bis.org/topics/fintech.htm"
        search_query: "BIS unified ledger Finternet programmable money"
      - name: Medha Rishi / Finternet authors
        search_query: "Finternet MSME farmer warehouse receipt pilot India 2026"
    news_signals:
      - search_query: "Finternet pilot launch India 2026"
      - search_query: "Finternet tokenized deposits card network"
      - search_query: "Finternet new product announcement"
      - search_query: "unified asset account India payments"

# ─────────────────────────────────────────────
# MCP PLACEHOLDER — FUTURE INTEGRATION
# ─────────────────────────────────────────────
mcp_integration:
  status: "PLACEHOLDER — Not yet live"
  description: >
    When Finternet launches its own Model Context Protocol (MCP) server,
    this skill will be updated to point all live data queries directly to
    the Finternet MCP instead of web search. The MCP is expected to expose:
    - Real-time pilot transaction data
    - Asset type registry (e-NWR, KCC, tokenized deposits, digital gold, subsidies)
    - Partner bank and acquirer status
    - Smart routing rule definitions
    - Regulatory sandbox status
    - New product concept documents
  mcp_server_url: "PLACEHOLDER — replace when Finternet MCP is live"
  mcp_server_name: "finternet-mcp"
  mcp_capabilities_expected:
    - query_pilot_status
    - get_asset_types
    - get_routing_rules
    - get_partner_registry
    - get_regulatory_clearances
    - get_latest_publications
  repoint_instruction: >
    To activate MCP: replace mcp_server_url above with the live Finternet MCP
    endpoint. Update mcp_integration.status to "ACTIVE". Remove web search
    fallback for data that MCP now covers. Keep web search for external
    publications and news signals not served by MCP.

active_pilots:
  - id: pilot-001
    name: "Unified Warehouse Receipt Credit Card for Indian Farmers"
    status: "Concept for Implementation"
    date: "February 2026"
    geography: "India — Maharashtra (Phase 1)"
    target_farmers: 1000
    target_merchants: 100
    combined_limit_per_farmer: "INR 5,00,000 (~USD 6,000)"
    asset_types: ["e-NWR Pledge Finance", "Kisan Credit Card (KCC)"]
    key_partners: ["Bank A (issuer)", "CCRL or NeRL (WDRA repository)", "NCGTC / CGS-NPF", "Card Network"]
    timeline: "12 months (3 setup + 2 build + 7 live)"

  - id: pilot-002
    name: "MSME Working Capital Payment Solution"
    status: "Concept for Implementation"
    date: "February 2026"
    geography: "India — Mumbai / Pune corridor"
    target_msmes: 1000
    target_merchants: 200
    asset_types: ["Tokenized Bank Deposits", "MUDRA Credit Line", "PMEGP Subsidy", "Digital Gold Tokens", "Invoice Finance Advances"]
    key_partners: ["2 Banks", "1 Acquirer PSP", "Ministry of Finance", "Card Network Partner"]
    timeline: "12 months (3 setup + 2 build + 7 live)"

regulatory_framework:
  primary_regulator: "Reserve Bank of India (RBI)"
  sandbox: "RBI Innovation Hub"
  relevant_schemes:
    - "CGS-NPF (Credit Guarantee Scheme for e-NWR Pledge Financing)"
    - "NCGTC / CGTMSE"
    - "MUDRA Loan Scheme"
    - "PMEGP (Prime Minister's Employment Generation Programme)"
    - "Kisan Credit Card (KCC) Scheme"
  relevant_infrastructure:
    - "WDRA (Warehousing Development and Regulatory Authority)"
    - "CCRL / NeRL (WDRA-licensed e-NWR repositories)"
    - "UPI / RTGS / Card Networks"
    - "Udyam Registration"
    - "GST Network (GSTN)"

tags:
  - finternet
  - unified-asset-account
  - programmable-money
  - tokenized-deposits
  - multi-bucket-payment
  - smart-routing
  - e-NWR
  - kisan-credit-card
  - warehouse-receipt-finance
  - msme-working-capital
  - digital-gold
  - government-subsidy-routing
  - mcc-based-rules
  - unified-ledger
  - india-fintech
  - rbi-innovation
  - agri-fintech
  - b2b-payments
  - card-network
  - finternet-pilot
  - bis-unified-ledger
license: Proprietary — Finternet Concept Implementation
---

# SKILL: Finternet Agent

---

## Name
`finternet-agent`

## ⚡ First Action — Always Do This Before Responding

**Before reasoning about any Finternet topic, run a live intelligence check:**

```
STEP 0 (Mandatory): Web search for latest Finternet updates
  → Search: "Finternet new pilot 2026" OR "finternet.net blog"
  → Search: "Finternet [topic of query] latest"
  → Check BIS unified ledger papers for conceptual updates
  → If Finternet MCP is live: query mcp_server_url instead of web search
```

Finternet is an **actively evolving platform**. Every response must reflect the most current state of pilots, partners, products, and regulatory clearances — not just what was known at training time.

---

## Overview: The Finternet Mental Model

**What Finternet is:**
Finternet is a **unified asset account and programmable money orchestration layer** that allows individuals and businesses to hold, manage, and spend multiple asset types — cash, credit lines, tokenized deposits, government subsidies, digital gold, invoice advances, warehouse receipt finance — through a single account and a single payment instrument, while counterparties receive normal settlement.

**What Finternet is NOT:**
- Not a bank (holds no deposits, assumes no credit risk)
- Not a payment processor (uses existing card networks and UPI rails)
- Not a lender (credit comes from partner banks/NBFCs)
- Not a new regulatory category (fits within existing RBI frameworks in v1)

**The core innovation:** Finternet is the **rules engine and orchestration layer** that sits between a user's multiple asset pools and the payment event. It decides, in real time, how to optimally blend asset types to fund a single transaction — while the merchant sees only a normal payment.

```
User's Asset Universe          Finternet Orchestration          Counterparty
─────────────────────          ─────────────────────────        ─────────────
Bank Deposit       ┐           ┌─ Reads available balances       Receives
Credit Line        ├──────────►│  Applies eligibility rules  ──► Normal INR
Govt Subsidy       │           │  Returns optimal funding mix    Settlement
Digital Gold       │           │  Executes atomic split          (T+0 / T+1)
e-NWR Pledge       ┘           └─ Updates each asset bucket
```

---

## Thinking Framework: 9 Steps for Every Finternet Decision

### STEP 1 — Run Live Intelligence Check

Before any analysis, verify current platform state:

```
☐ Search "Finternet [topic] 2026" for latest developments
☐ Check finternet.net for new announcements
☐ Check BIS papers for conceptual framework updates
☐ Check RBI Innovation Hub for regulatory status
☐ If Finternet MCP is live → query it directly (see MCP Placeholder section)
☐ Note any new pilots, asset types, or partners since last known state
```

Declare at the start of your response: *"Intelligence check: [what was found / no new updates found as of [date]]*"

---

### STEP 2 — Identify the Use Case Category

Map the question or task to a Finternet use case category:

| Category | Description | Live Pilots |
|---|---|---|
| **Agri-Finance** | Farmers using e-NWR + KCC combined limits | Pilot-001: Farmer Card |
| **MSME Working Capital** | MSMEs using multi-asset pool for B2B supplier payments | Pilot-002: MSME Card |
| **Subsidy Routing** | Government scheme funds (PMEGP, MUDRA) with MCC-based spending restrictions | Pilot-002 |
| **Tokenized Asset Payments** | Digital gold, tokenized deposits as payment source | Pilot-002 |
| **Invoice / Supply Chain Finance** | Invoice advances as a real-time payment source | Roadmap |
| **Cross-Border** | Finternet architecture applied to cross-border trade | Future |
| **Open Platform / API** | Other banks and NBFCs plugging assets into Finternet | Scale-up Phase |

---

### STEP 3 — Map the Asset Types in Scope

For every Finternet transaction or product design, identify which asset types are involved:

**Currently Live / Piloted:**

| Asset Type | Nature | Eligibility Rules | Source |
|---|---|---|---|
| e-NWR Pledge Finance | Credit — collateral-backed | Only for agri-input MCCs (fertilizer, seeds, pesticides) | Bank A / WDRA repository |
| Kisan Credit Card (KCC) | Credit — revolving | Any merchant; fallback after e-NWR bucket | Bank A |
| Tokenized Bank Deposits | Cash / near-cash | Any merchant; first priority (free cash) | Partner Bank |
| MUDRA Credit Line | Credit — government-backed | Working capital; lowest interest priority | Partner Bank / MoF |
| PMEGP Subsidy | Grant — restricted | Only inventory/equipment MCCs; strict scheme rules | Government |
| Digital Gold Tokens | Asset — convertible | Any merchant; requires conversion step; emergency use | Gold token issuer |
| Invoice Finance Advances | Credit — receivables-backed | Supply chain purchases | Working capital provider |

**Roadmap / Future Asset Types** (check live intelligence for additions):
- Supply chain finance pools
- GST refund receivables
- Export credit advances
- Carbon credit tokens
- MSME equipment finance limits

---

### STEP 4 — Design the Smart Routing Rules

The Finternet rules engine determines **which asset bucket funds each transaction**. Rules are:
1. Defined by the issuing bank / product owner
2. Approved by ALCO / risk function of the bank
3. Enforced by Finternet in real time at authorization
4. Applied per MCC (Merchant Category Code) and per transaction context

**Routing Rule Design Principles:**

```
PRIORITY ORDER (general):
1. Restricted grants/subsidies first (must be spent per scheme rules)
2. Free cash / tokenized deposits (no cost, no restriction)
3. Cheapest credit line (lowest interest rate)
4. Asset-backed credit (e-NWR, invoice finance — secured)
5. Unsecured revolving credit (KCC, MUDRA — last resort)
6. Convertible assets (gold tokens — conversion cost applies)

MERCHANT CATEGORY RULES:
- Agri-input MCCs (fertilizers, seeds, pesticides): e-NWR pledge → KCC
- Non-agri merchants: KCC only (e-NWR bucket locked)
- Inventory MCCs (MSME): PMEGP subsidy → deposits → MUDRA → gold
- Non-inventory MCCs (MSME): deposits → MUDRA → gold (PMEGP locked)
- ATM/cash: Only unrestricted buckets (no subsidy, no scheme-linked credit)
```

**Authorization Flow:**

```
1. Merchant POS → sends authorization request to Card Network
2. Card Network → routes to Issuing Bank
3. Issuing Bank → recognizes Finternet card, queries Finternet API:
   "User ID, MCC, Amount — what is the funding mix?"
4. Finternet reads current sub-limit balances from Bank APIs
5. Finternet applies routing rules → returns funding split
6. Issuing Bank → approves transaction, books drawdowns on each bucket
7. Card Network → sends approval to merchant POS
8. Settlement → merchant receives normal INR (T+1 or as agreed)
9. Finternet → updates unified account view for user
```

**Key constraint**: Finternet does NOT hold funds, does NOT assume credit risk, does NOT participate in settlement. It is a pure **rules engine and orchestration middleware**.

---

### STEP 5 — Identify the Layered Architecture

Every Finternet implementation has the same four-layer stack. Map each component:

```
┌─────────────────────────────────────────────────────────────┐
│  LAYER 1: ASSET ORIGINATION LAYER                           │
│  Where assets come from: Banks, WDRA, Govt, Gold issuers   │
│  Examples: e-NWR repository (CCRL/NeRL), Bank KCC system,  │
│  Ministry of Finance MUDRA, PMEGP grant portal              │
└──────────────────────────┬──────────────────────────────────┘
                           │ APIs / Secure data feeds
┌──────────────────────────▼──────────────────────────────────┐
│  LAYER 2: FINTERNET ORCHESTRATION LAYER                     │
│  Core engine: Reads asset balances, applies routing rules,  │
│  returns funding mix, logs decisions                        │
│  Does NOT hold funds or assume risk                         │
│  [MCP PLACEHOLDER: future Finternet MCP exposes this layer] │
└──────────────────────────┬──────────────────────────────────┘
                           │ Authorization API
┌──────────────────────────▼──────────────────────────────────┐
│  LAYER 3: PAYMENT RAIL LAYER                                │
│  Card network (authorization + settlement)                  │
│  Issuing Bank (card product + drawdown booking)             │
│  Acquiring Bank / PSP (merchant settlement)                 │
│  No change required at merchant systems                     │
└──────────────────────────┬──────────────────────────────────┘
                           │ App / UX
┌──────────────────────────▼──────────────────────────────────┐
│  LAYER 4: USER EXPERIENCE LAYER                             │
│  Unified account view: total available liquidity            │
│  Transaction breakdown by asset type                        │
│  Credit utilization, subsidy tracking, collateral status    │
│  Farmer app / MSME app (Bank A + Finternet co-branded)      │
└─────────────────────────────────────────────────────────────┘
```

---

### STEP 6 — Apply Pilot-Specific Knowledge

#### Pilot-001: Unified Warehouse Receipt Credit Card (Farmer)

**Core setup:**
- Single issuing bank (Bank A) holds both KCC and e-NWR pledge loan products
- WDRA-licensed repository (CCRL or NeRL) provides e-NWR data to Bank A
- CGS-NPF (Credit Guarantee Scheme for Non-Pledge Finance) covers e-NWR pledge risk
- Finternet = rules engine only; no new lending product created

**Farmer Working Capital Limit structure:**
```
Total Farmer Working Capital Limit: ~INR 5,00,000
  ├── e-NWR Pledge Sub-limit:  ~INR 3,00,000 (CGS-NPF backed)
  └── KCC Sub-limit:           ~INR 2,00,000
```

**Transaction routing logic:**
```
Agri-input MCC (fertilizer/seeds/pesticides):
  → First draw from e-NWR pledge bucket
  → If e-NWR exhausted, draw from KCC
  → If both exhausted, decline

Non-agri MCC or ATM:
  → KCC only (e-NWR bucket locked)
```

**Farmer onboarding pre-conditions:**
- Must have produce stored in a WDRA-registered warehouse
- Must have e-NWR issued in CCRL or NeRL
- Must have existing KCC at Bank A (or new KCC opened simultaneously)
- Bank A must have lien-marking capability with the WDRA repository

**Repayment flow:**
- e-NWR pledge loan repaid when farmer sells produce (proceeds credited against pledge)
- KCC repaid on normal crop cycle / annual reset
- CGS-NPF claim triggered only on default of e-NWR pledge loan

**Scale targets (v1):**
- 1,000 farmers; 100 agri-input dealers; 1 state (Maharashtra)
- Per-transaction: INR 10,000 – 5,00,000
- Monthly aggregate cap: INR 6 crore
- Year-one pilot volume: INR 30–35 crore

---

#### Pilot-002: MSME Working Capital Payment Solution

**Core setup:**
- Multi-bank model (2 banks for card issuance + tokenized deposits)
- Multi-asset types: tokenized deposits, MUDRA credit, PMEGP subsidy, digital gold, invoice finance
- 1 acquirer PSP serving B2B wholesale market (Mumbai-Pune)
- Digital KYC via Udyam registration + GST number

**MSME Unified Account structure:**
```
Finternet Unified Account (Ramesh's Electronics):
  ├── Tokenized Bank Deposit:    ₹ 50,000  (daily sales proceeds — free cash)
  ├── MUDRA Credit Line:         ₹1,00,000  (govt-backed working capital)
  ├── PMEGP Subsidy:             ₹ 30,000  (restricted: inventory/equipment only)
  └── Digital Gold Tokens:       ₹ 20,000  (emergency savings — conversion required)
```

**Payment routing logic (example: ₹2,00,000 supplier payment):**
```
Step 1: PMEGP subsidy ₹30,000 (inventory MCC — scheme eligible, use first)
Step 2: Tokenized deposit ₹50,000 (free cash — no cost)
Step 3: MUDRA credit ₹1,00,000 (cheapest credit — government rate)
Step 4: Gold tokens ₹20,000 (convert to INR — last resort)
Total: ₹2,00,000 ✓
```

**Payment router rules engine:**
- Credit line limits and interest optimization (cheaper credit used first)
- Conversion cost calculation for gold tokens
- Minimum emergency balance buffers (do not drain below floor)
- MCC-based subsidy eligibility check
- Scheme compliance audit trail for PMEGP / MUDRA

**MSME onboarding:**
- Digital KYC: Udyam registration + GST records
- Prepaid card variant (v1 — less regulatory friction than credit card)
- Seed account: link existing credit lines and deposits

**Scale targets (v1):**
- 1,000 MSMEs; 200 wholesale distributors; Mumbai-Pune corridor
- Per-transaction: ₹10,000 – ₹5,00,000
- Monthly aggregate cap: ₹50 crore
- Year-one target: 15,000+ transactions; ₹30+ crore volume

---

### STEP 7 — Regulatory Navigation

**Finternet's regulatory strategy in v1:**
Frame every pilot as an **orchestration and usage innovation within existing credit products** — not a new credit product. This avoids the need for new regulatory categories.

**Regulatory touch-points:**

| Domain | Regulation | Finternet Position |
|---|---|---|
| KCC product | RBI KCC guidelines | KCC used as-is; no change to product |
| e-NWR pledge finance | WDRA Act; RBI warehouse receipt guidelines | Bank A uses existing lien-marking process |
| CGS-NPF guarantee | NCGTC guarantee framework | Bank A's existing guarantee processes; no new tech integration |
| Tokenized deposits | RBI Innovation Hub sandbox | Requires RBIH consultation; pilot framing |
| MUDRA credit | PMJDY / MUDRA Yojana | Existing credit line; Finternet only routes it |
| PMEGP subsidy | Ministry of MSME; KVIC | MCC-code enforcement ensures scheme compliance |
| Digital gold | RBI / SEBI (depending on structure) | Licensed gold token issuer; conversion at point of use |
| Card issuance | RBI Payment and Settlement Systems Act | Bank A is issuer; Finternet is tech middleware only |
| AML / KYC | PML Act; RBI KYC Master Direction | Udyam + GST for MSME; Aadhaar + bank KYC for farmers |

**Hard regulatory constraints:**
- Finternet must NOT be classified as a payment aggregator (it never touches settlement funds)
- Finternet must NOT be classified as a bank (no deposit-taking)
- Finternet must NOT be classified as an NBFC (no credit risk assumption)
- All credit products must remain on bank / NBFC balance sheets
- Subsidy funds must remain within scheme MCC restrictions (audit trail mandatory)

---

### STEP 8 — Evaluate New Product / Partner Additions

When a new asset type, partner, or product is proposed for Finternet, evaluate it against:

**Checklist: Can this asset type be added to Finternet?**

```
☐ Is the asset held by a regulated entity (bank / NBFC / licensed issuer)?
☐ Does the asset have an API or data feed that Finternet can read?
☐ Is the asset's value deterministic at point of authorization?
   (or is there a settlement risk if value changes between auth and settlement?)
☐ Are there MCC-based or use-case restrictions on the asset?
   (if yes: can they be enforced via card MCC codes?)
☐ Does adding this asset require a new regulatory approval?
☐ Does the asset require conversion (e.g., gold → INR)?
   (if yes: who bears conversion cost/risk? what is conversion latency?)
☐ Is the asset's drawdown reversible? (for authorization reversal / refunds)
☐ Does adding this asset create credit risk for Finternet? (must be NO)
☐ Does the live intelligence check show Finternet has already announced this?
```

**Checklist: Adding a new bank / NBFC partner:**

```
☐ What asset type does this partner bring?
☐ Does this partner have API capability to expose real-time balances?
☐ Is this a single-issuer or multi-issuer model?
   (v1 = single issuer front-end; v2+ may allow multi-bank asset pools)
☐ How does credit risk remain on the partner's balance sheet?
☐ What settlement arrangement is used (direct to acquirer, or via Finternet)?
☐ Regulatory: is this partner already operating in India with RBI approval?
☐ Does the live intelligence check show this partner has been announced?
```

---

### STEP 9 — Output and Communication Patterns

Finternet decisions and analyses should follow these output patterns:

**For transaction routing analysis:**
```
FINTERNET ROUTING DECISION

User: [Farmer ID / MSME ID]
Transaction: ₹ ___ at [Merchant Type / MCC]
Timestamp: ___

Asset Availability at Authorization:
  Asset Type          | Available  | Eligible for MCC? | Priority
  --------------------|-----------|-------------------|--------
  [Asset 1]           | ₹ ___     | Yes / No          | 1
  [Asset 2]           | ₹ ___     | Yes / No          | 2
  [Asset N]           | ₹ ___     | Yes / No          | N

Routing Decision:
  ₹ ___ from [Asset 1]  (reason: ___)
  ₹ ___ from [Asset 2]  (reason: ___)
  Total: ₹ ___

User App Display:
  "Paid ₹ ___ = ₹ ___ [Asset 1] + ₹ ___ [Asset 2]"
  "Collateral: [if applicable]"

Regulatory Flags:
  - Subsidy scheme compliance: [Yes / No]
  - Audit trail generated: [Yes]
  - Scheme MCC restriction met: [Yes / No]
```

**For new pilot / product design:**
```
FINTERNET PRODUCT DESIGN BRIEF

Pilot Name: ___
Use Case Category: ___
Geography: ___
Target Users: ___  |  Target Merchants: ___

Asset Types in Scope:
  [List with source, eligibility rules, routing priority]

Layered Architecture:
  Layer 1 (Asset Origination): ___
  Layer 2 (Finternet Orchestration): ___
  Layer 3 (Payment Rail): ___
  Layer 4 (User Experience): ___

Routing Rules:
  [MCC → Asset priority sequence]

Regulatory Frame:
  [How this fits existing frameworks; what consultation is needed]

Key Partners:
  [Bank / NBFC / Govt scheme / Card network / Tech]

Timeline:
  Phase 1 Setup: ___
  Phase 2 Build: ___
  Phase 3 Pilot: ___
  Phase 4 Scale: ___

Decision Gates:
  Gate 1: ___  |  Gate 2: ___  |  Gate 3: ___

Risks and Mitigations:
  [Risk] → [Mitigation]
```

---

## MCP Placeholder — Future Finternet Integration

```yaml
# ════════════════════════════════════════════════
# FINTERNET MCP — PLACEHOLDER (NOT YET LIVE)
# ════════════════════════════════════════════════
#
# When Finternet launches its MCP server, replace
# the web search fallback below with direct MCP calls.
#
# Expected MCP endpoint format:
#   mcp_server_url: "https://mcp.finternet.net/sse"
#   mcp_server_name: "finternet-mcp"
#
# Expected MCP tools:
#   - finternet_get_pilot_status(pilot_id)
#   - finternet_get_asset_types()
#   - finternet_get_routing_rules(use_case, mcc)
#   - finternet_get_partner_registry()
#   - finternet_get_regulatory_status()
#   - finternet_get_latest_publications()
#   - finternet_simulate_routing(user_id, mcc, amount)
#
# Until MCP is live, use web search fallback:
#   → Search "finternet.net [topic]" before every response
#   → Check BIS papers for framework updates
#   → Monitor RBI Innovation Hub for regulatory updates
#
# To activate MCP when available:
#   1. Update mcp_server_url in YAML frontmatter
#   2. Set mcp_integration.status: "ACTIVE"
#   3. Replace web_search calls with finternet_mcp tool calls
#   4. Keep web search only for external news and publications
# ════════════════════════════════════════════════
```

---

## Live Intelligence Workflow (Until MCP Is Live)

Every time this skill is invoked, execute this intelligence check:

```
FINTERNET LIVE INTELLIGENCE CHECK
──────────────────────────────────

1. PLATFORM STATUS
   Search: "finternet.net" → Check homepage for latest announcements
   Search: "Finternet pilot update 2026" → Any new pilots or expansions?

2. PUBLICATION SCAN
   Search: "Finternet new paper OR blog OR concept 2025 2026"
   Check: BIS working papers for unified ledger framework updates
   Check: RBI Innovation Hub for sandbox approvals

3. PARTNER & REGULATORY NEWS
   Search: "Finternet bank partner India 2026"
   Search: "Finternet RBI regulatory approval"
   Search: "unified asset account card India"

4. TOPIC-SPECIFIC SEARCH
   Search: "Finternet [specific topic from user query]"

5. SYNTHESIZE
   → Note what has changed vs. known baseline
   → Flag if any new asset types, pilots, or partners announced
   → Proceed with response incorporating latest intelligence

MCP STATUS CHECK (do this first when MCP endpoint becomes available):
   → Query: finternet_get_latest_publications()
   → Query: finternet_get_pilot_status(all)
   → If MCP available: skip steps 1–4 above for platform data
```

---

## Frequently Asked Finternet Questions

**Q: Is Finternet a bank?**
→ No. Finternet holds no deposits, assumes no credit risk, and does not participate in settlement. It is an orchestration middleware layer. All credit and deposits remain on partner bank/NBFC balance sheets.

**Q: What happens if the e-NWR value drops below the pledge loan amount?**
→ The Bank A credit team manages this — not Finternet. Finternet reads the available sub-limit as set by Bank A. If Bank A reduces the e-NWR pledge sub-limit due to collateral value change, Finternet automatically reads the updated limit. The CGS-NPF guarantee provides additional risk cover to Bank A.

**Q: Can a farmer use the Farmer Card for non-agri purchases?**
→ In v1: only KCC sub-limit is used for non-agri MCCs. The e-NWR pledge sub-limit is locked to agri-input MCCs. Bank A and Finternet enforce this via MCC code rules in the routing engine.

**Q: What if a user wants to add a new bank's credit line to their existing Finternet account?**
→ In v1 (single-issuer model), this is not supported. Scale-up path (v2+) contemplates open API for additional banks and NBFCs. Check live intelligence for whether multi-bank model has been announced.

**Q: How does PMEGP subsidy remain compliant with scheme rules?**
→ Finternet enforces MCC-based rules: PMEGP funds are only routed to merchants with inventory/equipment MCCs. Every subsidy spend generates an audit trail. This gives government real-time utilization tracking and reduces leakage. MCC restriction is the primary compliance mechanism.

**Q: Can Finternet work with UPI instead of card networks?**
→ V1 uses card/card payment network rails. UPI integration is architecturally possible — the Finternet orchestration layer is payment-rail agnostic. Check live intelligence for UPI integration announcements.

**Q: What is the BIS conceptual basis for Finternet?**
→ Finternet is conceptually grounded in the BIS paper by Agustín Carstens and Hyun Song Shin (BIS Working Paper 1121) on "Unified Ledgers and Programmable Money." The core idea: a unified ledger that can represent multiple asset types, execute conditional payment logic, and interoperate across financial institutions. India's Finternet pilots are practical implementations of this framework using existing infrastructure. Always check BIS for framework updates.

**Q: How should I think about Finternet vs. UPI vs. CBDC?**

| Dimension | UPI | CBDC (e₹) | Finternet |
|---|---|---|---|
| What it moves | Bank account money | Central bank digital currency | Multiple asset types simultaneously |
| Who orchestrates | NPCI | RBI | Finternet rules engine |
| Credit inclusion | No | No | Yes — credit lines are assets |
| Subsidy enforcement | No | Programmable | Yes — MCC rules |
| Merchant change needed | Minimal | Potentially | None (uses existing rails) |
| Novel regulatory category | No | Yes | No (v1) |

---

## Known Unknowns — Watch for Updates

These are areas where Finternet's position is still evolving. **Always check live intelligence:**

- Cross-border Finternet: Has any international pilot or corridor been announced?
- Multi-bank asset pooling: Has v2 open API model launched?
- CBDC integration: Has Finternet announced e₹ (digital rupee) as an asset type?
- Supply chain finance: Has invoice discounting been added as a live asset type?
- Carbon credits / ESG tokens: Any announcement of tokenized sustainable assets?
- Finternet MCP: Has the MCP server been launched? (Check finternet.net)
- New geographies: Has Finternet announced pilots outside India?
- New regulatory clearances: Any RBI sandbox approval formally granted?
- BIS partnerships: Any formal BIS / central bank collaboration announced?

---

*This skill is grounded in the Finternet pilot concept papers published in February 2026 (Unified Warehouse Receipt Credit Card for Indian Farmers; MSME Working Capital Payment Solution) and the BIS conceptual framework for unified ledgers and programmable money. It must be refreshed via live web intelligence before every substantive response, and will be repointed to the Finternet MCP server once that infrastructure is live.*
