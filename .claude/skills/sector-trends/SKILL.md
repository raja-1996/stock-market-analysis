---
name: sector-trends
description: Analyze sector performance, rotation patterns, and thematic trends across all 11 GICS sectors. Use when the user asks about sectors, industry performance, sector rotation, which sectors are hot or cold, or thematic investing trends.
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Sector Trends Analysis

Research and analyze sector-level performance and rotation trends from the last 7 days. Use web search to find latest sector data and news.

Today's date: !`date +%Y-%m-%d`

## Research Checklist

### 1. Sector Performance Ranking
Search for performance of all 11 GICS sectors over the past week:
- Technology (XLK)
- Healthcare (XLV)
- Financials (XLF)
- Consumer Discretionary (XLY)
- Consumer Staples (XLP)
- Energy (XLE)
- Industrials (XLI)
- Materials (XLB)
- Real Estate (XLRE)
- Utilities (XLU)
- Communication Services (XLC)

### 2. Sector Rotation Signals
- Which sectors are leading vs lagging?
- Money flow patterns — where is capital rotating to/from?
- Defensive vs cyclical positioning (risk-on vs risk-off)
- Relative strength trends shifting

### 3. Sector-Specific Catalysts
For each notable sector, identify:
- Regulatory changes or policy news
- Major earnings from sector bellwethers
- Supply/demand dynamics
- Technological disruptions or breakthroughs
- M&A activity within the sector

### 4. Thematic Trends
- AI / semiconductor demand cycle
- Energy transition / clean energy
- Interest rate sensitivity plays (REITs, banks, utilities)
- Reshoring / infrastructure
- Healthcare innovation (GLP-1, biotech pipeline)
- Consumer spending shifts

### 5. ETF Flow Data
- Sector ETF inflows/outflows
- Leveraged/inverse ETF activity (sentiment indicator)
- New ETF launches or closures in specific themes

## Output Template
Follow the template in `.claude/skills/sector-trends/template.md`

Save the report to: `reports/YYYY-MM-DD-sector-trends.md`
