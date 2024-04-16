# Which Factors Are Most Determinant of Playoff Berths? An Analysis of Men's NCAA Basketball and the NBA

## 1. Introduction
Our project analyses which factors play the largest roll in NBA teams making the playoffs and Men's NCAA teams making the March Madness Tournament. We use machine learning techniques to predict if a team will make the playoffs and to discover what factors are involved when a team does make it. We used python to create XGBoost Decision Trees for both the NBA and NCAA playoffs and compared their accuracies as well as feature importances.

### Libraries Used
```sh
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import statsmodels.formula.api as sm
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
import xgboost as xgb
import numpy as np
```
## 2. The Excel Files
The NCAA dataset is contained in 
```sh 
Final_df
```
The NBA dataset is contained in 
```sh
NBA_Matrix
```
To make NBA_Matrix, these steps must be taken:
```sh
NBA = pd.read_excel('/Users/thomassniezek/Downloads/nba_team_stats_00_2019_playoffsinc.xlsx')
#remove non numeric columns
NBA_num = NBA.drop(['TEAM', 'Team and Season', 'SEASON', 'CONF'], axis = 1)
#remove unwanted variables
NBA_Matrix = NBA_num.drop(['GP','W','L','WIN%','MIN','FGM','FGA','3PM','3PA','FTM','FTA','REB','FG%','+/-'],axis=1)
```
To make Final_df, these steps must be taken:
```sh


```

## 3. Variable Explanation
