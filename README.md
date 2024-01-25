# Advanced Prediction Models for Scrabble Players Ratings

## Project Overview
Woogles.io is a gameplay website that hosts scrabble games, and it offers the choice of playing against 3 different levels of robots for the players. The primary goal of this project is to develop a predictive model that can accurately estimate the ratings of human players based on their gameplay in Scrabble matches. This estimation is based on comprehensive gameplay data collected from approximately 73,000 matches played between human players and three different bots (BetterBot, STEEBot, and HastyBot), each representing varying skill levels from beginner to advanced.

## Dataset Description
(https://www.kaggle.com/competitions/scrabble-player-rating)
The dataset encompasses multiple components, each offering insights into different aspects of the games:
1. Games Metadata (games.csv): This file provides essential metadata for each Scrabble game, including unique game IDs, player information, time controls, game outcomes, and additional game settings like lexicon used and time limits.
2. Gameplay Data (turns.csv): Detailed turn-by-turn data is available in this file, documenting each move's specifics, including player racks, move locations, points scored, and turn types.
3. Player Scores and Ratings (train.csv and test.csv): These files are crucial for the model's training and evaluation. 'train.csv' comprises players' final scores and their ratings before the game, used for training the model. 'test.csv' includes similar data but lacks the players' pre-game ratings, which the model aims to predict.

## Solution Overview
In this project report, we will outline our systematic approach to solving this challenge step by step. We started with a very comprehensive data preprocessing and feature engineering process to generate and transform the raw features into more informative metrics. With visualizations of the player statistics, we were able to further understand and clean up our data to prepare for modeling. After aggregating the features at hand, we proceeded to build Random Forest, XGBoost, and LightGBM models to predict the players’ ratings at best.
1. Data Preprocessing and Feature Engineering
2. Data Visualization and Analysis
3. Model Development and Comparison

## Predictive Models
Once our data was prepared, we decided to use three different models:
- XGBoost
- LightGBM
- Random Forest.
XGBoost, LightGBM and Random Forest were all obvious choices for this project. This dataset is both large and highly complex. As a result, it stands to reason that a predictive model that is able to handle numerous types and facets of data well would be a good candidate. And due to the underlying structure of both XGBoost and LightGBM being based off of decision trees, we elected to try these models first. Since they all achieved such strong results, we did not feel the need to pursue other options.

## Summary
After multiple attempts, we've achieved our best result with a private score of 98.75 and a public score of 101.58. This marks a significant improvement from our initial score of 196. In this context, lower scores are better. From this project, we think there are two main factors that help our progress.
1. Feature Engineering: Feature importance analysis provided by each model helps us understand which factors have the most significant impact on predicting performance ratings and identify key features that strongly influence a player's performance in Scrabble.
2. Model Comparison: By comparing the performance of different models, such as XGBoost, LightGBM and Random Forest, we can get the best fit model for prediction.


