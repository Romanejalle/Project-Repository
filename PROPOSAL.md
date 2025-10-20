# Project Proposal — Rugby Portfolio Analytics

## Project Title and Category
**Title:** Rugby Performance Portfolio: A Data-Driven Approach to Player Evaluation 
**Category:** Data Analysis & Visualization (Sports Analytics / Finance Hybrid)  

## Problem Statement or Motivation
In professional rugby, player evaluation is often based on subjective opinions or limited statistics. However, just like in financial markets, each player’s performance can be seen as a combination of return (points scored, assists, tackles completed) and risk (variability, injuries, inconsistency).
The motivation behind this project is to create a data-driven model that evaluates rugby players in the same way investors evaluate financial assets.By analyzing metrics such as points, tackles, assists, minutes played, and availability, the goal is to quantify both performance and consistency.Ultimately, the project aims to build a fair and interpretable ranking of players — and, if possible, an “optimal team portfolio” that balances risk and performance across positions.

## Planned Approach and Technologies
The project will be implemented in two stages:

Player Performance Analysis (Base Model):

Use Python (pandas, NumPy) to load and clean a dataset of professional rugby players (e.g., Kaggle or World Rugby sources).
Compute standardized performance metrics and a “performance-to-risk ratio” (similar to a Sharpe Ratio).
Normalize comparisons by position to account for different roles (forwards vs backs).
Visualize results with matplotlib and seaborn.

Portfolio-Style Team Selection (Stretch Goal):

Treat each player as an asset and build an “optimal XV” using performance and volatility measures.
Ensure positional diversification (8 forwards, 7 backs).
Use NumPy or SciPy for basic optimization and visualize the efficient frontier between performance and risk.

Development will take place in VS Code, with version control through Git and GitHub. 

## Expected Challenges and Mitigation
Data availability and quality: Rugby data can be incomplete; I will combine multiple sources or simulate missing variables (e.g., injuries).

Normalization by position: Handle positional bias by comparing players only within their role.

Defining metrics: Experiment with different formulas for “return” and “risk” until results make sense intuitively.

Optimization complexity: Start with simple averages before using optimization libraries if time permits.

Time management: Divide the work into weekly milestones and track progress through Git commits. 

## Success Criteria
The project will be successful if it:

Produces clean, interpretable results and visualizations;

Generates logical rankings by position;

Demonstrates a clear link between performance and variability;

Is well-documented and version-controlled on GitHub;

(Optional) Successfully builds an optimal “team portfolio.”

## Stretch Goals
If time allows:

Implement the portfolio optimization model;

Create an interactive dashboard (using Plotly or Streamlit);

Analyze performance trends over time;

Integrate new data sources or explore clustering (e.g., K-means for player profiles).
