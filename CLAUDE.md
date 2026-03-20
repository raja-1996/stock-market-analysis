# Stock Market Analysis - Economic News Analyzer

## Purpose
This project is an AI-driven economic news research and analysis system. It researches news from the last 7 days and produces structured investment reports covering macro economy, sector trends, and company-level signals.

## Available Analysis Skills
Each analysis type is a standalone skill. Claude can **auto-trigger** them based on your request, or you can invoke manually:

| Skill | Trigger | Auto-Invoke |
|-------|---------|-------------|
| `/macro-economy` | Economy, GDP, inflation, rates, employment, sentiment | Yes |
| `/sector-trends` | Sectors, rotation, ETFs, industry performance | Yes |
| `/company-watchlist` | Interesting stocks, earnings movers, insider buying, market scan | Yes |
| `/buy-opportunities` | Stocks to buy, undervalued, bullish setups, opportunities | Yes |
| `/exit-signals` | Stocks to sell/avoid, red flags, bearish, deteriorating | Yes |
| `/investment-picks` | Long-term investments, portfolio building, quality stocks | Yes |
| `/full-report` | Full weekly report (runs all 6 above in sequence) | Manual only |

### How Skills Work
- **Auto-invoke**: Skills 1-6 are triggered automatically when Claude detects your request matches the skill description. Just ask naturally — e.g., "what sectors are hot right now?" triggers `/sector-trends`.
- **Manual invoke**: Type `/full-report` to run the complete end-to-end analysis pipeline.
- Each skill has its own directory under `.claude/skills/` with a `SKILL.md` (instructions + frontmatter) and `template.md` (output format).

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

## Project Structure
```
CLAUDE.md                                   # This file — main orchestrator
.claude/skills/
├── macro-economy/
│   ├── SKILL.md                            # Instructions + frontmatter
│   └── template.md                         # Output format template
├── sector-trends/
│   ├── SKILL.md
│   └── template.md
├── company-watchlist/
│   ├── SKILL.md
│   └── template.md
├── buy-opportunities/
│   ├── SKILL.md
│   └── template.md
├── exit-signals/
│   ├── SKILL.md
│   └── template.md
├── investment-picks/
│   ├── SKILL.md
│   └── template.md
└── full-report/
    ├── SKILL.md
    └── template.md
reports/                                    # Generated reports land here
```

## Disclaimer
All analysis is for educational and research purposes only. Not financial advice. Always do your own due diligence before making investment decisions.
