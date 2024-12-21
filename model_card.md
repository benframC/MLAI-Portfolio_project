# Model Card

## Model Description

**Input:** Describe the inputs of your model 

Site, building, and meter IDs
Building use
Building floor area
Year built
Building floor count
Hourly weather: air temperature; cloud coverage; dew temperature; precipitation depth; sea level pressure; wind direction; wind speed
Hourly meter reading
Timestamp

**Output:** Describe the output(s) of your model

R2 performance metrics for various decision tree and random forest architectures.

**Model Architecture:** Describe the model architecture you’ve used

Both Scikit-learn's DecisionTreeRegressor and RandomForestRegressor are used. 

## Performance

After finding the best maximum depth in my decision tree to be 15 with a validation R2 score of 0.88166 (up from 0.86179 when no maximum depth was set on a different seed, and 0.69154 when the data wasn't shuffled before train-validation splitting), I used this depth to inform my random forest regressor.

The initial random forest R2 validation score was 0.89140. I then wished to perform a grid search, but to save on computing demand, I dropped some features that appeared meaningless.

After a grid search over the hyperparameters mentioned above, I find negligible improvement to an R2 validation score of 0.89224.

## Limitations

The grid search used is arbitrarily constrained. This was done due to limited computer processing power. The trees are also likely not optimal for this problem as it's trying to predict time series. I have structured the problem to predict hours randomly in time (training and test data are sampled from a shuffled chronological dataset), whereas nearby time signatures are obviously important, so another algorithm better suited to time series analyses would be preferred. This wasn't the focus of the project, however. 

## Trade-offs

The grid search used for the random forest hyperparameter tuning is small due to limited processing resource. This only offers a slight improvement on an untuned random forest, and slightly more improvement on an untuned decision tree, so the trade-off is likely not valuable in this case. 
