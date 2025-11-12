# Project Proposal — Rugby Portfolio Analytics

## Project Title and Category
**Title:** Rugby Portfolio Analytics: Predicting Player Performance with Machine Learning
**Category:** Data Analysis & Visualization / Machine Learning (Sports Analytics & Finance Hybrid)

## Problem Statement or Motivation
In professional rugby, player evaluation often relies on subjective assessments or isolated statistics. Yet, player performance and consistency can be analyzed much like financial assets — each player generates "returns" (points, assists, tackles) but also carries "risk" (injuries, inconsistency, variability).

This project aims to develop a data-driven framework that applies machine learning to predict future player performance from historical data. The predictions will then feed into a portfolio-style optimization model, helping identify an "optimal team" that balances expected performance and risk — similar to how investors optimize portfolios for return and volatility.

The motivation is both personal and academic: combining a passion for rugby with quantitative analysis and predictive modeling, bridging sports data and financial logic.

## Planned Approach and Technologies

Dataset: Kaggle - Stats best rugby player 2023/2024
Link: https://www.kaggle.com/datasets/pierrejeanne/stats-best-rugby-player-20232024
Description: 100 top professional rugby players with 30+ features including club/national performance (matches played, wins/losses, tries, points, minutes), physical attributes (age, height, weight, position), and discipline records (yellow/red cards) from the 2023-2024 season.
The project will be implemented in two major stages:

**1. Predictive Modeling (Machine Learning core)**

Use Python (pandas, NumPy, scikit-learn) to preprocess and analyze the rugby player dataset. Create predictive features: past performance averages (rolling windows), minutes played, age, position, workload metrics, and win/loss ratios. Train and compare four regression models:

- Linear Regression (baseline)
- Ridge Regression (regularized linear model)
- Random Forest (ensemble method)
- Gradient Boosting (advanced ensemble)

Models will predict a player's future performance metric (e.g., points per match or overall rating). Temporal validation strategy: Train on early-season data (September 2023 - January 2024), test on late-season data (February 2024 - June 2024) to simulate real-world prediction scenarios and avoid data leakage. Evaluate models using MAE, RMSE, and R², comparing against a naive baseline (average of recent performances).

**2. Portfolio Optimization (Application Layer)**

Use model predictions as the expected return (μ) for each player. Estimate risk (σ) from prediction variance or past performance volatility. Build a simplified portfolio optimization using scipy.optimize: select an "optimal XV" that maximizes predicted performance while maintaining positional diversity (8 forwards, 7 backs). Visualize results using matplotlib and seaborn (e.g., performance distributions, efficient frontier).
Development will take place in VS Code, with version control and documentation through Git and GitHub.

## Expected Challenges and Mitigation

- Limited dataset size (100 players): Mitigate by using cross-validation in combination with temporal split, and focusing on feature engineering to extract maximum information from available data.
- Data leakage / overfitting: Use strict time-based split (train on early season, test on late season) to ensure realistic evaluation. Apply regularization techniques (Ridge) to prevent overfitting.
- Positional bias: Normalize performance metrics by position or train position-specific models if performance varies significantly across positions.
- Model interpretability: Use feature importance (Random Forest, Gradient Boosting) and coefficient analysis (Linear/Ridge) to explain predictions and validate model reasoning.

## Success Criteria
The project will be successful if it:

- Produces working ML models that predict player performance better than a naive baseline across all four algorithms.
- Demonstrates clear performance differences between models, with documented MAE, RMSE, and R² metrics.
- Shows interpretable relationships between features (e.g., age, workload, past performance) and predicted performance through feature importance analysis.
- Generates professional visualizations (feature importance plots, prediction vs. actual, model comparison charts).
- Demonstrates clean, reproducible code with proper Git versioning (minimum 20 meaningful commits).
- Successfully integrates predictions into a functioning "team portfolio" optimization framework.

## Stretch Goals
If time allows, the project could be extended by:

- Developing a Streamlit dashboard for interactive exploration of predictions and player rankings.
- Implementing hyperparameter tuning (GridSearchCV) to optimize model performance.
- Adding a Neural Network model (using TensorFlow/Keras) as a fifth comparison point.
- Incorporating ensemble averaging across multiple models to improve prediction robustness.
- Extending the portfolio optimization to include budget constraints (simulated player salaries) for added realism.