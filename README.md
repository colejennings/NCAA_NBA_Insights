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
Final_NCAA.xlsx
```
The NBA dataset is contained in 
```sh
NBA_Matrix.xlsx
```

## 3. Variable Explanation
### NBA
| Variable | Definition |
| ------ | ------ |
| PTS | Average points scored in a game |
| 3P% | Three Point Percentage |
| FT% | Free Throw Percentage |
| OREB | Offensive Rebounds |
| DREB | Defensive Rebounds |
| AST | Assists |
| TOV | Turnovers |
| STL | Steals |
| BLK | Blocks |
| BLKA | Blocks Agianst |
| PF | Personal Fouls |
| PFD | Personal Fouls Drawn |
| Made_Playoffs | If the team made the playoffs or not (Binary) |
| Conf_West | If the team belonged to the western conference (Binary) |
