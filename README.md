# **League of Legends Esports Match Prediction Model**

**Is it possible to determine the winner based on data available at the 15th minute of a match?**

This project aims to predict that using a predictive model on LoL esports matches played in 2025 across the major leagues and international tournaments.

## Summary

#### Goals
- Predict the outcomes of League of Legends esports matches based on data available at the 15th minute of a match.
- Have the model predictions be more accurate than a simple rule-based prediction I come up with for each match.
- Investigate matches that were incorrectly predicted with a high probability.

#### Scope
Matches played in 2025 across the major leagues and international tournaments.

#### Key Finding
While the model didn't perform that much better than a rule based prediction system I developed, it highlighted a number of interesting matches where a team had a significant lead at 15 minutes but ended up losing.

## The Dataset
The dataset was sourced from Oracle's Elixir: [Match Data Downloads](https://oracleselixir.com/tools/downloads)

#### Features
The main features used in the model were:
- Gold difference @ 15
- XP difference @ 15
- Kills @ 15
- Winrate difference over last 10 matches
- Turret plate count (in-game objective)
- Void grub count (in-game objective)
- First dragon (in-game objective)

## Tools Used
- **Language**: Python
- **Libraries**: Pandas, Scikit-learn, NumPy, SciPy, LightGBM, Matplotlib, Seaborn

**Approach**: Apply Logistic Regression, followed by Random Forest and LightGBM to compare results.

## Results
- Predictive model accuracy: **70%**
- My rule based predictor accuracy: **68%**

Although the model is only very slightly better, this isn't too surprising given the volatile nature of the game where a lead at 15 minutes doesn't always mean a lot and can be flipped in the span of 5 minutes.

## Feature Importance
As expected, the most important feature by far was the **gold difference at 15 minutes**. This is expected given that it's the main indicator of which team has a lead, especially in the early stages of a match.

