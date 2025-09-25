## MarketPulse - Local Site Builder (Notebook)

This project generates a static, single-page website showing:

- Industry performance for S&P 500 over 30D, 3M, YTD vs S&P 500
- Top traded stocks by daily dollar volume
- Unusual high volume stocks (volume vs 30D avg)
- Unusual options volumes (Top 10) — optional with Polygon.io API
- Dividend yield leaders (TTM)

### Requirements

- Python 3.10+
- Jupyter Notebook or JupyterLab

Install dependencies:

```bash
pip install -r requirements.txt
```

Optional: set `POLYGON_API_KEY` for options volume aggregation.

### Run

1. Open the notebook:
   ```bash
   jupyter notebook notebooks/build_site.ipynb
   ```
2. Run all cells. Output is written to `dist/index.html`.
3. Open the file in your browser:
   ```bash
   xdg-open dist/index.html
   ```

### Data Sources

- Wikipedia (S&P 500 constituents, sector/sub-industry)
- Yahoo Finance (prices, volumes, dividends) via `yfinance`
- Polygon.io (optional, options snapshots)

### Notes

- All calculations are approximate and for illustration only.
- Industry returns are equal-weighted by constituent.
- "30D" and "3M" use calendar days anchored to nearest trading days.

# Analytics