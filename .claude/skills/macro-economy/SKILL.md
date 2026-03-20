---
name: macro-economy
description: Analyze macroeconomic landscape including GDP, inflation, Fed policy, employment, and global factors. Use when the user asks about economy, macro outlook, interest rates, inflation, jobs data, or overall market conditions.
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Macro Economy Analysis

Research and analyze the macroeconomic landscape from the last 7 days. Use web search to find the latest data and news.

Today's date: !`date +%Y-%m-%d`

## Research Checklist
Investigate each of the following areas by searching for recent news and data:

### 1. GDP & Growth
- Latest GDP data or revisions
- Leading economic indicators (LEI)
- PMI / ISM manufacturing and services data
- Consumer spending trends

### 2. Inflation
- CPI / PPI latest readings
- Core vs headline inflation trends
- Fed's preferred PCE measure
- Inflation expectations (breakevens, surveys)

### 3. Federal Reserve & Interest Rates
- Recent Fed speeches or meeting minutes
- Rate decision or forward guidance changes
- Market-implied rate expectations (Fed funds futures)
- Quantitative tightening updates

### 4. Employment
- Non-farm payrolls, unemployment rate
- Jobless claims (initial + continuing)
- Wage growth trends
- Labor force participation

### 5. Consumer & Business Sentiment
- Consumer confidence (Conference Board, Michigan)
- CEO confidence surveys
- Small business optimism (NFIB)
- Credit conditions

### 6. Global Macro Factors
- Major central bank decisions globally (ECB, BOJ, BOE)
- Geopolitical developments affecting markets
- Trade policy updates, tariffs
- Currency movements (DXY, major pairs)
- Commodity prices (oil, gold, copper)

## Scoring Reference
Use the scoring framework from CLAUDE.md:
- **Signal Strength** (1-5): 5=Very Strong, 4=Strong, 3=Moderate, 2=Weak, 1=Speculative
- **Risk Rating**: Low / Medium / High / Very High

## Output Template
Follow the template in `.claude/skills/macro-economy/template.md`

Save the report to: `reports/YYYY-MM-DD-macro-economy.md`
