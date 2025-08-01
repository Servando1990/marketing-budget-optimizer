

# Marketing Budget Optimizer

A machine learning pipeline for optimizing ad campaign pricing and forecasting future budgets using cohort analysis.

## Features

- **Ad Campaign Optimization**: Uses Bayesian Ridge regression with polynomial features to find optimal price per impression
- **Cohort Analysis**: Segments campaigns into cohorts for targeted optimization
- **Budget Forecasting**: Employs Facebook Prophet for time series forecasting of next 14 days
- **Interactive Dashboard**: Dash-based visualization for exploring data and results

## Project Structure

```
src/
├── ad_campaign_optimizer.py  # Core optimization logic using Optuna
├── campaign_manager.py       # Orchestrates cohort optimization and forecasting
├── cohort.py                # Cohort data structures and Prophet forecasting
└── environment.yml          # Conda environment configuration
```

## Requirements

- Conda installed
- Python packages: pandas, numpy, scikit-learn, optuna, prophet, dash

## Setup

1. Create conda environment:
   ```bash
   conda env create -f src/environment.yml
   ```

2. Activate environment:
   ```bash
   conda activate marketing-budget-optimizer
   ```

## Usage

### Exploratory Data Analysis
Navigate to `Example.ipynb` to perform EDA on the marketing data:
- Data exploration and cleaning
- Visualizations for understanding campaign performance
- Price per impression vs conversion analysis

### Interactive Dashboard
Run the Dash application:
```bash
python app.py
```

### Core Pipeline
The main pipeline consists of:
1. **Price Optimization**: Finding optimal price per impression using `AdCampaignOptimizer`
2. **Cohort Management**: Processing multiple cohorts via `CampaignManager`
3. **Budget Forecasting**: Predicting next 14 days spend with Prophet models

## Methodology

1. **Optimization Algorithm**: Uses Optuna to maximize conversion per session by optimizing price per impression
2. **Model**: Bayesian Ridge regression with polynomial features and log transformation
3. **Forecasting**: Prophet time series model with monthly seasonality
4. **Budget Adjustment**: Scales forecasted spend based on optimal vs historical pricing

## Future Enhancements

- Demand curve analysis and price elasticity modeling
- Advanced pricing algorithms considering cost and profit maximization
- Enhanced dashboard visualizations
- Production deployment capabilities


