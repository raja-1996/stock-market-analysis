# Full Market Analysis Report

Run a comprehensive end-to-end analysis covering all six modules. Execute each analysis sequentially, building context from one to the next.

## Execution Order

### Step 1: Macro Economy
Run the macro economy analysis first — this sets the backdrop for everything else.
- Research GDP, inflation, Fed policy, employment, sentiment, global factors
- Establish whether macro environment is bullish, bearish, or neutral
- Save to `reports/YYYY-MM-DD-macro-economy.md`

### Step 2: Sector Trends
With macro context established, analyze sector performance and rotation.
- Rank all 11 GICS sectors by weekly performance
- Identify rotation patterns and thematic trends
- Determine overweight/underweight sector views
- Save to `reports/YYYY-MM-DD-sector-trends.md`

### Step 3: Company Watchlist
Screen for companies showing early interesting signals.
- Cast a wide net across earnings, analyst activity, insider buying, corporate events
- Identify 10-15 companies worth monitoring
- Save to `reports/YYYY-MM-DD-company-watchlist.md`

### Step 4: Buy Opportunities
From watchlist and sector analysis, identify clear buying opportunities.
- Apply strict qualification criteria (Signal Strength 4-5, multiple confirmations)
- Provide full investment thesis for each
- Save to `reports/YYYY-MM-DD-buy-opportunities.md`

### Step 5: Exit Signals
Identify companies showing deterioration and red flags.
- Look for fundamental breakdowns, insider selling, technical damage
- Classify by urgency (URGENT / HIGH / MODERATE)
- Save to `reports/YYYY-MM-DD-exit-signals.md`

### Step 6: Investment Picks
Select quality companies for medium to long-term investment.
- Focus on business quality, moat, growth runway
- Ensure portfolio diversification across picks
- Save to `reports/YYYY-MM-DD-investment-picks.md`

### Step 7: Compile Executive Summary
After all 6 analyses are complete, create a master summary report.

Save the compiled report to: `reports/YYYY-MM-DD-full-report.md`

## Compiled Report Format

```markdown
# Weekly Market Intelligence Report — [Date Range]

## Executive Summary
[5-7 bullet points capturing the most critical insights across all analyses]

## Macro Environment: [Bullish / Neutral / Bearish]
[2-3 sentence summary of macro backdrop]

## Sector Positioning
| Overweight | Underweight | Watch |
|-----------|-------------|-------|
| [sectors] | [sectors]   | [sectors] |

## Top Watchlist Names
[Table of top 5 most interesting watchlist companies]

## Buy Opportunities
[Table of all qualified buy opportunities with conviction and upside]

## Exit Warnings
[Table of all exit signals with warning level and downside risk]

## Investment Picks
[Table of all investment picks with style, conviction, and base case return]

## Key Dates Ahead
[Important upcoming events: Fed meetings, major earnings, economic releases]

## Risk Dashboard
| Risk Factor | Level | Trend | Impact |
|-------------|-------|-------|--------|
| [factor] | [1-5] | [Rising/Falling/Stable] | [description] |

## Methodology Note
This report was compiled using the Stock Market Analysis framework, analyzing news and data from [start date] to [end date]. Each section uses a standardized scoring framework (Signal Strength 1-5, Risk Rating Low/Med/High/Very High). See individual section reports for detailed analysis and complete source citations.

## Disclaimer
This report is for educational and research purposes only. It does not constitute financial advice, investment recommendations, or an offer to buy or sell securities. Past performance is not indicative of future results. Always conduct your own research and consult with a qualified financial advisor before making investment decisions.
```

## Post-Report Actions
After completing the full report:
1. Verify all 7 report files exist in the `reports/` directory
2. Check that all company tickers are consistent across sections
3. Ensure no contradictions between sections (e.g., same company in buy AND exit)
4. Confirm all claims have cited sources
