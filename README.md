# Oil-Price-Event-Analysis
This project uses time series analysis to detect structural breaks in Brent crude oil prices and quantifies the impact of major geopolitical events, OPEC policies, and economic sanctions.

# Bayesian Change Point Detection in Brent Oil Prices

This project uses **Bayesian statistical modeling** with **PyMC3** to detect structural change points in **Brent crude oil prices**. By modeling log returns and using a switch-point approach, we identify potential market regime changes that could correspond to significant economic events or shifts in volatility.

---

## 🔍 Project Objectives

- Load and clean Brent oil price data.
- Analyze time series behavior and test for stationarity.
- Transform the data using **log returns** for more stable modeling.
- Apply **Bayesian change point detection** using PyMC3.
- Visualize and interpret the posterior distribution of change points and associated parameters.

---

---

## 🛠 Tools & Technologies

- **Python 3.10+**
- **Pandas**, **NumPy**, **Matplotlib**
- **Statsmodels** – ADF stationarity test
- **PyMC3** – Bayesian modeling
- **Arviz** – Posterior diagnostics and visualization

---

## 📈 Methodology Overview

1. **Data Loading & Cleaning**  
   Load Brent oil prices and ensure date parsing and sorting.

2. **Exploratory Analysis**  
   Plot raw prices and observe macroeconomic patterns.

3. **Stationarity Testing**  
   Use the Augmented Dickey-Fuller test to assess stationarity.

4. **Log Return Transformation**  
   Apply log transformation to make the series more stable.

5. **Bayesian Modeling**  
   - Model mean return as a two-regime system.
   - Define a switch point `τ` with uniform prior.
   - Use normal priors for means (`μ1`, `μ2`) and shared volatility (`σ`).
   - Apply PyMC3's `pm.math.switch` for likelihood definition.
   - Fit model using NUTS sampler and inspect posterior results.

6. **Visualization**  
   Plot the posterior distribution of the change point and compare the detected regime means.

---

## 📊 Key Results

- Identified **probable structural break point** in the return series.
- Inferred changes in **mean returns** before and after the switch.
- Provided **probabilistic insight** into regime changes using Bayesian statistics.

---

## 📦 Setup Instructions

1. **Clone the repository:**

```bash
git clone https://github.com/yourusername/bayesian-change-point.git
cd bayesian-change-point


## Create virtual environment and install dependencies

python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt

