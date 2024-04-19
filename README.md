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

### NCAA
| Variable | Definition |
| ------ | ------ |
| TEAM | Team and season for which the variables correspond to |
| ADJOE | Points scored/100 offensive possessions |
| ADJDE | points allowed/100 defensive possessions |
| EFG_O | Effective field goal % (offense) |
| EFG_D | Effective field goal % (defense) |
| TOR | Turnover rate (on offense) |
| TORD | Turnover rate (on defense) |
| ORB | Offensive rebounding rate |
| DRB | Defensive rebounding rate |
| FTR | Free throw rate (offensive) |
| FTRD | Free throw rate (defensive) |
| playoffs_binary | Playoffs binary variable (1 = made playoffs, 0 = did not make playoffs) |
| CONF_ACC | ACC Conference Dummy ( 1 = belongs to ACC, 0 = other conference) |
| CONF_B10 | Big 10 Conference Dummy ( 1 = belongs to Big 10, 0 = other conference) |
| CONF_B12 | Big 12 Conference Dummy ( 1 = belongs to Big 12, 0 = other conference) |
| CONF_BE | Big East Conference Dummy ( 1 = belongs to ACC, 0 = other conference) |
| CONF_SEC | SEC Conference Dummy ( 1 = belongs to SEC, 0 = other conference) |
| OpEx | Operating Expenses throughout the season (USD$) |
| OpRev | Operating Revenue throughout the season (USD$) |![image](https://github.com/colejennings/NCAA_NBA_Insights/assets/124570541/b2702b95-627d-466b-82b6-2c71c5fce3a1)

