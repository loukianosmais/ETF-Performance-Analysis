# Hi there, I'm Loukianos 👋

🎓 **International Economics Student** at Athens University of Economics and Business (AUEB)
🤖 **AI & Tech Enthusiast** with certifications from Claude Academy (AI Fluency, Human-Agent Teams)
🛠️ **Maker & Developer** working on Web Applications & Embedded Systems / Robotics

### 🛠️ Tech & Tools
* **AI & Machine Learning:** LLMs, Claude API, AI Agents, Prompting
* **Hardware & IoT:** Arduino, Circuit Design, Sensors & Modules
* **Web & Programming:** C++, Python, HTML/CSS, Web Games

### 📁 Featured Projects
* 🎮 **Football-Arcade** – Web-based arcade game built with AI-assisted programming
* 🤖 **Smart Object Detection** – Arduino system with ultrasonic sensors & audio/visual feedback
* 🎰 **Arduino Slot Machine** – Interactive DIY slot machine built with Arduino Uno R3

📫 **Connect with me:** [LinkedIn](https://www.linkedin.com/in/loukianos-mais)

# Which ETF Performed Best? A Data Analytics Project

## Research question
Which ETF is the best, based on its performance over the past few years?

## What "best" means here
Raw return favors risky funds, so results are shown **within category** (broad market, growth, value/dividend, mid/small cap, international, sector, bonds) and alongside fees and drawdown data. The main metric is the **5-year annualized total return** (dividends reinvested).

## Repository contents
| File | Description |
|---|---|
| [`data/ETF_analysis.xlsx`](data/ETF_analysis.xlsx) | Comparison of 50 large US-listed ETFs: AUM, expense ratio, 1Y and 5Y returns, rankings, drawdown detail, sources and notes |
| [`data/ETF_data_sources.xlsx`](data/ETF_data_sources.xlsx) | List of data elements and where to find them (Yahoo Finance, FRED, Trackinsight, Kaggle datasets, etc.) |

### Sheets in `ETF_analysis.xlsx`
- **Summary** – top 10 ETFs and best ETF per category (formula-driven)
- **ETF Data** – raw data and formulas for the 50 ETFs
- **Risk Detail** – 3-year returns, drawdowns and 1-year Sharpe ratios for a few ETFs
- **Sources & Notes** – links, as-of dates, data conflicts and gaps

## Data elements identified
Identification (ticker, issuer, category), price and return data, risk metrics (volatility, drawdown, beta), risk-adjusted metrics (Sharpe, Sortino), costs (expense ratio, tracking error), size and liquidity (AUM, volume), portfolio composition, and market context (benchmark, risk-free rate).

## Key findings (data as of 8 Oct 2026)
- Semiconductor and tech sector funds had the highest 5-year returns (SMH about 37.5% a year, SOXX about 31.7%), but they are concentrated and have higher fees.
- Among broad US funds, Nasdaq-100 funds (QQQM, QQQ) led at about 16% a year, versus about 13.6% for S&P 500 funds.
- S&P 500 funds (VOO, IVV, SPY, SPYM) perform almost identically, so fees decide between them.
- Higher returns came with deeper drawdowns: QQQ's worst 5-year drawdown was about -35% versus about -25% for VOO.
- Bond funds lost money over five years.

## Data sources
- [chartrow.com – Biggest ETFs](https://chartrow.com/lists/biggest-etfs)
- [totalrealreturns.com](https://totalrealreturns.com/n/QQQ,VOO,VOOG,VT,VTI,VXUS)
- [PortfoliosLab](https://portfolioslab.com/tools/stock-comparison/VOOG/QQQM)
- [Motley Fool – VOO vs QQQ](https://www.fool.com/coverage/etfs/2026/07/07/voo-vs-qqq-which-index-fund-is-the-better-buy-for-long-term-investors/)
- Other sources considered: Yahoo Finance (`yfinance`), FRED (DTB3), Trackinsight, ETF Central

## Method
5-year annualized return = (1 + 5-year cumulative total return)^(1/5) − 1. Ranks and category winners are calculated with spreadsheet formulas, so they update if the inputs change.

## Limitations
- Volatility, Sharpe and Sortino ratios were not available for most of the 50 ETFs. A full risk-adjusted ranking needs daily price data (e.g. via `yfinance`).
- Categories are assigned by the authors.
- Some sources disagree (e.g. VOO's AUM); see the *Sources & Notes* sheet.
- Past performance does not predict future returns. This project is for educational purposes and is not financial advice.

## Next steps
- Download daily prices and compute volatility, Sharpe, Sortino and max drawdown for all ETFs
- Add tracking error and premium/discount to NAV
- Build charts or a dashboard

