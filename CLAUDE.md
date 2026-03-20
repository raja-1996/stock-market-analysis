# Stock Market Analysis - Economic News Analyzer

## Purpose
This project is an AI-driven economic news research and analysis system. It researches news from the last 7 days and produces structured investment reports covering macro economy, sector trends, and company-level signals.

## Available Analysis Commands
Each analysis type is a standalone skill that can be triggered independently or composed into a full report:

- `/macro-economy` — Macro economic overview (GDP, inflation, rates, employment, sentiment)
- `/sector-trends` — Sector rotation, ETF performance, hot/cold sectors
- `/company-watchlist` — Early-signal companies worth monitoring
- `/buy-opportunities` — Clear opportunity companies with strong catalysts
- `/exit-signals` — Companies showing red flags, deteriorating fundamentals
- `/investment-picks` — Balanced risk/reward investment candidates
- `/full-report` — Runs ALL analyses above and compiles a comprehensive report

## Data Sources to Reference
When performing any analysis, pull from these source categories:
- **Financial News**: Reuters, Bloomberg, CNBC, MarketWatch, WSJ, Financial Times
- **Economic Data**: Bureau of Labor Statistics (BLS), Federal Reserve (FRED), US Treasury, Commerce Dept
- **Market Data**: Major index performance (S&P 500, NASDAQ, Dow, Russell 2000), VIX, bond yields
- **SEC / Earnings**: Recent 10-K/10-Q filings, earnings calls, guidance updates
- **Analyst Activity**: Upgrades/downgrades, price target changes, initiations
- **Fund Flows**: Institutional buying/selling, ETF inflows/outflows, 13F filings
- **Insider Activity**: Insider buying/selling patterns from SEC Form 4

## Scoring Framework
Use this consistent scoring system across all company analyses:

### Signal Strength (1-5)
- **5 — Very Strong**: Multiple confirming signals across fundamental, technical, and sentiment
- **4 — Strong**: Clear signal with at least 2 confirming factors
- **3 — Moderate**: Notable signal but mixed confirming factors
- **2 — Weak**: Early signal, needs more confirmation
- **1 — Speculative**: Single data point, high uncertainty

### Risk Rating (Low / Medium / High / Very High)
Based on: volatility, liquidity, sector risk, company-specific risk, macro exposure

## Output Standards
- Always state the analysis date range (last 7 days from current date)
- Cite specific news sources and dates for every claim
- Include ticker symbols for all companies mentioned
- Provide clear bull/bear cases, never one-sided analysis
- End every company section with a risk disclaimer
- Use tables for comparisons and rankings
- Keep language clear and jargon-free where possible

## Report Storage
Save all generated reports to the `reports/` directory with naming convention:
`reports/YYYY-MM-DD-{analysis-type}.md`

## Disclaimer
All analysis is for educational and research purposes only. Not financial advice. Always do your own due diligence before making investment decisions.
