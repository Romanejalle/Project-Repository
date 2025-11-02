# Project Proposal — Rugby Portfolio Analytics

## Project Title and Category
**Title:** Rugby Portfolio Analytics: Predicting Player Performance with Machine Learning
**Category:** Data Analysis & Visualization / Machine Learning (Sports Analytics & Finance Hybrid)

## Problem Statement or Motivation
In professional rugby, player evaluation often relies on subjective assessments or isolated statistics. Yet, player performance and consistency can be analyzed much like financial assets — each player generates “returns” (points, assists, tackles) but also carries “risk” (injuries, inconsistency, variability).

This project aims to develop a data-driven framework that applies machine learning to predict future player performance from historical data. The predictions will then feed into a portfolio-style optimization model, helping identify an “optimal team” that balances expected performance and risk — similar to how investors optimize portfolios for return and volatility.

The motivation is both personal and academic: combining a passion for rugby with quantitative analysis and predictive modeling, bridging sports data and financial logic.

## Planned Approach and Technologies
The project will be implemented in two major stages:

**1. Predictive Modeling (Machine Learning core)**

Use Python (pandas, NumPy, scikit-learn) to preprocess and analyze a dataset of professional rugby players (e.g., from Kaggle or World Rugby).

Create predictive features: past performance averages (rolling windows), minutes played, age, position, and workload metrics.

Train and compare regression models — Linear Regression, Random Forest, and Gradient Boosting — to predict a player’s future performance metric (e.g., points or overall rating per match).

Evaluate models using MAE, RMSE, and R², comparing against a simple baseline (e.g., average of recent performances).

**2. Portfolio Optimization (Application Layer)**

Use model predictions as the expected return (μ) for each player.

Estimate risk (σ) from prediction variance or past performance volatility.

Build a simplified portfolio optimization: select an “optimal XV” that maximizes predicted performance while maintaining positional diversity (8 forwards, 7 backs).

Visualize results using matplotlib and seaborn (e.g., performance distributions, efficient frontier).

Development will take place in VS Code, with version control and documentation through Git and GitHub.

## Expected Challenges and Mitigation

- Data availability: If complete rugby datasets are hard to find, combine multiple public sources or simulate limited variables (e.g., injury risk).
- Data leakage / overfitting: Use a time-based split (train on past seasons, test on later ones) to ensure realistic evaluation.
- Positional bias: Train separate models or normalize performance metrics by position.
- Model interpretability: Use feature importance or SHAP values to explain predictions.

## Success Criteria
The project will be successful if it:

- Produces a working ML model that predicts player performance better than a naive baseline.
- Shows clear relationships between features (e.g., age, workload) and predicted performance.
- Generates interpretable results and visualizations (feature importance, prediction vs. actual).
- Demonstrates clean, reproducible code with proper Git versioning.
- Optionally, integrates predictions into a functioning “team portfolio” optimization.

## Stretch Goals
If time allows, the project could be extended by:

- Developing a Streamlit dashboard for interactive exploration of predictions and player rankings.
- Incorporating a simple injury or availability prediction model to better capture the “risk” aspect.
- Extending the model to team-level predictions (estimating match outcomes from combined player stats).
- Exploring hyperparameter tuning or ensemble averaging to slightly improve prediction accuracy.