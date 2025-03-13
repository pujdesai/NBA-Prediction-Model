# NBA Game Outcome Prediction Model

This repository implements a machine learning project that predicts NBA game outcomes using historical game data. The project retrieves data using the nba_api, computes rolling averages for key game statistics, and trains a classifier to predict whether a team will win.

## Project Overview

The modeling approach involves the following steps:

1. **Data Retrieval**
   - Historical NBA game data is collected using nba_api endpoints such as `leaguegamefinder` and `leaguedashteamstats`.
   - Data is gathered across multiple seasons to ensure a robust dataset.

2. **Data Combination & Cleaning**
   - The `combine_team_games` function merges game records by joining home and away statistics based on common game identifiers.
   - The data is filtered and cleaned to ensure that each game’s statistics are correctly aligned for both teams.

3. **Feature Engineering with Rolling Averages**
   - A custom function, `rolling_averages`, computes 5-game rolling averages for several statistical metrics. This smooths out short-term fluctuations and captures recent performance trends.
   - New rolling-average features are added to the dataset, preparing it for model training.

4. **Target Variable Creation**
   - Win/loss outcomes are encoded as a binary target (1 for win, 0 for loss) in the `df_with_target` function.

5. **Model Training & Evaluation**
   - A Gaussian Naive Bayes classifier is used to predict game outcomes.
   - The dataset is split into training and testing subsets separately for home and away games.
   - Model performance is measured using accuracy and precision metrics.

6. **Prediction Function**
   - The `predictor` function utilizes the most recent rolling averages to predict the outcome of upcoming games, providing a simple interface for generating predictions.
