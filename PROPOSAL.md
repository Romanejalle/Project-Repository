# Project Proposal — Rugby Portfolio Analytics

## Project Title and Category
**Title:** Rugby Portfolio Analytics: Predicting Player Performance with Machine Learning  
**Category:** Data Analysis & Visualization / Machine Learning (Sports Analytics & Finance Hybrid)

## Problem Statement or Motivation
In professional rugby, player evaluation often relies on subjective assessments or isolated statistics. Yet, player performance can be analyzed like financial assets — each player generates "returns" (points, tackles) but also carries "risk" (injuries, inconsistency).

This project develops a data-driven framework using machine learning to predict future player performance. Predictions feed into a portfolio-style optimization model, identifying an "optimal team" that balances expected performance and risk — similar to how investors optimize portfolios for return and volatility.

The motivation is both personal and academic: combining a passion for rugby with quantitative analysis and predictive modeling.

## Planned Approach and Technologies

**Dataset:** Custom TOP 14 Player Statistics (2023-2025)

Source: Official TOP 14 website (https://top14.lnr.fr/)

Description: A manually curated dataset of approximately 100 top professional rugby players (8-12 per club) from 9 major TOP 14 clubs. The dataset contains 35 features across two complete seasons (2023-2024 and 2024-2025), covering player profiles, playing time, attacking/defensive metrics, kicking statistics, and discipline records.

This two-season structure enables robust temporal validation: training on 2023-2024 data and testing on 2024-2025 data, ensuring realistic evaluation without data leakage.

**1. Predictive Modeling (Machine Learning core)**

Use Python (pandas, NumPy, scikit-learn) to preprocess data and create predictive features: past performance averages, minutes played, age, position, and workload metrics. Train and compare four regression models:

- Linear Regression (baseline)
- Ridge Regression (regularized)
- Random Forest (ensemble)
- Gradient Boosting (advanced ensemble)

Models predict a player's future performance metric. Evaluate using MAE, RMSE, and R², comparing against a naive baseline.

**2. Portfolio Optimization (Application Layer)**

Use predictions as expected return (μ) and estimate risk (σ) from prediction variance. Build portfolio optimization using scipy.optimize to select an "optimal XV" maximizing performance while maintaining positional diversity (8 forwards, 7 backs). Visualize results using matplotlib and seaborn.

## Expected Challenges and Mitigation

- **Limited dataset size:** Mitigate with cross-validation and feature engineering to extract maximum information.
- **Data leakage / overfitting:** Use strict time-based split (train 2023-2024, test 2024-2025) and regularization.
- **Model interpretability:** Use feature importance and coefficient analysis to explain predictions.

## Success Criteria
The project will be successful if it:

- Produces ML models that outperform a naive baseline with documented MAE, RMSE, and R² metrics.
- Shows interpretable feature relationships through feature importance analysis.
- Generates professional visualizations (feature importance, prediction vs. actual, model comparison).
- Demonstrates clean code with proper Git versioning (minimum 20 commits).
- Successfully integrates predictions into a portfolio optimization framework.

## Stretch Goals
If time allows:

- Developing a Streamlit dashboard for interactive exploration.
- Implementing hyperparameter tuning (GridSearchCV).
- Adding ensemble averaging across models for improved robustness.