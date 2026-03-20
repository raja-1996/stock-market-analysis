---
name: full-report
description: Run a comprehensive end-to-end weekly market analysis covering macro economy, sectors, watchlist, buy opportunities, exit signals, and investment picks. Use when the user asks for a full market report, weekly analysis, complete market overview, or wants all analyses run together.
disable-model-invocation: true
allowed-tools: WebSearch, WebFetch, Read, Write, Bash, Glob, Grep
---

# Full Market Analysis Report

Run a comprehensive end-to-end analysis covering all six modules. Execute each analysis sequentially, building context from one to the next.

Today's date: !`date +%Y-%m-%d`

## Execution Order

Run each skill in sequence. Each step builds on the previous one's context.

### Step 1: Macro Economy
Run the `/macro-economy` analysis first — this sets the backdrop for everything else.
- Research GDP, inflation, Fed policy, employment, sentiment, global factors
- Establish whether macro environment is bullish, bearish, or neutral
- Save to `reports/YYYY-MM-DD-macro-economy.md`

### Step 2: Sector Trends
With macro context established, run `/sector-trends`.
- Rank all 11 GICS sectors by weekly performance
- Identify rotation patterns and thematic trends
- Determine overweight/underweight sector views
- Save to `reports/YYYY-MM-DD-sector-trends.md`

### Step 3: Company Watchlist
Run `/company-watchlist` to screen for early signals.
- Cast a wide net across earnings, analyst activity, insider buying, corporate events
- Identify 10-15 companies worth monitoring
- Save to `reports/YYYY-MM-DD-company-watchlist.md`

### Step 4: Buy Opportunities
Run `/buy-opportunities` using watchlist and sector context.
- Apply strict qualification criteria (Signal Strength 4-5, multiple confirmations)
- Provide full investment thesis for each
- Save to `reports/YYYY-MM-DD-buy-opportunities.md`

### Step 5: Exit Signals
Run `/exit-signals` to find deteriorating companies.
- Look for fundamental breakdowns, insider selling, technical damage
- Classify by urgency (URGENT / HIGH / MODERATE)
- Save to `reports/YYYY-MM-DD-exit-signals.md`

### Step 6: Investment Picks
Run `/investment-picks` for long-term candidates.
- Focus on business quality, moat, growth runway
- Ensure portfolio diversification across picks
- Save to `reports/YYYY-MM-DD-investment-picks.md`

### Step 7: Compile Executive Summary
After all 6 analyses are complete, create a master summary using the template in `.claude/skills/full-report/template.md`.

Save the compiled report to: `reports/YYYY-MM-DD-full-report.md`

## Post-Report Validation
After completing the full report:
1. Verify all 7 report files exist in the `reports/` directory
2. Check that all company tickers are consistent across sections
3. Ensure no contradictions between sections (e.g., same company in buy AND exit)
4. Confirm all claims have cited sources
