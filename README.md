# Quant Transition Log

A public log of my transition from actuarial science into quantitative finance. Each project rebuilds an actuarial technique in a quant workflow, or applies quant methods to real market data, with the reasoning written up alongside the code.

**Status:** Phase 1 (Technical Bridge), Week 1
**Last updated:** <!-- YYYY-MM-DD -->

---

## About

I'm a student with an actuarial science background: probability, statistics, time value of money, risk models, and life and financial contingencies. I'm building on that foundation toward stochastic calculus, market microstructure, and production-quality Python and C++.

The premise of this repo is that actuarial thinking transfers to quant work more than people assume, but some habits need to change (conservative smoothing vs. edge-seeking, real-world vs. risk-neutral probabilities, loop-based vs. vectorized code). I document both the transfers and the corrections.

**Contact:** <!-- LinkedIn / email -->

---

## Repository Structure

```
quant-transition-log/
├── notebooks/     # Analysis notebooks, numbered in the order written
├── src/           # Reusable modules (data fetching, tear sheets, etc.)
├── data/          # Local data cache (git-ignored, regenerate via src/)
├── environment.yml
└── README.md
```

Data files are not committed. Run the fetch module in `src/` to rebuild the local cache.

---

## Setup

```bash
git clone https://github.com/<your-username>/quant-transition-log.git
cd quant-transition-log

conda env create -f environment.yml
conda activate quant

jupyter lab
```

Python 3.11. Core stack: NumPy, pandas, SciPy, statsmodels, matplotlib, seaborn, yfinance, pyarrow.

---

## Contents

### Phase 1: Technical Bridge (Weeks 1-4)

| # | Notebook | What it does | Actuarial link | Status |
|---|----------|--------------|----------------|--------|
| 00 | `00_setup_check.ipynb` | Environment smoke test: pulls SPY data, writes Parquet | n/a | Done |
| 01 | `01_mortality_pandas.ipynb` | Rebuilds a mortality / annuity calculation in vectorized pandas | Life contingencies | Planned |
| 02 | `02_yield_curve_pv.ipynb` | Present value using an interpolated market yield curve instead of a flat rate | Time value of money | Planned |
| 03 | `03_reserve_triangle_backtest.ipynb` | Treats each diagonal of a loss triangle as a point-in-time forecast and measures forecast error | Loss reserving | Planned |
| 04 | `04_tearsheet_demo.ipynb` | Tear sheet (cumulative returns, drawdown, rolling Sharpe) for a simple moving-average strategy | n/a | Planned |

### Later phases

- **Phase 2 (Months 2-3):** Stochastic calculus and derivatives pricing, plus a Monte Carlo option pricer validated against Black-Scholes.
- **Phase 3 (Months 4-5):** Statistical arbitrage / mean-reversion backtester with realistic transaction costs and slippage.
- **Phase 4 (Month 6):** Interview preparation and outreach.

---

## Progress Tracker

- [x] Development environment set up
- [ ] Python for data analysis course completed
- [ ] Data-fetch module with Parquet caching (`src/`)
- [ ] Three actuarial-to-quant translation notebooks
- [ ] Reusable tear sheet module (`src/`)
- [ ] C++ course: Level 1
- [ ] C++ course: Level 2

---

## Actuarial to Quant: Lessons Log

Short notes on where actuarial intuition helped and where it misled me. Newest first.

<!--
Template:
### YYYY-MM-DD: Title
- **What I was doing:**
- **Where the actuarial instinct helped:**
- **Where it needed correcting:**
-->

*No entries yet.*

---

## Disclaimer

This repository is for learning and research. Nothing here is investment advice. Backtested results do not predict future performance, and early notebooks use deliberately simplified strategies to test the pipeline, not to find tradable edge.