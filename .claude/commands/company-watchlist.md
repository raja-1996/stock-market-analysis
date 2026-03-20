# Company Watchlist Screening

Research and identify companies showing early interesting signals from the last 7 days. These are NOT buy/sell calls — they are names worth monitoring for developing situations. Use web search to find latest company news and data.

## Research Checklist

### 1. Earnings Surprises
- Companies that beat/missed earnings significantly in the past week
- Notable guidance raises or cuts
- Unusual earnings call commentary

### 2. Analyst Activity
- Fresh initiations at major brokerages
- Significant price target changes (>15% move)
- Rating changes (upgrades/downgrades)
- Contrarian analyst calls

### 3. Insider Activity
- Unusual insider buying clusters (multiple insiders buying)
- Large single insider purchases (>$1M)
- CEO/CFO buying (highest signal value)
- Note: Insider selling alone is weaker signal (can be tax/diversification)

### 4. Corporate Events
- M&A announcements or rumors
- Spin-offs, splits, or restructuring
- New product launches or FDA approvals
- Major contract wins or losses
- Management changes (CEO, CFO)

### 5. Technical Breakouts / Breakdowns
- Stocks hitting 52-week highs/lows with volume
- Unusual volume spikes (>3x average)
- Key technical level breaks

### 6. News-Driven Movers
- Companies in the news for regulatory reasons
- Legal/litigation developments
- Policy beneficiaries or victims
- Social media / retail investor attention

## Screening Criteria
A company makes the watchlist if it has:
- At least 2 signals from different categories above, OR
- 1 very strong signal (Signal Strength 4-5)

## Output Format

```markdown
# Company Watchlist — [Date Range]

## Executive Summary
[Number of companies screened, key themes emerging]

## Watchlist

### [Company Name] ($TICKER) — [Sector]
- **Signal Strength**: [1-5] | **Risk**: [Low/Med/High/Very High]
- **Why it's on the list**: [1-2 sentence summary]
- **Signals detected**:
  - [Signal 1 with source and date]
  - [Signal 2 with source and date]
- **What to watch next**: [upcoming catalyst or confirmation needed]
- **Bull case**: [brief]
- **Bear case**: [brief]

---

[Repeat for each company]

## Watchlist Summary Table

| Ticker | Company | Sector | Signal Strength | Key Signal | Next Catalyst |
|--------|---------|--------|----------------|------------|---------------|

## Sources
[Numbered list of all sources cited]
```

Save the report to: `reports/YYYY-MM-DD-company-watchlist.md`
