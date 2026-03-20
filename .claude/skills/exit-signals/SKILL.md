---
name: exit-signals
description: Identify companies showing clear warning signs, red flags, and deteriorating conditions. Use when the user asks about stocks to sell, avoid, or reduce, companies with problems, red flags, bearish setups, or risk warnings.
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Exit Signals Analysis

Research and identify companies showing clear warning signs and deteriorating conditions from the last 7 days. These are companies where holders should consider reducing or exiting positions. Use web search to find latest data and news.

Today's date: !`date +%Y-%m-%d`

## Pre-Check
Before starting, read any existing reports in `reports/` directory from this week for context.

## Research Checklist

### 1. Fundamental Deterioration
- Earnings miss with lowered guidance
- Revenue deceleration or decline
- Margin compression
- Cash burn acceleration
- Debt levels rising / covenant concerns
- Declining return on equity

### 2. Red Flag Events
- SEC investigations or accounting irregularities
- Auditor changes or qualified opinions
- Restatements of prior financials
- Executive departures (especially CFO)
- Dividend cuts or suspension
- Credit rating downgrades

### 3. Competitive / Industry Threats
- Market share losses to competitors
- Disruptive technology emerging in their space
- Regulatory headwinds (new rules, fines, bans)
- Key customer or contract losses
- Patent expirations or IP challenges
- Supply chain disruptions unique to company

### 4. Insider & Smart Money Exits
- Heavy insider selling (especially CEO/CFO)
- Multiple insiders selling simultaneously
- Institutional ownership declining
- Major hedge fund exits (13F data)
- Analyst downgrades with significant PT cuts

### 5. Technical Breakdown Signals
- Price below 50-day AND 200-day moving averages
- Death cross (50-day crossing below 200-day)
- Breaking key support levels on high volume
- Relative strength declining vs sector and market
- Increasing short interest

### 6. Valuation Traps
- Looks cheap but fundamentals deteriorating ("value trap")
- Sector derating in progress
- Peer group all declining (systemic issue)
- Earnings estimates being revised down

## Qualification Criteria
A company qualifies as an "Exit Signal" if it has:
- Signal Strength 4-5 on the negative side
- At least 2 fundamental negatives
- At least 1 confirmed red flag or catalyst for further decline
- Technical picture bearish

## Warning Level Classification
- **URGENT**: Multiple severe red flags, immediate review recommended
- **HIGH**: Strong deterioration signals, consider reducing position
- **MODERATE**: Early warning signs developing, monitor closely

## Output Template
Follow the template in `.claude/skills/exit-signals/template.md`

Save the report to: `reports/YYYY-MM-DD-exit-signals.md`
