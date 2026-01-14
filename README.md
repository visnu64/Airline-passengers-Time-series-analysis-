# Airline Passengers — Time Series Analysis (ARIMA & SARIMAX)

Overview
--------
This repository contains a time series analysis of the classic "Airline Passengers" dataset using ARIMA and SARIMAX models. The analysis is performed in a Jupyter notebook and explores data loading, visualization, decomposition, stationarity testing, model selection, diagnostics, and forecasting.

Files in this repository
------------------------
- `Time Series analysis(ARIMA and SARIMAX).ipynb` — Jupyter notebook with the full exploratory analysis, modeling steps, diagnostics, and forecasts.
- `airline_passengers.csv` — The dataset used in the notebook (monthly totals of international airline passengers).
- `README.md` — This file.

Dataset
-------
`airline_passengers.csv` is the dataset used for the notebook. It typically contains monthly passenger totals (the canonical dataset spans 1949–1960). The notebook shows how the CSV is loaded and parsed as a datetime-indexed time series.

What the notebook covers
------------------------
- Data loading and initial inspection
- Time series visualization (line plots, seasonal plots)
- Decomposition into trend/seasonality/residuals
- Stationarity checks (ADF test, rolling statistics)
- ACF and PACF analysis
- Fitting ARIMA and seasonal SARIMAX models
- Model selection based on AIC and diagnostic plots
- Forecasting future values and plotting results
- Residual diagnostics and evaluation

Quick start
-----------
1. Clone the repository:
   git clone https://github.com/visnu64/Airline-passengers-Time-series-analysis-.git
2. Change directory:
   cd Airline-passengers-Time-series-analysis-
3. Install the usual Python data stack if you don't already have it. Example:
   pip install pandas numpy matplotlib seaborn statsmodels jupyter pmdarima
   (pmdarima is optional — only needed if the notebook uses auto_arima)
4. Start Jupyter and open the notebook:
   jupyter notebook "Time Series analysis(ARIMA and SARIMAX).ipynb"

Reproducing the analysis
------------------------
- Open the notebook and run the cells in order. The notebook contains explanatory text and plots for each step.
- If the notebook uses any random seeds for reproducibility, the seed is set in the notebook cells.
- To re-run the forecasting experiments change the forecast horizon in the corresponding notebook cell and re-run model fitting/forecast steps.

Notes on modeling
-----------------
- The notebook fits both non-seasonal ARIMA and seasonal SARIMAX models to capture the clear yearly seasonality.
- Model comparison is primarily done using AIC and residual diagnostics (e.g., Ljung-Box test, residual plots).
- If auto-arima (pmdarima.auto_arima) is used, it helps find candidate parameters quickly — always verify diagnostics manually.

Dependencies
------------
Suggested Python packages:
- Python 3.8+
- pandas
- numpy
- matplotlib
- seaborn
- statsmodels
- jupyter
- pmdarima (optional, for auto_arima)

If you want a requirements file generated (requirements.txt), I can create one listing exact package versions used.

License
-------
No license file is included in the repository. If you want a license (MIT, Apache-2.0, etc.), tell me which one and I can add a LICENSE file.

Next steps I can take
---------------------
- Update/replace the repository README.md with this content and push as a commit.
- Generate a requirements.txt with pinned versions extracted from your environment (or recommended versions).
- Add a short script to run the analysis end-to-end (e.g., a Python script that fits the chosen model and saves forecasts).
- Add a LICENSE file if you want one.

If you'd like me to commit the README.md into the repository, tell me the branch name to use (e.g., `main` or a new branch) and I'll prepare the commit message and push it.
