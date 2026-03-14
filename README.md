# Sector Risk Diagnostics – U.S. Tech Mega-Caps

Dynamic eigenmode decomposition and systemic risk analysis of AAPL, NVDA, TSLA, META using rolling PCA.

## What this project does

- Rolling PCA on daily log returns (126-day window)
- Tracks variance concentration ratio C(t) = λ₁ / Tr(Σ)
- Measures eigenvector stability between windows
- Builds a Systemic Risk Index (SRI) combining concentration, instability, and PC1 volatility
- Computes residual dispersion and its relation to systemic dominance
- Visualizes Monte Carlo efficient frontier (10,000 portfolios)

## Key findings

- Strong PC1 dominance → sector behaves like one asset
- Negative correlation between concentration C(t) and residual dispersion (ρ ≈ -0.13)
- Narrow & steep efficient frontier confirms limited diversification

## Main files

- `main.ipynb`          → complete analysis & visualizations
- `requirements.txt`    → dependencies (yfinance, numpy, pandas, scipy, matplotlib)
- `plots/`              → exported figures (frontier, concentration, SRI, etc.)

## How to run

```bash
# 1. Clone or download the repo
# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook main.ipynb
# or
jupyter lab
