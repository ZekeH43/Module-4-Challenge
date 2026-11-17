# Whale Portfolio Analysis

This is a preserved **FinTech course notebook**, updated with a project overview and basic source-integrity checks. The original assignment code remains in [Starter_Code/whale_analysis.ipynb](Starter_Code/whale_analysis.ipynb).

## Purpose

The exercise uses Python to analyze historical returns across large investor ('whale') portfolios, algorithmic strategies, and market benchmarks. It is intended as a learning artifact and **has not been revalidated as a production or live-data application**.

## Repository layout

- Main notebook: `Starter_Code/whale_analysis.ipynb`
- Source data: aapl_historical.csv, cost_historical.csv, goog_historical.csv, sp500_history.csv, algo_returns.csv, and whale_returns.csv under Starter_Code/Resources/
- `scripts/validate_assets.py`: built-in Python checks that notebooks are readable JSON and included CSV files have headers
- `.github/workflows/source-integrity.yml`: runs the source checks on pull requests

## Running locally

1. Use an isolated Python environment suitable for the historical notebook. Start with Python 3.10/3.11, adjusting packages as necessary.
2. From the repository root, optionally create a virtual environment:
   ```bash
   python -m venv .venv
   # Windows: .venv\Scripts\activate
   # macOS/Linux: source .venv/bin/activate
   python -m pip install notebook pandas numpy matplotlib seaborn hvplot
   ```
3. Launch Jupyter with the notebook directory as the working directory:
   ```bash
   cd Starter_Code
   jupyter notebook whale_analysis.ipynb
   ```
4. Review the notebook's imports, file paths, package versions, and any external-data requirements before running cells in order.

The installation command is an **unverified starting point**, not a pinned or tested dependency set. Historic data formats and package APIs may need additional work.

## Lightweight repository validation

Run from the repository root:

```bash
python scripts/validate_assets.py
```

This checks file integrity only: it **does not execute notebooks, train models, test analytics, or validate numerical outcomes**.

## Limitations and portfolio context

The full notebook includes historical saved outputs, and the accompanying CSVs are snapshots rather than live market feeds.

For an internship discussion, explain the data preparation, methods selected, evaluation limits, and what you would improve for reliable reproducibility. Original notebooks and assignment resources remain preserved.
