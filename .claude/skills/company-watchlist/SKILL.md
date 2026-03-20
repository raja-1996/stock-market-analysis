---
name: company-watchlist
description: Screen and identify companies showing early interesting signals worth monitoring. Use when the user asks about interesting stocks, companies to watch, earnings movers, insider buying, analyst upgrades, or wants a broad market scan for notable activity.
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Company Watchlist Screening

Research and identify companies showing early interesting signals from the last 7 days. These are NOT buy/sell calls — they are names worth monitoring for developing situations. Use web search to find latest company news and data.

Today's date: !`date +%Y-%m-%d`

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

## Scoring Reference
- **Signal Strength** (1-5): 5=Very Strong, 4=Strong, 3=Moderate, 2=Weak, 1=Speculative
- **Risk Rating**: Low / Medium / High / Very High

## Output Template
Follow the template in `.claude/skills/company-watchlist/template.md`

Save the report to: `reports/YYYY-MM-DD-company-watchlist.md`
