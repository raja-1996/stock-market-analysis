---
name: investment-picks
description: Identify quality companies for medium to long-term investment with strong moats, growth runways, and reasonable valuations. Use when the user asks about long-term investments, portfolio building, quality stocks, or strategic investment candidates.
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Investment Picks Analysis

Research and identify balanced investment candidates from the last 7 days — companies with favorable risk/reward profiles for medium to long-term holding. Use web search to find latest data and news.

Today's date: !`date +%Y-%m-%d`

## How This Differs from Buy Opportunities
- **Buy Opportunities** = tactical, catalyst-driven, shorter time horizon
- **Investment Picks** = strategic, quality-focused, 6-12+ month holding period, portfolio building

## Pre-Check
Before starting, read any existing reports in `reports/` directory from this week (especially macro, sector, and buy-opportunities) for context and to avoid duplicating picks.

## Research Checklist

### 1. Business Quality Assessment
- Durable competitive advantages (moat)
- Consistent revenue and earnings growth track record
- Strong management team with good capital allocation history
- High returns on invested capital (ROIC)
- Recurring or predictable revenue streams
- Industry leadership position

### 2. Growth Runway
- Total addressable market (TAM) expanding
- Multiple growth vectors (products, geographies, adjacencies)
- Secular tailwinds supporting the business
- R&D pipeline or innovation track record
- Ability to grow without excessive dilution or debt

### 3. Financial Health
- Strong balance sheet (net cash or manageable debt)
- Consistent free cash flow generation
- Healthy margins with stability or expansion trend
- Shareholder-friendly capital return (buybacks, dividends)
- No accounting red flags

### 4. Valuation Reasonableness
- Not trading at extreme premium to historical range
- Reasonable relative to growth rate (PEG, EV/EBITDA/growth)
- Margin of safety exists at current price
- DCF or comparable analysis supports upside

### 5. Recent Developments (Last 7 Days)
- Any earnings or guidance updates
- Strategic announcements (M&A, partnerships, new products)
- Management commentary on outlook
- Analyst perspective changes
- Sector dynamics shifting in their favor

### 6. Portfolio Fit Considerations
- Diversification across sectors
- Mix of growth and value characteristics
- Range of market cap sizes (large, mid, small)
- Income generation potential (dividends)
- Correlation to existing common holdings

## Qualification Criteria
A company qualifies as an "Investment Pick" if it meets:
- Business quality score of 4-5
- Growth runway clearly identifiable
- Financial health solid (no balance sheet concerns)
- Valuation not extreme — reasonable entry point
- Recent catalyst or development that makes NOW a good time

## Output Template
Follow the template in `.claude/skills/investment-picks/template.md`

Save the report to: `reports/YYYY-MM-DD-investment-picks.md`
