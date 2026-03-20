# Stock Market Analysis - Economic News Analyzer

## Purpose
This project is an AI-driven economic news research and analysis system. It researches news from the last 7 days and produces structured investment reports covering macro economy, sector trends, and company-level signals.

## Skills Available

The following skills are available in `.claude/skills/`. Claude will auto-trigger the appropriate skill based on your request — just ask naturally. You can also invoke any skill manually with `/skill-name`.

### `/macro-economy` — Macro Economic Analysis
Analyzes GDP, inflation, Fed policy, interest rates, employment data, consumer sentiment, and global macro factors.
**Auto-triggers when you ask about**: economy, macro outlook, inflation, interest rates, jobs data, Fed, GDP, recession risk, or overall market conditions.

### `/sector-trends` — Sector Performance & Rotation
Ranks all 11 GICS sectors by weekly performance, identifies rotation patterns, thematic trends (AI, energy transition, GLP-1, reshoring), and ETF flow data.
**Auto-triggers when you ask about**: sectors, industry performance, sector rotation, which sectors are hot/cold, ETF flows, or thematic investing.

### `/company-watchlist` — Company Screening & Watchlist
Screens for companies showing early interesting signals — earnings surprises, analyst upgrades/downgrades, insider buying clusters, M&A, technical breakouts, unusual volume.
**Auto-triggers when you ask about**: interesting stocks, what's moving, earnings movers, insider buying, analyst activity, or a broad market scan.

### `/buy-opportunities` — Buy Opportunity Identification
Identifies companies with clear buying signals where fundamentals, catalysts, valuation, technicals, and smart money all align. Strict qualification: Signal Strength 4-5, 3+ fundamental positives, near-term catalyst required.
**Auto-triggers when you ask about**: stocks to buy, undervalued companies, bullish setups, investment opportunities, or actionable buy ideas.

### `/exit-signals` — Exit & Red Flag Warnings
Identifies companies showing deterioration — earnings misses, margin compression, insider selling, SEC red flags, technical breakdowns, valuation traps. Classifies by urgency: URGENT / HIGH / MODERATE.
**Auto-triggers when you ask about**: stocks to sell or avoid, red flags, bearish companies, portfolio risk, deteriorating fundamentals, or what to exit.

### `/investment-picks` — Long-Term Investment Candidates
Selects quality companies for 6-12+ month holding — focuses on competitive moats, growth runways, financial health, ROIC, and reasonable valuations. Different from buy-opportunities (tactical) — these are strategic portfolio builders.
**Auto-triggers when you ask about**: long-term investments, portfolio building, quality stocks, best stocks to hold, or strategic investment candidates.

### `/full-report` — Complete Weekly Market Intelligence Report (Manual Only)
Runs ALL 6 analyses above in sequence (macro → sectors → watchlist → buy → exit → investment picks), then compiles a master executive summary. Each step builds on the previous one's context.
**Manual invoke only** — type `/full-report` to run. Not auto-triggered to prevent accidentally running the full pipeline.

### How Skills Work
- **Auto-invoke**: Skills 1-6 are triggered automatically when Claude detects your request matches the skill description. Just ask naturally — e.g., "what sectors are hot right now?" triggers `/sector-trends`.
- **Manual invoke**: Type `/full-report` to run the complete end-to-end analysis pipeline.
- Each skill has its own directory under `.claude/skills/` with a `SKILL.md` (instructions + YAML frontmatter) and `template.md` (output format).
- Skills use `allowed-tools` to restrict tool access and `!`date`` for dynamic date injection.
- Buy/exit/investment skills auto-read existing reports in `reports/` for cross-referencing context.

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
