# Deal Screening — Pre-IPO Secondaries

description: Quickly screen inbound late-stage private secondary opportunities against the fund's investment criteria. Designed for BVI SPC vehicles taking minority positions in private technology companies via secondaries, structured primaries, or SPV access. Extracts deal facts, applies a pass/fail framework calibrated to growth-stage metrics (not LBO buyouts), and outputs a one-page screening memo. Use when reviewing brokered secondary offers, forwarded SPV deals, direct primary allocations, or triaging inbound deal flow. Triggers on "screen this deal", "screen this secondary", "review this offer", "should we look at this", "triage this opportunity", or "deal screening".

## Workflow

### Step 1: Extract Deal Facts

From the offer materials (broker memo, SPV summary, founder/CFO note, or description), extract:

**Company**
- Name, sector/subsector, headquarters and primary jurisdictions of operation
- Stage and most recent round (series, date, lead, post-money)
- Description (1-2 sentences of what they do)

**Operating metrics**
- Latest ARR or revenue run-rate
- YoY revenue / ARR growth
- Gross margin (compute-adjusted for AI / infra companies)
- Net dollar retention (where applicable)
- Burn rate and cash runway (or path to profitability)
- Headcount and recent hiring trend

**Deal terms**
- Type: secondary (direct / tender / SPV), primary, structured primary
- Share class on offer (common, preferred series — material for liquidation preference)
- Implied valuation (post-money $)
- Discount to last primary / 409A / most recent secondary print
- Tranche size offered; minimum and maximum bites
- Seller (employee / early investor / fund LP / founder) and stated motivation
- Timing pressure (binding date, ROFR window, expiry)

**Structural**
- Transfer restrictions, ROFR / company consent status (P0 — most secondaries die here)
- Information rights post-close (full / pro-rata / none)
- Carry and fee profile if going via an SPV (vs. direct on cap table)
- US investor compatibility (PFIC exposure, QEF election availability — flag for tax counsel)

**Liquidity**
- Stated path to liquidity (IPO timing, M&A optionality, ongoing secondary market depth)
- Lockups expected post-IPO

### Step 2: Screen Against Criteria

Apply the fund's investment criteria (ask user if not on file):

| Criterion | Target | Actual | Pass/Fail |
|-----------|--------|--------|-----------|
| Revenue / ARR scale | | | |
| Growth rate | | | |
| Gross margin | | | |
| Net dollar retention | | | |
| Sector fit | | | |
| Stage (Series E+ / pre-IPO) | | | |
| Implied valuation | | | |
| Discount to last round | | | |
| Tranche size fit (SPC vehicle) | | | |
| Liquidity timeline | | | |
| Transfer status (ROFR clean?) | | | |
| Information rights | | | |
| US investor structure (PFIC) | | | |

### Step 3: Quick Assessment

Provide a 4-part assessment:

1. **Verdict**: Pass / Further Diligence / Hard Pass
2. **Bull case** (2-3 bullets): What makes this attractive vs. comparable late-stage opportunities, and what about the entry point specifically (discount, structural access, timing)
3. **Bear case** (2-3 bullets): What you'd worry about — growth deceleration, multiple compression, transfer restrictions, governance, share-class economics
4. **Key questions** (3-5 bullets): What you need answered before progressing. Always include: ROFR clearance pathway, latest financials beyond the broker headline, share-class mechanics on a liquidation event.

### Step 4: Output

One-page screening memo formatted for an internal IC quick screen. Tone is direct — no hedging. If the offer's headline number is misleading (e.g. discount to a stale 409A, share class differences hiding the true effective price), say so explicitly.

## Important Notes

- Speed matters — secondary screening should take under 30 minutes for a typical broker offer.
- Be direct about red flags. Brokers oversell; bid discipline starts at screen.
- **Discount to last round is not the same as discount to current value.** A 10% headline discount to a 12-month-old round may still be expensive vs. current fundamentals — call this out where relevant.
- **Common vs. preferred matters.** A "secondary" of common stock at the same headline as the preferred is usually a worse deal than it looks. Always note share class and where it sits in the preference stack.
- **ROFR / company consent is the most frequent kill condition.** If the seller can't confirm a path to closing without company friction, flag at screen rather than wasting DD cycles.
- For US investor tranches, PFIC exposure on the underlying company should be a screen-stage flag, not a discovery in subscription docs.
- Save fund criteria in memory once confirmed for future deals.
