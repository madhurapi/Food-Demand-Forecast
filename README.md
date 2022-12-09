# Food-Demand-Forecast
#### Problem Statement: 
The client wants centers with demand forecasting for upcoming weeks so that these centers will plan the stock of raw materials accordingly.

#### Evaluation Metric: 
100*RMSLE where RMSLE is Root of Mean Squared Logarithmic Error

#### Approach:
+ Train data including calculated field : Discount, % discount, discount y/n
+ No null values, no duplicates hence EDA was easy to approach.
+ One Hot Encoding 
+ Feature Selection Approach:
    + Centre_id and meal_id had entries more than 77 , 51 resp. labels
    + Getting dummies for these features would lead to dimensionality curse
    + Getting top 30 frequently meal_id and center_id and merging rest of the labels(bcoz other remaining labels are very less frequent)
+ Algorithms(R2 , 100*RMSLE):
    + RF ( 0.76, 64.62)
    + XGBoost ( 0.42 , 86.30)
    + lightgbm and CatBoost
  
#### Source: https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon-1/#AboutRank 
#### AV Rank: 1411/13930
