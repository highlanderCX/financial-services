# Returns Analysis — Growth Equity Secondaries

description: Build IRR / MOIC sensitivity tables for minority pre-IPO secondary investments held in SPC / SPV vehicles. Models returns across entry valuation, hold period, exit scenario (IPO / M&A / secondary block), entry discount, and fee load. Excludes LBO mechanics (leverage, debt paydown, EBITDA bridges) — designed for unlevered growth-equity returns to LPs net of vehicle fees. Use when sizing up a late-stage secondary or primary opportunity, stress-testing exit assumptions, or preparing returns exhibits for IC or LP materials. Triggers on "returns analysis", "IRR sensitivity", "MOIC table", "what's the return at", "model the returns", "back of the envelope", or "secondary returns".

## Workflow

### Step 1: Gather Deal Inputs

Ask for (or extract from prior screening / DD work):

**Entry**
- Implied post-money valuation at entry ($M)
- Discount (if any) to last primary round
- Share class purchased (common / preferred series — note any liquidation preference)
- Tranche size / equity invested at the SPC level
- Transaction costs (legal, broker fee, transfer fee — typically 1-3% of tranche)

**Operating assumptions** (drives exit valuation)
- Current ARR / revenue
- Revenue / ARR CAGR over hold period (bull / base / bear)
- Terminal year revenue at exit
- Expected exit revenue multiple (or EBITDA multiple, if durably profitable by exit)

**Vehicle**
- Management fee (typically 1-2% on committed or invested)
- Carried interest (typically 10-20% over a preferred return, if any)
- Preferred return / hurdle (if any)
- Estimated SPC operating expenses (admin, audit, legal — fixed $ per year)
- Hold period in years

**Exit**
- Exit scenarios to model:
  - **IPO with lockup** (180 days standard) — model exit at unlock at then-current public multiple
  - **Strategic / financial M&A** — typically lower multiple but liquid
  - **Pre-IPO secondary block** — typically requires a meaningful discount to then-private valuation

### Step 2: Base Case Returns (Gross and Net)

Calculate at vehicle (SPC) level:

| Metric | Value |
|--------|-------|
| Entry valuation (implied post-money) | |
| Equity invested at SPC | |
| Exit valuation (base case) | |
| Pro-rata exit proceeds at SPC | |
| Transaction costs (entry + exit) | |
| **Gross MOIC** | |
| **Gross IRR** | |
| Cumulative management fees | |
| Carried interest distributed | |
| **Net MOIC (to LP)** | |
| **Net IRR (to LP)** | |

Returns attribution (gross):
- Revenue growth contribution (terminal revenue / entry revenue)
- Multiple expansion / contraction contribution
- Entry discount capture (if bought below last round value)
- Fee and cost drag (always negative)

### Step 3: Sensitivity Tables

Build 2-way sensitivity matrices. In each cell, show **Net IRR / Net MOIC** to LP.

**Exit Valuation vs. Hold Period** (most important — exit timing risk dominates secondaries)

| | 2yr hold | 3yr hold | 4yr hold | 5yr hold | 6yr hold |
|---|----------|----------|----------|----------|----------|
| Exit at 1x entry | | | | | |
| Exit at 1.5x | | | | | |
| Exit at 2x | | | | | |
| Exit at 3x | | | | | |
| Exit at 5x | | | | | |

**Revenue CAGR vs. Exit Revenue Multiple** (the underlying value drivers)

**Entry Discount vs. Exit Valuation** (how much does the discount you negotiated actually buy you)

### Step 4: Scenario Analysis

Build 3 scenarios for IC / LP communication:

| | Bull | Base | Bear |
|---|------|------|------|
| Revenue CAGR over hold | | | |
| Hold period | | | |
| Exit type | | | |
| Exit valuation | | | |
| Gross MOIC / IRR | | | |
| Net MOIC / IRR | | | |

Always include a genuine downside scenario where exit is delayed and / or the company raises a flat or down round at the secondary market discount. A 1.0x net MOIC is not a downside.

### Step 5: Output

Excel workbook with:
- Inputs / assumptions tab
- Base case calculation
- Sensitivity tables (conditional formatting — green for above hurdle, red for below)
- Scenario summary
- LP-facing one-page returns summary

## Key Formulas

- **Gross MOIC** = Exit Proceeds (pre-fee) / Equity Invested
- **Net MOIC** = LP Distribution / LP Contribution (after management fees and carry)
- **Gross IRR** = solve for r: Equity × (1 + r)^n = Exit Proceeds (adjust for interim cash flows)
- **Net IRR**: same equation applied to LP-level cash flows (capital calls, fees, distributions)
- **Returns attribution**:
  - Growth: (Exit Revenue / Entry Revenue − 1) × Entry Valuation, applied to equity stake
  - Multiple: (Exit Multiple − Entry Multiple) × Exit Revenue, applied to equity stake
  - Discount capture: Last Round Value − Entry Price (one-time, at close)
  - Fee drag: (Gross IRR − Net IRR) over the hold

## Important Notes

- **No leverage.** Don't model debt — these are unlevered equity positions in private companies.
- **No EBITDA bridge.** Late-stage private tech is typically modelled on revenue multiples; only use EBITDA mechanics if the company is durably profitable.
- **Fee drag is material.** A 1.5% management fee plus 15% carry on a 3-year hold compresses a gross 3.0x to roughly net 2.4-2.5x. Always report both gross and net.
- **Lockup risk.** If exit is via IPO, the 180-day lockup means actual realisation is six months after IPO. Build this into IRR — the difference is meaningful at short holds.
- **Lot size and pro-rata.** If the SPC is one of multiple co-investors in an SPV, model the SPC's pro-rata share of fees and proceeds, not the underlying SPV economics.
- **US investor treatment.** If the underlying company is a PFIC and a QEF election is unavailable, after-tax returns to US LPs are materially worse than the pre-tax net IRR. Flag this in the LP-facing summary if relevant.
- **Liquidity discount on secondary exit.** If modelling a pre-IPO secondary block exit (not IPO), apply a 20-35% discount to then-private valuation to reflect the same buyer-side bid you exploited at entry.
- **Preferred share economics.** If the position is in preferred stock with a liquidation preference, model the preference in downside scenarios — it materially changes the bear case.
