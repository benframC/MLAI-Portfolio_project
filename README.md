### Final portfolio project - Predicting electricity consumption for building energy use


# Non-technical explanation
I have tested the performance of various machine learning techniques to predict hourly electricity usage profiles, which would be useful to identify if an energy saving initiative is working, for example. The purpose here was not an advanced optimisation of the prediction problem, but to instead personally learn to use some techniques that might be applicable to energy data in general and understand the performance differences. The dataset used is publicly available from The American Society of Heating, Refrigerating and Air-Conditioning Engineers (ASHRAE) and comprises metered electricity consumption of hundreds of buildings in the USA.

# Data
Data is sourced from ASHRAE's Kaggle competition, the Great Energy Predictor III (https://www.kaggle.com/competitions/ashrae-energy-prediction/overview). 

Input data: 
- Site, building, and meter IDs
- Building use
- Building floor area
- Year built
- Building floor count
- Hourly weather: air temperature; cloud coverage; dew temperature; precipitation depth; sea level pressure; wind direction; wind speed
- Hourly meter reading
- Timestamp

## Models
A summary of the model you’re using and why you chose it. 

I tried two models from scikit-learn: DecisionTreeRegressor and RandomForestRegressor. I chose these as I wanted to expand on my learning from the training course and they could be relevant in my work, which is also related to energy consumption data. 

## Hyperparameter optimisation
I used a grid search to attempt to optimise the hyperparameters of the random forest: number of trees; maximum number of features to consider when looking for the best split; and minimum number of samples required to split an internal node. I also played around with the maximum tree depth. 

## Results
After finding the best maximum depth in my decision tree to be 15 with a validation R2 score of 0.88166 (up from 0.86179 when no maximum depth was set on a different seed, and 0.69154 when the data wasn't shuffled before train-validation splitting), I used this depth to inform my random forest regressor. 

The initial random forest R2 validation score was 0.89140. I then wished to perform a grid search, but to save on computing demand, I dropped some features that appeared meaningless. 

After a grid search over the hyperparameters mentioned above, I find negligible improvement to an R2 validation score of 0.89224. 
