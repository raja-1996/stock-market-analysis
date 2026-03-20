---
name: buy-opportunities
description: Identify companies with clear buying opportunity signals backed by fundamentals, catalysts, and technicals. Use when the user asks about stocks to buy, investment opportunities, undervalued companies, bullish setups, or wants actionable buy ideas.
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Buy Opportunities Analysis

Research and identify companies with clear buying opportunity signals from the last 7 days. These are companies where multiple factors align to suggest potential upside. Use web search to find latest data and news.

Today's date: !`date +%Y-%m-%d`

## Pre-Check
Before starting, read any existing reports in `reports/` directory from this week for context (especially macro-economy and sector-trends reports if they exist).

## Research Checklist

### 1. Fundamental Strength
- Strong earnings beat with raised guidance
- Revenue acceleration (sequential and YoY)
- Margin expansion
- Free cash flow growth
- Healthy balance sheet (low debt, strong cash position)
- Improving return on equity (ROE)

### 2. Catalyst Identification
- New product cycle beginning
- Market share gains documented
- TAM expansion (new markets, geographies)
- Regulatory tailwinds (approvals, favorable policy)
- Cost restructuring benefits materializing
- Industry consolidation beneficiary

### 3. Valuation Check
- Trading below historical average multiples
- Discount to peer group
- PEG ratio attractive (<1.5 for growth, reasonable for value)
- Price/FCF compelling
- Sum-of-parts undervaluation

### 4. Technical Confirmation
- Price above key moving averages (50-day, 200-day)
- Relative strength vs sector and market positive
- Volume confirming price moves
- Bullish pattern formations

### 5. Smart Money Signals
- Institutional accumulation (rising ownership %)
- Insider buying activity
- Analyst upgrades with conviction
- Hedge fund 13F additions

## Qualification Criteria
A company qualifies as a "Buy Opportunity" if it meets ALL of:
- Signal Strength 4-5
- At least 3 fundamental positives
- At least 1 clear near-term catalyst
- Technical picture not bearish
- Valuation not extreme (not top decile of sector)

## Output Template
Follow the template in `.claude/skills/buy-opportunities/template.md`

Save the report to: `reports/YYYY-MM-DD-buy-opportunities.md`
